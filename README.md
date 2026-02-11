# SQL Security Filtering Case Study

## Overview
This repository demonstrates the use of SQL filtering techniques to investigate security-related events within an organizational database. The project focuses on analyzing login activity and employee machine assignments using structured queries and logical operators.

## Scenario
As a security analyst, I investigated suspicious login attempts and retrieved department-specific employee data to support incident response and system updates. The analysis was performed on the `log_in_attempts` and `employees` tables using MariaDB (MySQL-compatible).

## Skills Demonstrated
- SQL data retrieval using `SELECT`
- Filtering with `WHERE`
- Logical operators: `AND`, `OR`, `NOT`
- Pattern matching using `LIKE` and `%`
- Date and time filtering
- Investigating anomalous login activity
- Querying department-based device information

## Key Security Tasks Performed
- Identified failed login attempts occurring after business hours
- Retrieved login activity for specific incident dates
- Filtered login attempts originating outside Mexico
- Queried employee data by department and building location
- Excluded specific departments from update targeting

## Tools Used
- MariaDB (MySQL-compatible)
- SQL command-line interface

## Project Files
- `apply-sql-filters-security.md` — Full case study with queries and explanations

## Disclaimer
This case study is based on a simulated organizational environment and is intended for educational and professional portfolio purposes.

