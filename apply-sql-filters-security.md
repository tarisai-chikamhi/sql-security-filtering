Apply filters to SQL queries
Project description
In this project, I used SQL filtering techniques to investigate potential security concerns within an organization’s database. I queried the log_in_attempts and employees tables to identify suspicious login activity and retrieve employee machine information. By applying logical operators such as AND, OR, NOT, and LIKE, I narrowed large datasets into security-relevant results to support incident investigation and system updates.
Retrieve after hours failed login attempts
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00:00'
AND success = 0;
Explanation
This query retrieves failed login attempts that occurred after 18:00 (6:00 PM).
•	login_time > '18:00:00' filters login attempts that happened after business hours.
•	success = 0 identifies failed login attempts.
•	AND ensures both conditions must be satisfied.
This query helps identify potentially suspicious activity occurring outside normal working hours.
Retrieve login attempts on specific dates
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-08'
OR login_date = '2022-05-09';
Explanation
This query retrieves login attempts from two specific dates surrounding a suspicious event.
•	login_date filters records by date.
•	OR allows results from either May 8 or May 9.
This method narrows the dataset to a targeted investigation window.

Retrieve login attempts outside of Mexico
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';
Explanation
The country column includes both MEX and MEXICO, so pattern matching is required.
•	LIKE 'MEX%' matches any country value beginning with “MEX”.
•	% acts as a wildcard for any characters following “MEX”.
•	NOT excludes those records.
This query retrieves login attempts originating outside Mexico.
Retrieve employees in Marketing
SELECT *
FROM employees
WHERE department = 'Marketing'
AND office LIKE 'East-%'; 
Explanation
This query retrieves Marketing employees located in the East building.
•	department = 'Marketing' filters by department.
•	office LIKE 'East-%' matches all East building offices.
•	AND ensures both conditions are met.
The % wildcard captures any office number in the East building.
Retrieve employees in Finance or Sales
SELECT *
FROM employees
WHERE department = 'Finance'
OR department = 'Sales';

Explanation
This query retrieves employees in either the Finance or Sales departments.
•	OR allows records that meet either department condition.
This ensures all relevant employees receive the required security update.
Retrieve all employees not in IT
SELECT *
FROM employees
WHERE NOT department = 'Information Technology';
Explanation
This query retrieves all employees outside the IT department.
•	NOT excludes the Information Technology department.
•	This allows updates to be targeted only to departments that require them.
Summary
In this project, I applied SQL filtering techniques to investigate login activity and retrieve department-specific employee information. I used logical operators such as AND, OR, and NOT, along with pattern matching using LIKE and wildcards, to efficiently narrow database records. These queries demonstrate practical experience using SQL to support security investigations and operational decision-making.

SQL filtering case study
