SQL Portfolio Project: HR Management Report

------------------------------------------

Table of contents:
1. Overview
2. Dataset
3. Root Cause Analysis Process
4. Links
5. Built with
6. Key Insights
7. Major SQL statements functions , managing database objects and constraints used
8. Afterword

------------------------------------------

1. Overview

This project revolves around Workforce Overview Analysis in a mid-sized company. To analyze the data advanced SQL formulas (MySQL) were used, together with Google Dashboard for visualizations as well as a written report with the insights from analysis and recommendations for the future. 

------------------------------------------

2. Dataset

As the source data a sample open-source database from SQL Tutorial https://www.sqltutorial.org/ was used. This database was created for the sake of SQL open tutorial, yet it was chosen to be used for personal purpouses, from the scratch, taking initial structure of tables and their entries.
Only few employees' entry personal data were slightly modified in the Analysis compared to the original data, as it did not include any people employed in last 20 years. To make it more up to date few "junior positions" with respective salary and hire date were added.

This data set contains an SQL database called HR_project, which consist of 7 tables dedicated to HR data:
- The regions table: stores the data of regions such as Asia, Europe, America, and the Middle East and Africa. The countries are grouped into regions.
- The countries table: stores the data of countries where the company is doing business.
- The locations table: stores the location of the departments of the company.
- The departments table: stores department data.
- The employees table: stores the personal data of employees.
- The jobs table: stores the job data including job title and salary range.
- The dependents table: stores the employee’s dependents.

Relations between tables presents a image called "HR Department" to be found in the folder "Images".

To put it into worlds, table "employees" is linked to the tables:
- "jobs" via job_id,
- "departments" via department_id,
- "dependents" via dependent_id.
Table "departments" is linked to the table "locations" via location_id.
Table "locations" is linked to the table "countries" via country_id.
Table "countries" is linked to the table "regions" via region_id.

Key column variables in the dataset include:
- table "employees":
  - employe_id - unique employee identification number in the company
  - first_name
  - last_name
  - email
  - phone_number
  - hire_date
  - job_id
  - salary
  - manager_id
  - department_id
- table "jobs":
  - job_id - unique job title identification number in the company
  - job_title
  - min_salary - also called "salary floor" as it indicates lowest possible salary range per job title
  - max_salary - also called "salary ceiling" as it indicates highest possible salary range per job title
- table "dependents":
  - dependent_id - unique dependent identification number in the company
  - first_name
  - last_name
  - relationship
  - employee_id
- table "departments":
  - department_id - unique department identification number in the company
  - department_name
  - location_id
- table "locations":
  - location_id - unique location identification number in the company
  - street_address
  - postal_code
  - city
  - state_province
  - country_id
- table "countries":
  - country_id - unique country identification number in the company
  - country_name
  - region_id
- table "regions":
  - region_id - unique region identification number in the company
  - region_name

------------------------------------------

3. Root Cause Analysis Process

- The Analysis is aimed to play an important role in the regular HR data evaluation and is presented from the perspective of an HR Management Report.
- The Analysis serves the purpouse of answering the following questions:
  - What is the distribiution of employees and employees salaries per region, country, city, department, job role?
  - How many job roles are there in the company and what are salaries linked to them?
  - Which 10 employees have maximum and minimum salaries?
  - Which employees are best paid in their departments and what is their job role?
  - Who are the employees who are paid higher salary than an average salary per region?
  - Is the seniority (length of being hired) in the company correlated with higher salary average?
  - Is the data complete (no empty cells) and errorproof?
  - Family dependants and what is their relationship with company employees? 

------------------------------------------

4. Links

- Solution URLs:
  -   Project Report: Project Portfolio HR management Report (PDF file)
  -   Google Sheet Dashboard: https://docs.google.com/spreadsheets/d/e/2PACX-1vSX3_0VDhDbhb6szUIVFTQUO-or4aXIz209_9NnPMALn50NcB26Twhe_6dlwy8_kv7wkXezLUnbCJrK/pubhtml?gid=1622005887&single=true 

------------------------------------------

5. Built with:

- MySQL: HR Department Advanced SQL Portfolio Project (SQL Text file)
- Google Sheets: Google Sheets HR Management Report (Dashboard) (Adobe Acrobat Document)
- MS Word: Project Portfolio HR Management Report (Adobe Acrobat Document)
- MS Word: HR Management Report Metatable (Google Sheet insert file) (Csv file)
- Images (Jpg file)
------------------------------------------

6. Key Insights:

- The company operates in two regions, namely Europe and North America, and employs 40 people in total.
- The vast majority of workforce comes from America (32), with as many as 18 people located in Seattle, USA. Other cities include South San Francisco (7) and Southlake (5) in the USA and Toronto (2) in Canada.
- In Europe the company has branches in United Kingdom and Germany. UK employs 7 people in total (Oxford 6 , London 1) and in Germany there is 1 employee operating from Munich.
- As for the departments, most of them are located in the USA: Accounting, Administration, Executive, Finance, Purchasing, Shipping and IT. Marketing department operates from Canada, Public Relations from Germany, while Sales and HR may be found in the United
- The departments with highest number of staff include: Purchasing (6), Finance (6), Shipping (7) and Sales (6).
- There is a total of 19 job roles in the company.
- Listing of the job roles and workforce numbers: Programmer, Accountant, Purchasing Clerk (5 people each), Stock Manager, Sales Representative (4 people each), Sales Manager, Shipping Clerk, Administration Vice President (2 people each). Rest of titles include one person per job role in the company : Company President, Marketing Manager, Accounting Manager, Finance Manager, Purchasing Manager, Stock Clerk, Administration Assistant, Marketing Representative, HR Representative, Public Relations Representative, Public Accountant.
- The total monthly company payroll equals to 316.400.
- 5 company departments with the highest payroll are respectively: Executive (58.000), Sales (57.700), Finance (51.600), Shipping (38.200) and IT (28.800).
- The rest of the departments payroll presents as follows: Purchasing (24.900), Accounting (20.300), Marketing (16.000), PR (10.000), HR (6.500), Administration (4.400).
- Considering average salaries, the highest salary in the company may be earned in the Executive department (AVG 19.333), Accounting department (AVG 10.150), PR (AVG 10.000), Sales (AVG 9.617), Finance (AVG 8.600).
- Again considering average salaries, the lowest salaries should be earned in the Purchasing department (AVG 4.150), Administration ( AVG 4.400), Shipping ( AVG 5.457), IT ( AVG 5.760).
- Looking at salaries from the perspective of regional split, average salaries in Europe exceeded those in America (9.275 vs 7.569).
- At the same time, in America there were 15 people which salaries turned out to be higher than an average salary for the region, while in Europe there were just 3 persons which salaries turned out to be higher than an an average salary for the region.average salary for the region. This indicates that the salary This indicates that the salary range is wider in America, than it is in Europe.range is wider in America, than it is in Europe.
- 5 best paid jobs in the company were managing jobs and included: Company President (24.000), Administration Vice President (17.000), Sales Manager (14.000), Marketing Manager (13.000), Finance Manager (12.000), Accounting Manager (12.000).
- 5 lowest paid jobs in the company included: Purchasing Clerk (2.500), Stock Clerk (2.700), Marketing Representative (3.000), Shipping Clerk (3.900), Programmer (4.200).
- After conducting a check of employee actual salaries vs salaries range according to the company guidelines it was noted that no salary exceeded the maximum salary range given per job role. However, there were  two situations in which the actual salary of an employee was lower than the minimum salary range given per their job role. These two cases should be further analysed as for the reasons behind them as well as whether adjustments in the salaries of the employees should be made. The positions involved inc luded Marketing Representative and Stock Manager.
- Comparing an average salar ies in terms of seniority of employment, it was noted that the employees who have worked longer in the company tended to earn more than those with shorter seniority. Average salary  for senior worker in the company equalled to 8.877, while it was 5.529 for mid position and 3.800 per junior position. That should give a healthy attitude to seniority of employment, given the assumption that  employees who work in the company longer have more relevant work experience and capability.
- In terms of workforce demography, it would be recommended that more junior employees were recruited. Currently in the company there are 30 seniors, 7 mids and only 3 juniors.

------------------------------------------
7. Major SQL statements functions , managing database objects and constraints used
• SQL CREATE DATABASE
• SQL CREATE TABLE
• SQL INSERT INTO
• SQL ALTER TABLE
• SQL SELECT
• SQL DISTINCT
• SQL LIMIT
• SQL COMPARISON OPERATORS
• SQL LOGICAL OPERATORS
• SQL Alias
• SQL JOIN
• SQL LEFT JOIN
• SQL GROUP BY
• SQL ORDER BY
• SQL WHERE
• SQL HAVING
• SQL CREATE VIEW
• SQL AGGREGATE FUNCTIONS
• SQL CASE
• SQL IS NULL
• SQL GROUP_CONCAT
• SQL WINDOW FUNCTIONS
• SQL RANK()
• SQL PARTITION BY
• SQL DATEDIFF()
• SQL CURDATE()
• SQL SUBQUERY
• SQL CORRELATED SUBQUERY


------------------------------------------
   
8. Afterword
- This Portfolio Project aims to prove my analytical, SQL and Google Sheets skills and I hope it to be useful for my future employers to assess my knowledge and qualifications as top! Hope to see you during a direct interview. Kind greetings. ;) 
   









