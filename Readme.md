# PostgreSql-Fundamentals

Slide Link: https://drive.google.com/file/d/1ZQn4Q4DG9UyybOYUdY8USEFBTb0xo2DL/view?usp=drive_link



In this module, you’ll learn the fundamentals of PostgreSQL. From installing tools like pgAdmin and Beekeeper Studio to understanding key data types (Integer, Boolean, Character, Date, UUID), you’ll build a strong base. You’ll also practice creating and dropping databases/tables, applying constraints, and exploring different insert methods.

By the end, you’ll be ready to structure and manage data confidently in PostgreSQL.

## 44-1 Intro to SQL
- The language we use to talk with databases - aka Structured Query Language
- We wil use postgres and communicate using sql 

![alt text](image.png)

- SQL Is declarative language 
- You tell the database what you want, not how to do it. (database will manage it)
- lets see a sql statement 
```
SELECT name FROM students WHERE age > 18 
```
- Tell step by step is `Imperative` but sql is `declarative`

### SQL commands Category  

- `Data Definition Language` :  CREATE, DROP, ALTER TRUNCATE
- `Data Manipulation Language` : INSERT, UPDATE, DELETE
- `Data Query Language` : SELECT
- `Data Control Language` : GRANT, REVOKE
- `Transaction Control` : COMMIT, ROLLBACK

![alt text](image-1.png)

- So, SQL is a declarative language to interact with databases. It’s old but gold, and still the backbone of all modern data systems
- It’s also powering the future with AI

