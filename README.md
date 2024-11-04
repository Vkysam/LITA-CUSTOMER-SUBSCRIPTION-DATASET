### PROJECT TITLE: LITA-CAPSTONE-CUSTOMER-SUBSCRIPTION-DATASET ANALYSIS PROJECT

### CONTENT

[Project Overview](#project-overview)
[Goal](#goal)
[Description](#description)
[Data Sources](#data-Sources)
[Technology Used](#technology-Used)
[Tools Used](#tools-Used)
[Skills](#skills)
[Data Cleaning and Preparations](#data-cleaning-and-preparations)
[Exploratoratory Data Analysis](#exploratoratory-data-analysis)
[Data Analysis and Data Visualization](#data-analysis-and-visualization)


### PROJECT OVERVIEW

This data Analysis project aims to give insights on the sales performance of the CAPSTONE SUBSCRIPTION DATASET
project for a period of two years. These analysis will help make informed decisions for a possible growth strategies.

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

### DATA ANALYSIS AND VISUALIZATION
---

![Screenshot 2024-11-01 064032](https://github.com/user-attachments/assets/a0d5d6cc-a706-469e-974e-25fe77621790)

![Screenshot 2024-11-01 064134](https://github.com/user-attachments/assets/cd1881a5-6db7-4a1b-a658-a3ccdb2e2acb)

```SQL
  select region, COUNT(*) AS Numberofsales
from [LITA Capstone CustomerData_Subscription]
Group by Region
Order by Region
```

```SQL
   SELECT subscriptionType,
Sum(Revenue) AS totalsales
from [LITA Capstone CustomerData_Subscription]
Group by subscriptionType
```

```SQL
   Select COUNT(CUSTOMERID) AS Customerperregion, Region 
FROM [LITA Capstone CustomerData_Subscription]
Group by Region
Having COUNT(CustomerID) >=5
```

```SQL
   SELECT TOP 1 subscriptiontype, COUNT(*) AS total_customers
FROM [LITA Capstone CustomerData_Subscription]
GROUP BY subscriptiontype
ORDER BY total_customers DESC
```

```SQL
SELECT
     customerid
     FROM [LITA Capstone CustomerData_Subscription]
     WHERE DATEDIFF(DAY, subscriptionStart, subscriptionEnd) >= 365;
```

```SQL
SELECT Canceled, COUNT(*) AS subscription_count
FROM [LITA Capstone CustomerData_Subscription]
WHERE Canceled = '1' 
GROUP BY Canceled
ORDER BY 1 DESC;
```

```SQL
SELECT Canceled, COUNT(*) AS subscription_count
FROM [LITA Capstone CustomerData_Subscription]
WHERE Canceled = '0' 
GROUP BY Canceled
ORDER BY 1 DESC;
```

```SQL
SELECT 
    COUNT(*) AS total_active
FROM 
    [LITA Capstone CustomerData_Subscription]
WHERE 
    Canceled = '1';
```

```SQL
SELECT 
    Canceled,
    COUNT(*) AS total
FROM 
    [LITA Capstone CustomerData_Subscription]
WHERE 
    canceled IN ('0', '1')
GROUP BY 
    canceled;
```

```SQL
SELECT 
    COUNT(*) AS total_active
FROM 
    [LITA Capstone CustomerData_Subscription]
WHERE 
    Canceled = '0';
```

![Screenshot 2024-11-04 102153](https://github.com/user-attachments/assets/805319a1-cfbd-4b84-b850-37d702d0c647)

💻

