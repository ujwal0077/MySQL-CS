
# MySQL Cheat Sheet

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
```

## Data Types
```markdown
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
```

## Database Operations
```sql
-- Create a new database
CREATE DATABASE database_name;

-- Delete a database
DROP DATABASE database_name;

-- Rename a database
RENAME DATABASE old_name TO new_name;
```

## Table Operations
```sql
-- Create a new table
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    ...
);

-- Delete a table
DROP TABLE table_name;

-- Rename a table
RENAME TABLE old_name TO new_name;

-- Add a column to a table
ALTER TABLE table_name ADD column_name datatype;

-- Drop a column from a table
ALTER TABLE table_name DROP COLUMN column_name;

-- Modify a column in a table
ALTER TABLE table_name MODIFY COLUMN column_name datatype;
```

## Data Manipulation
```sql
-- Insert data into a table
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);

-- Update data in a table
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;

-- Delete data from a table
DELETE FROM table_name
WHERE condition;
```

## Querying Data
```sql
-- Select all columns from a table
SELECT * FROM table_name;

-- Select specific columns from a table
SELECT column1, column2, ...
FROM table_name;

-- Select with a condition
SELECT column1, column2, ...
FROM table_name
WHERE condition;

-- Select with sorting
SELECT column1, column2, ...
FROM table_name
ORDER BY column1 ASC|DESC;

-- Select with grouping
SELECT column1, COUNT(*)
FROM table_name
GROUP BY column1;
```

## Joins
```sql
-- Inner join
SELECT columns
FROM table1
INNER JOIN table2
ON table1.column = table2.column;

-- Left join
SELECT columns
FROM table1
LEFT JOIN table2
ON table1.column = table2.column;

-- Right join
SELECT columns
FROM table1
RIGHT JOIN table2
ON table1.column = table2.column;

-- Full join
SELECT columns
FROM table1
FULL OUTER JOIN table2
ON table1.column = table2.column;
```

## Indexes
```sql
-- Create an index
CREATE INDEX index_name
ON table_name (column1, column2, ...);

-- Drop an index
DROP INDEX index_name
ON table_name;
```

## Views
```sql
-- Create a view
CREATE VIEW view_name AS
SELECT columns
FROM table_name
WHERE condition;

-- Drop a view
DROP VIEW view_name;
```

## Stored Procedures
```sql
-- Create a stored procedure
CREATE PROCEDURE procedure_name (parameters)
BEGIN
    -- SQL statements
END;

-- Call a stored procedure
CALL procedure_name (arguments);

-- Drop a stored procedure
DROP PROCEDURE procedure_name;
```

## Functions
```sql
-- Create a function
CREATE FUNCTION function_name (parameters)
RETURNS return_datatype
BEGIN
    -- SQL statements
    RETURN value;
END;

-- Drop a function
DROP FUNCTION function_name;
```

## Backup and Restore
```sql
-- Backup a database
mysqldump -u username -p database_name > backup_file.sql

-- Restore a database
mysql -u username -p database_name < backup_file.sql
```
