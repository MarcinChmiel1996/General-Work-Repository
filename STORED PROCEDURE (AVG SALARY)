USE employees

DELIMITER $$

CREATE PROCEDURE gimme_salary ()

BEGIN

SELECT e.emp_no, e.first_name, e.last_name, AVG(s.salary) AS paid
FROM employees e
INNER JOIN salaries s ON s.emp_no= e.emp_no
GROUP BY e.emp_no
ORDER BY s.salary;
END $$

DELIMITER ;

CALL gimme_salary();
