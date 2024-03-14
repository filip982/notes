# SQL 

SQL stands for Structured Query Language designed to manipulate data in the Relational Database Management Systems (RDBMS).

## ORDER BY
```
SELECT 
    *
FROM 
    employees
ORDER BY 
    first_name
```

## DISTINCT
```
SELECT DISTINCT
    column1, column2, ...
FROM
    table1;
```

## LIMIT
```
SELECT 
    column_list
FROM
    table1
ORDER BY column_list
LIMIT row_count OFFSET offset;
```
