# PostgreSQL Notes

PostgreSQL is one of the world’s most advanced **open-source relational database management systems (RDBMS)**.  
It is widely used for building reliable, scalable, and high-performance applications.

---

## What is DBMS vs RDBMS?

- **DBMS**: Database Management System  
- **RDBMS**: Relational Database Management System (data stored in tables with relationships)

PostgreSQL is an **RDBMS** that strictly follows relational principles.

---

## Why Use PostgreSQL?

- Open source and community driven  
- ACID compliant (reliable transactions)  
- Advanced data types (JSON, UUID, Arrays, etc.)  
- High scalability and performance  
- Powerful indexing and query optimization  
- Modern and production-ready

---

## Basic PostgreSQL (psql) Commands

| Command           | Description |
|-------------------|--------------|
| `\l`              | List all databases |
| `\conninfo`       | Show current database connection info |
| `\dt`             | Show all tables in the current database |
| `\!cls`           | Clear terminal (Windows) |
| `\!clear`         | Clear terminal (Linux/macOS) |



### Create Table Example
```sql
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name VARCHAR(50)
);


SQL->(Structured Query Language)
SQL is used to interact with relational databases like PostgreSQL.

Categories of SQL Commands
1. Data Definition Language (DDL)
CREATE
ALTER
DROP
TRUNCATE

2. Data Manipulation Language (DML)
INSERT
UPDATE
DELETE

3. Data Query Language (DQL)
SELECT

4. Data Control Language (DCL)
GRANT
REVOKE

5. Transaction Control Language (TCL)
COMMIT
ROLLBACK

## GUI Tool (Beginner Friendly)
Working directly with SQL in the terminal can be tricky for beginners.
A recommended GUI tool is Beekeeper Studio.


## Why Beekeeper Studio?
1. VS Code–like interface
2. Easy database and table navigation
3. Safe query execution
4. Beginner friendly


PostgreSQL Data Types Commonly Used
Boolean
Numeric
Character
Date / Time
UUID

Less Common but Powerful
JSON / JSONB
Array
XML
Binary



Boolean Type
| Value   |
| ------- |
| `TRUE`  |
| `FALSE` |
| `NULL`  |


Numeric Data Types
| Data Type          | Storage                          |
| ------------------ | -------------------------------- |
| `SMALLINT`         | 2 bytes                          |
| `INTEGER`          | 4 bytes                          |
| `BIGINT`           | 8 bytes                          |
| `REAL`             | 4 bytes                          |
| `DOUBLE PRECISION` | 8 bytes                          |
| `NUMERIC`          | Variable                         |
| `SERIAL`           | 4 bytes (Auto-increment integer) |


Character Data Types
| Type         | Description                | Use Case               |
| ------------ | -------------------------- | ---------------------- |
| `CHAR(n)`    | Fixed length               | Country code (`USA`)   |
| `VARCHAR(n)` | Variable length with limit | Username, email        |
| `TEXT`       | Unlimited length           | Descriptions, comments |


Date & Time Data Types
| Data Type     | Example                  |
| ------------- | ------------------------ |
| `DATE`        | `1980-12-20`             |
| `TIME`        | `14:30:00`               |
| `TIMEZ`       | `14:30:00+06`            |
| `TIMESTAMP`   | `2025-08-29 14:30:00`    |
| `TIMESTAMPTZ` | `2025-08-29 14:30:00+06` |
| `INTERVAL`    | `3 days 4 hours`         |


UUID (Universally Unique Identifier)
Used when you need globally unique IDs.
550e8400-e29b-41d4-a716-446655440000


## Why UUID?
No collision risk across systems
Better for distributed applications
More secure than incremental IDs