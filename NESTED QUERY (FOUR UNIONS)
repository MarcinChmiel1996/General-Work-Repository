/* Query that inserts into employee manager table 41 rows
 showing employees with various ID's, assigned to two managers
 + two queries C and D that assign both employee to manager 
 and manager to employee with numbers switched.
 
 The whole syntax uses various SQL comands such as:
 Nested queries, JOIN, UNION, AGGREGATE FUNCTIONS, WHERE clause, ALIASES.*/

INSERT INTO emp_manager SELECT U.* 
FROM
(SELECT A.* 
FROM

(SELECT e.emp_no AS ID, 
MIN(dp.dept_no) AS department,
 (SELECT
emp_no
 FROM
 dept_manager dp
WHERE emp_no = 110022) AS managerro

FROM employees e
JOIN dept_emp dp ON e.emp_no = dp.emp_no
WHERE e.emp_no <=10020
GROUP BY e.emp_no
ORDER BY e.emp_no)
AS A 

UNION

SELECT B.* 
FROM

(SELECT e.emp_no AS ID, 
MIN(dp.dept_no) AS department,
 (SELECT
emp_no
 FROM
 dept_manager dp
WHERE emp_no = 110039) AS managerro

FROM employees e
JOIN dept_emp dp ON e.emp_no = dp.emp_no
WHERE e.emp_no <10020
GROUP BY e.emp_no
ORDER BY e.emp_no)
AS B 

UNION

SELECT C.* FROM
(SELECT e.emp_no AS ID, 
MIN(dp.dept_no) AS department,
 (SELECT
emp_no
 FROM
 dept_manager dp
WHERE emp_no = 110039) AS managerro
FROM employees e
JOIN dept_emp dp ON e.emp_no = dp.emp_no
WHERE e.emp_no = 110022
GROUP BY e.emp_no
ORDER BY e.emp_no)
AS C 

UNION
SELECT D.* FROM
(SELECT e.emp_no AS ID, 
MIN(dp.dept_no) AS department,
 (SELECT
emp_no
 FROM
 dept_manager dp
WHERE emp_no = 110022) AS managerro
FROM employees e
JOIN dept_emp dp ON e.emp_no = dp.emp_no
WHERE e.emp_no = 110039
GROUP BY e.emp_no
ORDER BY e.emp_no)
AS D) 

AS U;







