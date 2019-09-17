Automation tests of primitive RESTfull API service.

_Do you have any comments or questions? Welcome!_

---
**Technologies:**

Building - **[Gradle](https://github.com/gradle/gradle)**.

Test running and assertions - **[TestNG](https://github.com/cbeust/testng)**.

Running and validation of HTTP requests - **[REST Assured](https://github.com/rest-assured/rest-assured)**.

SQL queries - **[JOOQ](https://github.com/jOOQ/jOOQ)**.

JSON objects - **[org.json](https://github.com/stleary/JSON-java)**.

SQLite database [venv/main.db](venv/main.db) connected by native JDBC.

Tests are separated by classes accordingly to webservice endpoints. 

In case of no response from webservice, suite fails without running any test.

All parameters for tests are managed by [testng.xml](testng.xml) file.

---
**RESTfull API service** [venv/superservice.py](venv/superservice.py) was writen on Python 
using *bottle* and *sqlalchemy* libraries.
Endpoints:
- **/ping/** - just returns code 200 on GET.
- **/authorize/** - returns authorization token (valid for 1 min) for user/password = supertest/superpassword.
- **/api/save_data/** - saves data to *venv/main.db* for authorized user (50% succeeded).

For starting *superservice*, please install Python and import libraries. 

Start with parameter **run**. If need to create database, start with parameter **migrate**. 