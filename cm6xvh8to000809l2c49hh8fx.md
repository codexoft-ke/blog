---
title: "Part 3: Mastering SQL"
seoTitle: "Master SQL: Tips and Techniques"
seoDescription: "Learn SQL basics, joins, aggregation, subqueries, CTEs, window functions, and performance optimization techniques for efficient database management"
datePublished: Sun Feb 09 2025 17:02:40 GMT+0000 (Coordinated Universal Time)
cuid: cm6xvh8to000809l2c49hh8fx
slug: part-3-mastering-sql
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1739120444313/9bf226a2-93f2-4950-a679-5dc954fb65d2.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1739120541639/cdf97010-d4f0-4b97-9deb-ebba3493c913.jpeg
tags: sql-server, backend, databases, sql

---

## **1\. SQL Basics: SELECT, INSERT, UPDATE, DELETE**

### **The Four Pillars of SQL**

SQL (Structured Query Language) is the standard language for interacting with relational databases. Let’s start with the essentials:

#### **SELECT: Retrieve Data**

```sql
-- Select all columns from a table  
SELECT * FROM Employees;  

-- Select specific columns  
SELECT FirstName, Department FROM Employees;  

-- Filter rows with WHERE  
SELECT * FROM Employees  
WHERE Salary > 50000;
```

**Example Output**:

| EmployeeID | FirstName | Department | Salary |
| --- | --- | --- | --- |
| 101 | Alice | Engineering | 75000 |
| 102 | Bob | Sales | 60000 |

---

#### **INSERT: Add New Data**

```sql
-- Insert a single row  
INSERT INTO Employees (EmployeeID, FirstName, Department, Salary)  
VALUES (103, 'Charlie', 'Marketing', 55000);  

-- Insert multiple rows  
INSERT INTO Employees  
VALUES  
  (104, 'Diana', 'HR', 48000),  
  (105, 'Evan', 'Engineering', 72000);
```

---

#### **UPDATE: Modify Existing Data**

```sql
-- Give a raise to all engineers  
UPDATE Employees  
SET Salary = Salary * 1.10  
WHERE Department = 'Engineering';
```

---

#### **DELETE: Remove Data**

```sql
-- Delete an employee by ID  
DELETE FROM Employees  
WHERE EmployeeID = 105;  

-- Delete all interns (use with caution!)  
DELETE FROM Employees  
WHERE Title = 'Intern';
```

---

## **2\. Joins Demystified: INNER, LEFT, RIGHT, and FULL OUTER JOINs**

### **Why Joins Matter**

Joins combine data from multiple tables based on related columns.

**Sample Tables**:  
**Employees**

| EmployeeID | Name | DepartmentID |
| --- | --- | --- |
| 101 | Alice | 1 |
| 102 | Bob | 2 |

**Departments**

| DepartmentID | DepartmentName |
| --- | --- |
| 1 | Engineering |
| 2 | Sales |

---

### **INNER JOIN**

Returns rows where there’s a match in both tables.

```sql
SELECT Employees.Name, Departments.DepartmentName  
FROM Employees  
INNER JOIN Departments  
  ON Employees.DepartmentID = Departments.DepartmentID;
```

**Output**:

| Name | DepartmentName |
| --- | --- |
| Alice | Engineering |
| Bob | Sales |

---

### **LEFT JOIN**

Returns all rows from the left table, even if no match exists in the right table.

```sql
SELECT Employees.Name, Departments.DepartmentName  
FROM Employees  
LEFT JOIN Departments  
  ON Employees.DepartmentID = Departments.DepartmentID;
```

**Output** (if a department is missing):

| Name | DepartmentName |
| --- | --- |
| Alice | Engineering |
| Bob | Sales |
| Charlie | NULL |

---

### **RIGHT JOIN and FULL OUTER JOIN**

* **RIGHT JOIN**: All rows from the right table, with matches from the left.
    
* **FULL OUTER JOIN**: All rows from both tables, with NULLs where no match exists.
    

---

## **3\. Aggregation and Grouping: SUM, COUNT, AVG, and GROUP BY**

### **Summarizing Data**

**Sample Table: Orders**

| OrderID | CustomerID | Amount |
| --- | --- | --- |
| 1 | 101 | 150 |
| 2 | 101 | 200 |
| 3 | 102 | 75 |

---

#### **COUNT and GROUP BY**

```sql
-- Count orders per customer  
SELECT CustomerID, COUNT(OrderID) AS TotalOrders  
FROM Orders  
GROUP BY CustomerID;
```

**Output**:

| CustomerID | TotalOrders |
| --- | --- |
| 101 | 2 |
| 102 | 1 |

---

#### **SUM and AVG**

```sql
-- Total and average sales per customer  
SELECT CustomerID,   
       SUM(Amount) AS TotalSpent,  
       AVG(Amount) AS AverageOrder  
FROM Orders  
GROUP BY CustomerID;
```

**Output**:

| CustomerID | TotalSpent | AverageOrder |
| --- | --- | --- |
| 101 | 350 | 175 |
| 102 | 75 | 75 |

---

#### **HAVING: Filter Aggregated Results**

```sql
-- Customers with total spending over $300  
SELECT CustomerID, SUM(Amount) AS TotalSpent  
FROM Orders  
GROUP BY CustomerID  
HAVING SUM(Amount) > 300;
```

---

## **4\. Subqueries and Common Table Expressions (CTEs)**

### **Subqueries: Queries Within Queries**

```sql
-- Find employees earning more than the average salary  
SELECT FirstName, Salary  
FROM Employees  
WHERE Salary > (SELECT AVG(Salary) FROM Employees);
```

---

### **CTEs: Simplify Complex Queries**

```sql
-- Calculate department-wise average salary  
WITH DeptAvg AS (  
  SELECT Department, AVG(Salary) AS AvgSalary  
  FROM Employees  
  GROUP BY Department  
)  
SELECT * FROM DeptAvg  
WHERE AvgSalary > 60000;
```

**Output**:

| Department | AvgSalary |
| --- | --- |
| Engineering | 73500 |

---

## **5\. Advanced SQL: Window Functions and Recursive Queries**

### **Window Functions**

Perform calculations across related rows without collapsing them into a single output.

```sql
-- Rank employees by salary within their department  
SELECT   
  FirstName,  
  Department,  
  Salary,  
  RANK() OVER (PARTITION BY Department ORDER BY Salary DESC) AS SalaryRank  
FROM Employees;
```

**Output**:

| FirstName | Department | Salary | SalaryRank |
| --- | --- | --- | --- |
| Alice | Engineering | 75000 | 1 |
| Evan | Engineering | 72000 | 2 |
| Bob | Sales | 60000 | 1 |

---

### **Recursive Queries**

Used for hierarchical data (e.g., organizational charts).

```sql
-- Generate a sequence of numbers from 1 to 5  
WITH RECURSIVE Numbers AS (  
  SELECT 1 AS n  
  UNION ALL  
  SELECT n + 1 FROM Numbers WHERE n < 5  
)  
SELECT * FROM Numbers;
```

**Output**:

| n |
| --- |
| 1 |
| 2 |
| 3 |
| 4 |
| 5 |

---

## **6\. Optimizing SQL Queries: Execution Plans and Performance Tuning**

### **Reading Execution Plans**

Use `EXPLAIN` to see how the database executes a query:

```sql
EXPLAIN SELECT * FROM Employees WHERE Department = 'Engineering';
```

**Output**:

```plaintext
Seq Scan on Employees  (cost=0.00..25.00 rows=500 width=44)  
  Filter: (Department = 'Engineering'::text)
```

**Key Takeaways**:

* **Seq Scan**: Full table scan (slow for large tables).
    
* **Index Scan**: Uses an index (faster).
    

---

### **Optimization Tips**

1. **Use Indexes**: Create indexes on frequently filtered columns.
    
    ```sql
    CREATE INDEX idx_department ON Employees(Department);
    ```
    
2. **Avoid SELECT** \* : Fetch only needed columns.
    
3. **Limit Subqueries**: Replace correlated subqueries with JOINs where possible.
    
4. **Batch Inserts**: Use multi-row `INSERT` statements instead of loops.
    

---

## **Conclusion**

SQL is a powerful tool for transforming raw data into actionable insights. By mastering joins, aggregation, and advanced techniques like window functions, you’ll unlock the full potential of your databases.

**Next Up**: In **Part 4: Working with NoSQL Databases**, we’ll explore MongoDB, Redis, and other non-relational systems!

---

### **FAQs**

**Q: What’s the difference between WHERE and HAVING?**  
A: `WHERE` filters rows before aggregation; `HAVING` filters after.

**Q: When should I use a CTE instead of a subquery?**  
A: CTEs improve readability for complex multi-step queries.

**Q: Can window functions modify data?**  
A: No—they only compute values based on row groupings.