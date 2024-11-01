# LITA-CUSTOMER-SUBSCRIPTION-DATASET


##VICTORIA SAMUEL_ DATA ANALYST PORTFOLIO 

This is a repository to showcase skills, share projects and track my progress in Data Analytics / Data Science related topics.

# LITA-DATA-ANALYSIS-DOCUMENTATION

[Goal](#goal)
[Description](#Description)
[Data Sources](#Data-Sources)
[Technology Used](#Technology-Used)
[Tools Used](#Tools-Used)
[Skills](#Skills)
[Data Cleaning and Preparations](#Data-Cleaning-and-Preparations)
[Exploratoratory Data Analysis](#Exploratoratory-Data-Analysis)
[Data Analysis](#Data-Analysis)
[Data Visualization](#Data-Visualization)

### Goal
---
To examine the profits for each country and also profit for each geopolitical zone
To know the country with the highest profits and the subscription that sold more.


### Description
---
The dataset contains records of brands sold, countries and plant_cost, cost, region, months, year, profit and unit_cost records by country between 2017-2019. This project includes the following steps: data loading, data cleaning and preprocessing and EDA (exploratory data analysis).

### Data Sources
---
The primary source data used here is a CSV data file to and this an open source data from sites such as KAGGLEor FRED or any other repository site.

### Technology Used
---
SQL Server

### Tools Used
---
- Microsoft Excel [Download here](https://www.microsoft.com)
     1. for Data cleaning
     2. visualization
- SQL- Structured Querry Language for data querrying
- Github- for portfolio Building

### Skills 
  -data analysis 
  -data visualization, 


### Skills 
---
  select 
  *
  FROM
    

### Data Cleaning and Preparations
---
The initail phase of data cleaning and preparations,we perform the following action;
1.Dta loading and inspection
2. Handling missing variables
3. Data cleaningand formatting

### Exploratoratory Data Analysis
---
EDA involved the exploring of the Data to answer some questions about the Data such as:
 - What is the overall sales trend
 - Which product are top sellers
 - What are the products on peak sales

### Exploratoratory Data Analysis
---h
EDA involved the exploring of the Data to answer some questions about the Data such as:
 - What is the overall sales trend
 - What was the subscription on peak sales

### Data Analysis
---

![Screenshot 2024-11-01 064032](https://github.com/user-attachments/assets/a0d5d6cc-a706-469e-974e-25fe77621790)

![Screenshot 2024-11-01 064134](https://github.com/user-attachments/assets/cd1881a5-6db7-4a1b-a658-a3ccdb2e2acb)

```
select region, COUNT(*) AS Numberofsales
from [LITA Capstone CustomerData_Subscription]
Group by Region
Order by Region

```
SELECT subscriptionType,
Sum(Revenue) AS totalsales
from [LITA Capstone CustomerData_Subscription]
Group by subscriptionType

```
Select COUNT(CUSTOMERID) AS Customerperregion, Region 
FROM [LITA Capstone CustomerData_Subscription]
Group by Region
Having COUNT(CustomerID) >=5

```
SELECT TOP 1 subscriptiontype, COUNT(*) AS total_customers
FROM [LITA Capstone CustomerData_Subscription]
GROUP BY subscriptiontype
ORDER BY total_customers DESC

```
SELECT
customerid
FROM [LITA Capstone CustomerData_Subscription]
WHERE DATEDIFF(DAY, subscriptionStart, subscriptionEnd) >= 365;

```
SELECT Canceled, COUNT(*) AS subscription_count
FROM [LITA Capstone CustomerData_Subscription]
WHERE Canceled = '1' 
GROUP BY Canceled
ORDER BY 1 DESC;

```
SELECT Canceled, COUNT(*) AS subscription_count
FROM [LITA Capstone CustomerData_Subscription]
WHERE Canceled = '0' 
GROUP BY Canceled
ORDER BY 1 DESC;

```
SELECT 
    COUNT(*) AS total_active
FROM 
    [LITA Capstone CustomerData_Subscription]
WHERE 
    Canceled = '1';

```
SELECT 
    COUNT(*) AS total_active
FROM 
    [LITA Capstone CustomerData_Subscription]
WHERE 
    Canceled = '0';

```
