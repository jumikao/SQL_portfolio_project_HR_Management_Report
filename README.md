SQL Portfolio Project: HR Management Report

Table of contents:
1. Overview
2. Dataset
3. Root Cause Analysis Process
4. Links
5. Built with
6. Key Insights

------------------------------------------

1. Overview
This project revolves around Workforce Overview Analysis in a mid-sized company. To analyze the data advanced SQL formulas (MySQL) were used, together with Google Dashboard for visualizations as well as a written report with the insights from analysis and recommendations for the future. 


2. Dataset
As the source data a sample open-source database from SQL Tutorial https://www.sqltutorial.org/sql-correlated-subquery/ was used (tables and tables' entries). This database was created for the sake of SQL open tutorial, yet it was chosen to use it for personal purpouses from the scratch.
Only few employees' entry personal data were slightly modified in the Analysis compared to the original data, as it did not include any people employed in last 20 years. To make it more up to date few "junior positions" with respective salary and hire date were added.

This data set contains an SQL database called HR_project, which consist of 7 tables dedicated to HR data:
-- The regions table: stores the data of regions such as Asia, Europe, America, and the Middle East and Africa. The countries are grouped into regions.
-- The countries table: stores the data of countries where the company is doing business.
-- The locations table: stores the location of the departments of the company.
-- The departments table: stores department data.
-- The employees table: stores the personal data of employees.
-- The jobs table: stores the job data including job title and salary range.
-- The dependents table: stores the employee’s dependents.

Relations between tables presents a image called "HR Department" to be found in the folder "Images".

To put it into worlds, table "employees" is linked to the tables:
- "jobs" via job_id,
- "departments" via department_id,
- "dependents" via dependent_id.
Table "departments" is linked to the table "locations" via location_id.
Table "locations" is linked to the table "countries" via country_id.
Table "countries" is linked to the table "regions" via region_id.

Key column variables in the dataset include:
-table "employees":
  -- employe_id - unique employee identification number in the company
  --first_name
  --last_name
  --email
  --phone_number
  --hire_date 
  --job_id
  --salary
  --manager_id
  --department_id
-table "jobs":
  --job_id - unique job title identification number in the company
  --job_title 
  --min_salary - also called "salary floor" as it indicates lowest possible salary range per job title
  --max_salary - also called "salary ceiling" as it indicates highest possible salary range per job title
-table "dependents":
  --dependent_id - unique dependent identification number in the company
  --first_name
  --last_name
  --relationship
  --employee_id
-table "departments":
  --department_id - unique department identification number in the company
  --department_name
  --location_id
-table "locations":
  --location_id - unique location identification number in the company
  --street_address
  --postal_code
  --city
  --state_province
  --country_id
-table "countries":
  --country_id - unique country identification number in the company
  --country_name
  --region_id
-table "regions":
  --region_id - unique region identification number in the company
  --region_name


3. Root Cause Analysis Process
The Analysis is aimed to play an important role in the regular HR data evaluation and is presented from the perspective of an HR Management Report.
The Analysis serves the purpouse of answering the following questions:
- What is the distribiution of employees and employees salaries per region, country, city, department, job role?
- How many job roles are there in the company and what are salaries linked to them?
- Which 10 employees have maximum and minimum salaries?
- Which employees are best paid in their departments and what is their job role?
- Who are the employees who are paid higher salary than an average salary per region?
- Is the seniority (length of being hired) in the company correlated with higher salary average?
- Is the data complete (no empty cells) and errorproof?
- Family dependants and what is their relationship with company employees? 



5. Links
Solution URLs:
Project Report:
Google Sheet Dashboard:

6. Built with:
-MySQL
-Google Sheets
-Pivot tables, SQL Aggregations

8. Key Insights:









