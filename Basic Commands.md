# MySQL Basic Commands (Beginner Guide)

Ye file **MySQL / MariaDB ke basic commands** cover karti hai — bilkul **`SHOW DATABASES;`** se start karke daily-use commands tak. Ye **DBMS lab, viva, practice** ke liye perfect hai.

---

## 1️⃣ Database Related Commands

```sql
SHOW DATABASES;
```

> Server me jitne bhi databases hain unki list dikhata hai.

```sql
CREATE DATABASE company;
```

> Naya database create karta hai.

```sql
USE company;
```

> Kaam karne ke liye database select karta hai.

```sql
DROP DATABASE company;
```

> Poora database permanently delete kar deta hai.

---

## 2️⃣ Table Related Commands

```sql
SHOW TABLES;
```

> Current database ki saari tables dikhata hai.

```sql
CREATE TABLE student (
    id INT PRIMARY KEY,
    name VARCHAR(20),
    age INT
);
```

> Nayi table create karta hai.

```sql
DESC student;
```

> Table ka structure dikhata hai (columns + data types).

```sql
DROP TABLE student;
```

> Table ko permanently delete karta hai.

---

## 3️⃣ INSERT Commands

```sql
INSERT INTO student VALUES (1, 'Rahul', 20);
```

> Table me ek record insert karta hai.

```sql
INSERT INTO student VALUES
(2, 'Amit', 21),
(3, 'Neha', 22);
```

> Multiple records ek saath insert karta hai.

---

## 4️⃣ SELECT Commands

```sql
SELECT * FROM student;
```

> Table ka poora data dikhata hai.

```sql
SELECT name, age FROM student;
```

> Sirf selected columns dikhata hai.

```sql
SELECT * FROM student WHERE age > 20;
```

> Condition ke according data fetch karta hai.

---

## 5️⃣ UPDATE Command

```sql
UPDATE student SET age = 23 WHERE id = 2;
```

> Existing record update karta hai.

---

## 6️⃣ DELETE & TRUNCATE

```sql
DELETE FROM student WHERE id = 1;
```

> Specific record delete karta hai.

```sql
TRUNCATE TABLE student;
```

> Table ka poora data delete karta hai (structure safe rehta hai).

---

## 7️⃣ ALTER TABLE Commands

```sql
ALTER TABLE student ADD marks INT;
```

> Table me naya column add karta hai.

```sql
ALTER TABLE student MODIFY name VARCHAR(50);
```

> Column ka data type change karta hai.

```sql
ALTER TABLE student DROP marks;
```

> Column delete karta hai.

---

## 8️⃣ Constraints (Basics)

```sql
CREATE TABLE department (
    deptno INT PRIMARY KEY,
    dname VARCHAR(20)
);
```

> PRIMARY KEY example.

```sql
CREATE TABLE employee (
    empno INT PRIMARY KEY,
    ename VARCHAR(20),
    deptno INT,
    FOREIGN KEY (deptno) REFERENCES department(deptno)
);
```

> FOREIGN KEY example.

---

## 9️⃣ Useful Utility Commands

```sql
SELECT DATABASE();
```

> Currently selected database ka naam dikhata hai.

```sql
SHOW COLUMNS FROM student;
```

> Table ke columns dikhata hai.

```sql
EXIT;
```

> MySQL se bahar nikalne ke liye.

---

## 🔟 Notes for Lab & Viva

* `;` lagana **mandatory** hai
* SQL **case-insensitive** hoti hai
* `DROP` dangerous hota hai (undo nahi hota)
* `DESC` lab exams me kaafi pucha jata hai

---

✅ **Tip:** Is file ko tum VS Code / GitHub / Notepad me open kar sakte ho.

Agar chaho to next:

* JOIN commands
* Aggregate functions (SUM, AVG, COUNT)
* Viva questions


