# Hello MySql

# SQL Command Categories

In MySQL, commands are categorized based on their functionality. Understanding these groups helps in managing database structures, data integrity, and security.



## 📊 Summary Table

| Category | Full Name | Purpose | Key Commands |
| :--- | :--- | :--- | :--- |
| **DDL** | Data Definition Language | Defines database structure | `CREATE`, `ALTER`, `DROP`, `TRUNCATE` |
| **DML** | Data Manipulation Language | Manages data within tables | `INSERT`, `UPDATE`, `DELETE` |
| **DQL** | Data Query Language | Retrieves data | `SELECT` |
| **DCL** | Data Control Language | Manages access and security | `GRANT`, `REVOKE` |
| **TCL** | Transaction Control Language | Manages database transactions | `COMMIT`, `ROLLBACK`, `SAVEPOINT` |

---

## 1. DDL (Data Definition Language)
Used to define or modify the physical structure of the database.
* **CREATE**: Used to create the database or its objects (table, index, function, views).
* **ALTER**: Used to alter the structure of the existing database.
* **DROP**: Used to delete objects from the database.

```sql
-- Example: Creating a new table
CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    email VARCHAR(100)
);
```

## 2. DML (Data Manipulation Language)
Used for managing data within schema objects.

* **INSERT**: Insert data into a table.

* **UPDATE**: Update existing data within a table.

* **DELETE**: Delete records from a database table.
```sql
-- Example: Adding a new record
INSERT INTO students (id, name, email) 
VALUES (1, 'John Doe', 'john@example.com');
```
## 3. DQL (Data Query Language)
Used to fetch data from the database.

* **SELECT**: It is the most used command in SQL. It allows users to pull specific data based on conditions.

```sql
-- Example: Fetching specific data
SELECT name, email FROM students WHERE id = 1;
```

## 4. DCL (Data Control Language)
Used to create roles, permissions, and control access to the database.

* **GRANT**: Gives user access privileges to the database.

* **REVOKE**: Withdraw user access privileges.

## 5. TCL (Transaction Control Language)
Used to manage transactions to ensure data integrity (ACID properties).

* **COMMIT**: Saves the work done.

* **ROLLBACK**: Restores database to original state since the last COMMIT.



**Basic Commands of Database**
---
* CREATE DB
---
```sql
CREATE DATABASE db_name;
```
or
```sql
CREATE DATABASE IF NOT EXISTS db_name;
```
---
*  DROP DB
---
```sql
DROP DATABASE db_name;
```
or
```sql
DROP DATABASE IF EXISTS db_name;
```
---
* SHOW DB
---
```sql
SHOW DATABASES;
```
---
* SHOW TABLES;
---
```sql
SHOW TABLES;
```

---
## **Lets practice sql with task** 
---

###  Task 1        
Create a db for your x-company.create a table inside this db to store employee info(id, name, age, address, job_role ). Add 2 or 3 info on this table. And the last select and view table data. 

### Solutions 

```sql 
CREATE DATABASE x_company;

CREATE TABLE employee(
    employee_id INT PRIMARY KEY,
    employee_name VARCHAR(50),
    employee_age INT NOT NULL,
    employee_address VARCHAR(100),
    employee_job_role VARCHAR(50)
);

INSERT INTO employee
(employee_id, employee_name, employee_age, employee_address, employee_job_role) 
VALUES 
(1001, "MD. Fahim Morshed", 25, "Dhaka, Bangladesh" , "Manager"),
(1002, "MD. Rahim Hasan", 25, "Dhaka, Bangladesh" , "Accountant"),
(1003, "MD. Tarik Alam", 25, "Dhaka, Bangladesh" , "Marketing");


SELECT * FROM employee;

```






