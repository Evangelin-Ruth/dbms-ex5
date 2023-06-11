## EXPERIMENT 05: SQL QUERY TO FETCH DUPLICATE RECORDS HAVING MATCHING DATA IN SOME FIELDS OF A TABLE
## AIM:
To write a SQL query to fetch duplicate records having matching data in some fields of a table

## ALGORITHM:
1. Create a database called "MyDatabase" if it does not already exist.
2. Switch to the "MyDatabase" database.
3. Create a table called "students" with columns: "id" (INTEGER, PRIMARY KEY), "name" (TEXT, NOT NULL), and "gender" (TEXT, NOT NULL).
4. Insert sample data into the "students" table.
5. Execute an SQL query to fetch duplicate records by comparing the "name" and "gender" fields.
6. Group the records by "name" and "gender" using the GROUP BY clause.
7. Filter the result to include only combinations that appear more than once using the HAVING clause.
8. Retrieve the names, genders, and counts of the duplicate records.
9. Display the result.

## PROGRAM:
```
create database if not exists MyDatabase;
use MyDatabase;

CREATE TABLE students (
  id INTEGER PRIMARY KEY,
  name TEXT NOT NULL,
  gender TEXT NOT NULL
);

INSERT INTO students VALUES (1, 'Akash', 'M');
INSERT INTO students VALUES (2, 'Amy', 'F');
INSERT INTO students VALUES (3, 'Jacob', 'M');
INSERT INTO students VALUES (4, 'Amy', 'F');
INSERT INTO students VALUES (5, 'Isha', 'F');
INSERT INTO students VALUES (6, 'John', 'M');
INSERT INTO students VALUES (7, 'John', 'M');
INSERT INTO students VALUES (8, 'Amy', 'F');

SELECT name, gender, COUNT(*) as count
FROM students
GROUP BY name, gender
HAVING count > 1;
```
## OUTPUT:
### Original Table:
![image](https://github.com/Evangelin-Ruth/dbms-ex5/assets/94219798/d9a198f2-ac71-4011-b61f-a8eb1ab5936d)
### Duplicate data:
![image](https://github.com/Evangelin-Ruth/dbms-ex5/assets/94219798/ab55d511-48d3-4b71-9683-8e9f5b8ad27c)
## RESULT:
SQL query to fetch duplicate records having matching data in some fields of a table was successful done.

