## MySQL Cheat Sheet

## Table of Contents
- [Basic Commands](#basic-commands)
- [Data Types](#data-types)
- [Database Operations](#database-operations)
- [Table Operations](#table-operations)
- [Data Manipulation](#data-manipulation)
- [Querying Data](#querying-data)
- [Joins](#joins)
- [Indexes](#indexes)
- [Views](#views)
- [Stored Procedures](#stored-procedures)
- [Functions](#functions)
- [Backup and Restore](#backup-and-restore)

## Basic Commands
```sql
-- Connect to MySQL
mysql -u username -p

-- Show all databases
SHOW DATABASES;

-- Select a database
USE database_name;

-- Show all tables in a database
SHOW TABLES;

-- Describe the structure of a table
DESCRIBE table_name;

-- Show all columns in a table
SHOW COLUMNS FROM table_name;

-- Exit MySQL
EXIT;

## Features

- INT: Integer
- VARCHAR(n): Variable length string with max length n
- CHAR(n): Fixed length string with length n
- TEXT: Large text
- DATE: Date (YYYY-MM-DD)
- DATETIME: Date and time (YYYY-MM-DD HH:MM:SS)
- TIMESTAMP: Timestamp
- FLOAT: Floating point number
- DOUBLE: Double precision floating point number
- DECIMAL(m, d): Fixed point number with m digits and d decimals


