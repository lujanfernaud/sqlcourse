# SQLCourse

SQL exercises from [sqlcourse.com](http://www.sqlcourse.com).

## Snippets

Code used for these exercises.

### Comparison Operators

```
=     -- Equal
>     -- Greater than
<     -- Less than
>=    -- Greater than or equal
<=    -- Less than or equal
<>    -- Not equal to
LIKE  -- Compare a value to similar values using wild card operators
```

When using `LIKE`, the percent sign `%` can be used as a wild card to match any character that might appear before or after the characters specified.

#### Examples:

Display the first and last names for everyone whose last name ends in an "ay".

```sql
SELECT first, last
  FROM empinfo
 WHERE last LIKE '%ay';
```

Select first name, last name, and salary for anyone with "Programmer" in their title.

```sql
SELECT firstname, lastname, salary
  FROM employees_jnd2017
 WHERE title LIKE '%Programmer%';
```

### Selecting Data

```sql
SELECT first, last, city
  FROM empinfo
 WHERE city <> 'Payson';
```

### Creating Tables

```sql
CREATE TABLE employees_jnd2017
            (firstname VARCHAR(15),
             lastname  VARCHAR(20),
             title     VARCHAR(30),
             age       NUMBER(2),
             salary    NUMBER(6));
```

### Inserting Into a Table

```sql
INSERT INTO employees_jnd2017
            (firstname, lastname, title, age, salary)
     values ('Jonie', 'Weber', 'Secretary', 28, 19500);
```

### Updating Records

```sql
UPDATE employees_jnd2017
   SET lastname = 'Weber-Williams'
 WHERE firstname = 'Jonie' AND lastname = 'Weber';
```

### Deleting Records

```sql
DELETE FROM employees_jnd2017
      WHERE firstname = 'Jonie'
        AND lastname = 'Weber-Williams';
```

### Dropping a Table

```sql
DROP TABLE employees_jnd2017;
```
