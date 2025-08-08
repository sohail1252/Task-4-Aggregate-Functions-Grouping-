# Task-4-Aggregate-Functions-Grouping-
Creating table , then inserting values , adding functions last step is Grouping the table 

CREATE TABLE employees (
    emp_id INT PRIMARY KEY,
    name VARCHAR(50),
    department VARCHAR(50),
    salary DECIMAL(10,2)
);

INSERT INTO employees (emp_id, name, department, salary) VALUES
(1, 'John',  'HR',    45000),
(2, 'Alice', 'HR',    52000),
(3, 'Raj',   'IT',    60000),
(4, 'Maria', 'IT',    62000),
(5, 'Ahmed', 'Sales', 40000),
(6, 'Priya', 'Sales', 55000),
(7, 'Karan', 'IT',    58000);


SELECT 
    department, 
    COUNT(*) AS total_employees,  
    AVG(salary) AS avg_salary    
FROM employees
GROUP BY department         
HAVING AVG(salary) > 50000;
