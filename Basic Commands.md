# MySQL Basic Commands (Beginner Guide)

This file covers **basic MySQL / MariaDB commands** — starting from **`SHOW DATABASES;`** up to commonly used daily commands. It is perfect for **DBMS lab work, viva preparation, and practice**.

---

## 1️⃣ Database Related Commands

```sql
SHOW DATABASES;
```

> Displays the list of all databases available on the server.

```sql
CREATE DATABASE company;
```

> Creates a new database.

```sql
USE company;
```

> Selects a database to work with.

```sql
DROP DATABASE company;
```

> Permanently deletes the database.

---

## 2️⃣ Table Related Commands

```sql
SHOW TABLES;
```

> Displays all tables in the currently selected database.

```sql
CREATE TABLE student (
    id INT PRIMARY KEY,
    name VARCHAR(20),
    age INT
);
```

> Creates a new table.

```sql
DESC student;
```

> Shows the structure of the table (columns and data types).

```sql
DROP TABLE student;
```

> Permanently deletes the table.

---

## 3️⃣ INSERT Commands

```sql
INSERT INTO student VALUES (1, 'Rahul', 20);
```

> Inserts a single record into the table.

```sql
INSERT INTO student VALUES
(2, 'Amit', 21),
(3, 'Neha', 22);
```

> Inserts multiple records at once.

---

## 4️⃣ SELECT Commands

```sql
SELECT * FROM student;
```

> Displays all records from the table.

```sql
SELECT name, age FROM student;
```

> Displays only the selected columns.

```sql
SELECT * FROM student WHERE age > 20;
```

> Fetches data based on a condition.

---

## 5️⃣ UPDATE Command

```sql
UPDATE student SET age = 23 WHERE id = 2;
```

> Updates an existing record.

---

## 6️⃣ DELETE & TRUNCATE

```sql
DELETE FROM student WHERE id = 1;
```

> Deletes a specific record.

```sql
TRUNCATE TABLE student;
```

> Deletes all records from the table (table structure remains intact).

---

## 7️⃣ ALTER TABLE Commands

```sql
ALTER TABLE student ADD marks INT;
```

> Adds a new column to the table.

```sql
ALTER TABLE student MODIFY name VARCHAR(50);
```

> Modifies the data type of a column.

```sql
ALTER TABLE student DROP marks;
```

> Deletes a column from the table.

---

## 8️⃣ Constraints (Basics)

```sql
CREATE TABLE department (
    deptno INT PRIMARY KEY,
    dname VARCHAR(20)
);
```

> Example of PRIMARY KEY.

```sql
CREATE TABLE employee (
    empno INT PRIMARY KEY,
    ename VARCHAR(20),
    deptno INT,
    FOREIGN KEY (deptno) REFERENCES department(deptno)
);
```

> Example of FOREIGN KEY.

---

## 9️⃣ Useful Utility Commands

```sql
SELECT DATABASE();
```

> Displays the name of the currently selected database.

```sql
SHOW COLUMNS FROM student;
```

> Displays the columns of the table.

```sql
EXIT;
```

> Exits from MySQL.

---

## 🔟 Notes for Lab & Viva

* Using `;` at the end of commands is **mandatory**
* SQL is **case-insensitive**


---






