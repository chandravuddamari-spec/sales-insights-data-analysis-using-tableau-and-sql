<h1 align="center">Sales Insights - Data Analysis using Tableau and SQL</h1>

This repository contains a comprehensive Sales Insights Data Analysis project for an India-based hardware company, utilizing Tableau and SQL to drive data-driven decision making.

### About Project

- Performed India-based hardware company sales insights - A Data Analysis project.
- Developed ETL mappings using SQL to extract the data from unstructured sources and transformed it to the staging area to conduct data cleaning and design a star schema data model on Tableau.
- Developed a Tableau dashboard to perform analysis, producing quantitative visualizations in Tableau to draw valuable insights based on different parameters affecting company performance year on year and provide business solutions.

## Technologies Used

* Advanced Excel
* MySQL | SQL Server
* Tableau | Power BI
* Statistics

## Certifications

- Data Visualization with Tableau - by Simplilearn
- Databases and SQL for Data Science with Python - by IBM
- Statistics for Data Science with Python - by IBM
- Data Visualization with Advanced Excel - by PWC

## Project - India based Hardware company Sales Insights - Data Analysis performed on Tableau and SQL
  
### Problem Statements
The Sales Director needs to understand the performance of the company in various Indian states to optimize pricing and discount strategies.

- Q1. Revenue breakdown by cities.
- Q2. Revenue breakdown by years and months.
- Q3. Top 5 customers by revenue and sales quantity.
- Q4. Top 5 Products by revenue.
- Q5. Net Profit and Profit Margin by Market.

### Approach - Project Planning and Aims Grid
  
#### 1. Purpose: What? Why? What do we want to achieve?
To unlock sales insights that were not previously visible to the sales team for decision support and automate reporting to reduce manual time spent in data gathering.

#### 2. Stakeholders: Who will be involved?
- Sales Director
- I.T. Team
- Customer Service Team
- Data and Analytics Team

#### 3. End Result: What do we want to achieve?
An automated dashboard providing quick and latest sales insights in order to support data-driven decision making.

#### 4. Success Criteria: What will be our success criteria?
- Dashboards uncovering sales order insights with the latest data available.
- Sales team able to take better decisions and prove 10% cost savings of total spend.
- Sales analysts stop data gathering manually in order to save 20% of their business time and reinvest it in value-added activity.

### Data Analysis - Approach
The project follows a structured pipeline: Data Discovery -> Data Analysis via SQL -> Data Cleaning and ETL -> Data Visualization in Tableau.

### Setup Process
  
Step 1: Download the database files (db_dump.sql or db_dump.xlsx).
Step 2: Import the data into MySQL and perform ETL (Extract, Transform, Load) processes as required.
Step 3: Use Tableau Public or Tableau Desktop to perform Data Analysis.
Step 4: Connect Tableau with the MySQL database or Excel database.
Step 5: Save the analysis file as .twb or .twbx.

## Data Analysis Using SQL
  
1. Show all customer records
    `SELECT * FROM customers;`

2. Show total number of customers
    `SELECT count(*) FROM customers;`

3. Show transactions for Chennai market (market code for Chennai is Mark001)
    `SELECT * FROM transactions where market_code='Mark001';`

4. Show distinct product codes that were sold in Chennai.
    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

5. Show transactions where currency is US dollars.
    `SELECT * from transactions where currency="USD"`

6. Show transactions in 2020 joined by date table.
    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

7. Show total revenue in year 2020.
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
8. Show total revenue in year 2020, January Month.
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

9. Show total revenue in year 2020 in Chennai.
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";`

## Data Analysis Using Tableau 
  
The analysis includes a Star Schema data model to link dimensions and facts efficiently. The dashboards focus on two primary areas:

1. Revenue Analysis: Tracking income across different regions and time periods.
2. Profit Analysis: Evaluating market-specific margins and net profit trends.

## Project References

1. Tableau Project Dashboard: Sales Insights - Data Analysis using Tableau
2. MySQL Installation and Configuration guides
3. OLTP and OLAP architectural differences
4. Star Schema: Fact Table and Dimension Table documentation

## Related Projects

- Spotify Data Analysis using Python
- Statistics for Data Science using Python
- Python Lessons and Libraries for Data Science

## About the Developer

**Sai Chandra Vuddamari**
Research and Innovation Analyst

I am a detail-oriented analyst who builds structure out of critical thinking, analyzing data through Excel trackers, dashboards, and SQL/R. I work directly with stakeholders to close gaps and maintain accurate reporting in fast-paced, evolving environments. With over 4 years of professional experience, I focus on transforming raw data into actionable business intelligence.

**Contact Information:**
- Email: sssaichandra375@gmail.com
- Key Skills: SQL, Python, R, VBA, Tableau, Advanced Excel