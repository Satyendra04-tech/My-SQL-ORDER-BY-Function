# Hello all, I am sharing how to use ORDER BY function in SQL  

### SQL sometimes return the same request query results in a different order. We can add <mark> ORDER BY</mark> to sort rows based on column value, in either ascending or descending order.  

* Syntax =  
```
SELECT Column_1, Column_2 FROM table
ORDER BY Column_1 ASC:
```
```
SELECT Column_1, Column_2 FROM table
ORDER BY Column_1 DESC
```   
Here ASC stands for ascending order and DESC stands for descending order.  

### We have to use ORDER BY towards the end of the query because we generally have to do selection and filtering first followed by ordering.  

```
SELECT Column_1, Column_2 FROM table
ORDER BY Column_1
```  
If we do not use ASC/DESC then SQL will take ascending as default.  

### We can use ORDER BY multiple columns when there are duplicate entries in a column.  

## Examples  

### Suppose we have a table T1 which has columns named store_id, first_name, last_name.  

1. Sort the table T1 in ascending first_name.
```
SELECT * FROM T1
ORDER BY first_name;
```

2. Sort the table T1 in ascending store_id followed by ascending first_name.
```
SELECT store_id, first_name FROM T1
ORDER BY store_id, first_name;
```  

3. Sort the table T1 in descending store_id followed by ascending first_name.
```
SELECT store_id, first_name FROM T1
ORDER BY store_id DESC, first_name ASC;
```  

4. Sort the table T1 in descending store_id followed by ascending first_name.
```
SELECT first_name FROM T1
ORDER BY store_id DESC, first_name ASC;
```  
Note = We haven't selected store_id in SELECT statement but still the code will work same.  

## That's it for the WHERE functions, see you in the next chapter !!