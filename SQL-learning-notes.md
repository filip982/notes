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

## CASE - WHEN
```
SELECT
	InvoiceDate,
	BillingAddress,
	BillingCity,
	total,
	CASE
	WHEN total < 2.00 THEN 'Baseline Purchase'
	when total BETWEEN 2.00 and 6.99 then 'Low Purchase'
	when total BETWEEN 7.00 and 15.00 then 'Target Purchase'
	else 'Top Performer'
	end as PurchaseType
FROM
	Invoice
WHERE	
	total  > 1.98 and (BillingCity LIKE 'P%' OR BillingCity like 'D%')
ORDER BY 
	PurchaseType, InvoiceDate
```

## INNER JOIN
```
SELECT
	c.LastName,
	c.FirstName,
	i.InvoiceId,
	i.CustomerId,
	i.InvoiceDate,
	i.total
FROM
	Invoice as i
INNER JOIN
	Customer as c
ON 
	i.CustomerId = c.CustomerId
ORDER BY 
    c.CustomerId
```

