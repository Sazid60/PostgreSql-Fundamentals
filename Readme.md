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

## 44-2 pgAdmin Basics
- use of pgadmin- unnecessary

## 44-3 Install Beekeeper Studio
- beekeeper supports cross platform and cross db 

## 44-4 Integer & Boolean Types
- we can set data type to the attributes of a table 
- Setting data types improves :
    1. Data Accuracy
    2. Memory Efficiency
    3. Performance 
    4. Clarity and Constrains  

![alt text](image-2.png)

### Data Type
- `Boolean (we will commonly use)` 
- `Numbers (we will commonly use)` - 
- Binary 
- `Date/Time (we will commonly use)`
- json
- `Character (we will commonly use)`
- `UUID (we will commonly use)`
- Array 
- XML

#### Boolean 
- true 
- false 
- null 

#### Number / Int 

##### Small Int (int2)
- `Storage` : 2 bytes 
- `Range` : -32,768 to +32,767
- `Use case` : Small numbers (like age,quantity)

##### Integer (int4)
- `Storage` : 4 bytes 
- `Range` : ~ -2B to +2B
- `Use case` : Default choice for whole numbers

##### Bigint (int8)
- `Storage` : 8 bytes 
- `Range` : ~ -9 quintillion to +9 quintillion
- `Use case` : Very large numbers (IDs,counters)


##### Real (float4)
- `Storage` : 4 bytes
- `Range` : ~6 decimal digits precision
- `Use case` : Approximate values (e.g.,sensor data)

##### DOUBLE PRECISION (float8)
- `Storage` : 4 bytes
- `Range` : ~15 decimal digits precision
- `Use case` : Higher precision calculations

##### NUMERIC / DECIMAL
- `Storage` : variable
- `Range` : User-defined precision (exact)
- `Use case` : Money, financial calculations

##### SERIAL
- `Storage` : 4 bytes (auto-increment integer)
- `Range` : 1 to 2,147,483,647
- `Use case` : Auto-incrementing IDs, primary keys


![alt text](image-3.png)


## 44-5 Character, Date & UUID Types
### Character 

#### CHAR

- `Storage` : n bytes
- `Length` : Fixed length n
- `Use case` : When you know the exact length (like country codes:'USA')

#### VARCHAR

- `Storage` : Variable
- `Length` : Up to n characters
- `Use case` : Flexible length but with a max limit (like usernames, emails)

#### TEXT

- `Storage` : Variable
- `Length` : unlimited
- `Use case` : Long text, descriptions,
comments


![alt text](image-4.png)

### DATE 

![alt text](image-5.png)

### UUID 

![alt text](image-6.png)

## 44-6 Create & Drop DB/Table
- Create database 

```

create database school;

```

- Delete a database 

```
drop database school;
```

- create a table 

![alt text](image-7.png)

```
CREATE TABLE students (
  id serial,
  name varchar(50),
  age int,
  isActive boolean,
  dob date 
)
```

- delete a table 

```
drop table students;
```

- there is a safe way to delete a table (if exists delete)

```
drop table if exists students; 
```