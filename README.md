![image](https://github.com/prashantjagtap2909/MySQL/assets/93985255/7047bace-2481-425b-8618-4975b22fdfdd)



1. What are the names of all employees?    
   - SELECT Name FROM emp_data;
     
2. How many employees are there in total? 
   - SELECT COUNT(*) AS total_employees FROM emp_data;
  
3. What departments do the employees work in?
   -  SELECT DISTINCT Department FROM emp_data;
      
4. How many employees work in each department?
    - SELECT Department, COUNT(*) AS total_employee_per_department FROM emp_data
GROUP BY Department;

5. Who is the highest-paid employee? 
    - SELECT Name, Salary FROM emp_data
ORDER BY Salary DESC
LIMIT 1;

6. Who is the lowest-paid employee? 
    - SELECT Name, Salary FROM emp_data
ORDER BY Salary ASC
LIMIT 1;

7. How many employees earn more than RS 20000 per year? 
   - SELECT COUNT(*) AS total_employee_more_than_20k FROM emp_data
WHERE Salary > 20000;

8. What is the average salary of all employees? 
   - SELECT AVG(Salary) AS average_salary FROM emp_data;
    
9. Who are the top 5 highest-paid employees?
   -  SELECT Name, Salary FROM emp_data
ORDER BY Salary DESC
LIMIT 5;

10. Who are the employees in the Marketing department? 
11. How many employees have a salary between RS 15000 and RS 25000? 
    - SELECT COUNT(*) AS total_employee_between_15k_25k FROM emp_data
WHERE Salary BETWEEN 15000 AND 25000;

12. Who are the employees with a salary of NULL? 
    - SELECT * FROM emp_data
WHERE Salary IS NULL;

13. Who are the employees with a first name starting with "J"? 
14. What are the salaries of all employees sorted in descending order?
    -  SELECT Name, Salary FROM emp_data
ORDER BY Salary DESC;

15. What is the total salary expenditure of the company? 
    - SELECT SUM(Salary) AS total_salary_expenditure FROM emp_data;
     
16. Who are the employees with the same first names?
17. How many employees are there in Pune location?
    -  SELECT COUNT(*) AS total_employee_pune FROM emp_data
WHERE Location = 'Pune';

18. What is the average salary of employees in Dev department? 
    - SELECT AVG(Salary) AS average_salary_dev FROM emp_data
WHERE Department = 'Dev';

19. Who are the employees with salaries above the average? 
    - SELECT Name, Salary FROM emp_data
WHERE Salary > (SELECT AVG(Salary) FROM emp_data);

20. Who are the employees with the lowest salary in Test department?
    -  SELECT Name, Salary FROM emp_data
WHERE Department = 'Test'
ORDER BY Salary ASC
LIMIT 1;

21. How many employees were hired in 2023 year? 
22. Who are the employees hired in the year 2023? 
23. What is the total salary expenditure in Dev and Support department? 
    - SELECT SUM(Salary) AS total_salary_dev_support FROM emp_data
  WHERE Department IN ('Dev', 'Support');

24. Who are the employees with a salary greater than the average salary of 
Dev department?
    - SELECT Name, Salary FROM emp_data
  WHERE Department = 'Dev'
  AND Salary > (SELECT AVG(Salary) FROM emp_data WHERE Department = 'Dev');

25. What is the total salary expenditure in Pune location?   
    - SELECT SUM(Salary) AS total_salary_p

