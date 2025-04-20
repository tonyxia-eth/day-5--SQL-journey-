# SQL Learning Journey - Day 5

## Overview
Today marks Day 5 of my SQL journey as part of CS50's Introduction to Databases course. I worked on a variety of queries that allowed me to explore different aspects of SQL, including pattern matching, aggregations, and filtering. I also began learning about the `DISTINCT` command, which I am still wrapping my head around!

## 2.sql — Districts That End in "(non-op)"
**Goal:** List all districts whose names end with "(non-op)".

```sql
-- List districts that are marked as non-operational
SELECT name
FROM districts
WHERE name LIKE '%(non-op)';
Key Concepts:

LIKE and Pattern Matching: The LIKE keyword allows for partial matches. The % symbol is a wildcard that matches zero or more characters.

3.sql — Average Per-Pupil Expenditure
Goal: Find the average amount spent per pupil.




-- Calculate average per-pupil expenditure
SELECT AVG(per_pupil_expenditure)
FROM expenditures;
Key Concepts:

AVG() Function: This function calculates the average of a specified column.

4.sql — Top 10 Cities with Most Public Schools
Goal: Show 10 cities with the most public schools.



-- Top 10 cities with most public schools
SELECT city, COUNT(*) AS total
FROM schools
WHERE type = 'Public School'
GROUP BY city
ORDER BY total DESC
LIMIT 10;
Key Concepts:

COUNT() Function: Counts the number of records in each group.

GROUP BY Clause: Groups the results by the specified column (in this case, cities).

ORDER BY and LIMIT: Orders the results by the total count and limits the result to 10.

5.sql — Cities with 3 or Fewer Public Schools
Goal: Show cities that have 3 or fewer public schools.

-- Cities with 3 or fewer public schools
SELECT city, COUNT(*) AS total
FROM schools
WHERE type = 'Public School'
GROUP BY city
HAVING total <= 3;
Key Concepts:

HAVING Clause: Similar to WHERE, but used to filter results after aggregation (e.g., filtering grouped data).

COUNT() and HAVING: Filters cities based on the number of public schools they have.

DISTINCT Command
I started learning about the DISTINCT command, which is used to eliminate duplicate values from query results. I will continue exploring how to best use it in upcoming tasks!

Next Steps
Further explore the use of DISTINCT.

Work on more advanced SQL queries involving joins and subqueries.

Stay tuned for more updates as I continue this learning journey!


# day-5--SQL-journey-

