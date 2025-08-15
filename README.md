# Google-cybersecurity-Portfolio-Activity-Apply-filters-to-SQL-queries
Portfolio demonstrating SQL queries using AND, OR, NOT, and LIKE operators to investigate login attempts and employee data for cybersecurity scenarios.

## Project Overview
This project demonstrates the use of SQL queries to filter and retrieve information from database tables in a cybersecurity context. The goal was to investigate potential security incidents, including failed login attempts and employee machine updates, using the `log_in_attempts` and `employees` tables.

## Objectives
- Retrieve after-hours failed login attempts.  
- Investigate login activity on specific dates.  
- Identify login attempts outside of Mexico.  
- Retrieve employees in the Marketing department located in the East building.  
- Retrieve employees in Finance or Sales departments.  
- Retrieve all employees not in the Information Technology (IT) department.

## Technologies Used
- SQL (MariaDB / MySQL)
- Word (for documenting queries and explanations)

## SQL Skills Demonstrated
- Filtering with `AND`, `OR`, and `NOT` operators  
- Using `LIKE` for pattern matching  
- Filtering by date and time  
- Querying multiple tables to extract relevant information

## File Contents
- `Apply_filters_to_SQL_queries.docx` : The main portfolio document containing all SQL queries, explanations, and summary.  

## How to Use
1. Open `Apply_filters_to_SQL_queries.docx` to view all queries and explanations.  
2. Queries can be run in a MariaDB or MySQL environment with the provided table structure (`log_in_attempts` and `employees`).  
3. The document can be used to showcase SQL skills for cybersecurity job applications or portfolio reviews.  

## Example SQL Queries
```sql
-- Retrieve after-hours failed login attempts
SELECT *
FROM log_in_attempts
WHERE success = 0
  AND login_time > '18:00:00';

-- Retrieve employees in Marketing department in East building
SELECT *
FROM employees
WHERE department LIKE '%Marketing%'
  AND office LIKE 'East%';

