# E-Commerce Performance Analysis


### Project Overview
---

An E-commerce company established in 2023, operates five stores strategically located across all regions of the country. This project aims to provide insights into the sales performance, customer behavior, and product trends in order to identify key revenue drivers and uncover potential issues affecting profitability. 

<img width="1484" height="708" alt="overview" src="https://github.com/user-attachments/assets/1d2b96bd-90bc-4445-bab5-7a3a86a637c1" />


### Data Sources

EliteMart Retail Sales Dataset: The primary dataset used for the analysis is the "EliteMart_retail_sales_dataset.csv" file, containing detailed information about the company's transactions.

### Tools

- PowerBI - Data cleaning, Data preparation, Data Analysis & Creating reports


### Data Cleaning/Preparation

In the initial data preparation phase, we performed the following tasks:
1. Data loading and Inspection.
2. Handling missing values.
3. Data cleaning and Formatting.

### Exploratory Data Analysis

EDA involved exploring the sales data to answer key questions, such as;

- Total number of sales?
- Total profit?
- Year over Year Company growth?
- Number of Customers?
- Avergae Customer Tenure?

## Data Analysis

DAX formula used to calculate year over year growth

```DAX
YOY sales growth = 
 VAR currentYearSales =
 CALCULATE(
    SUM(Transactions[Totalprice]),
    YEAR(Transactions[Date]) = 2025)
VAR OLDyearSales =
    CALCULATE(
        SUM(Transactions[Totalprice]),
        YEAR(Transactions[Date]) = 2024)
RETURN
    currentYearSales - OLDyearSales
```

DAX formula used to claculate Average store sales

```DAX
AVERAGE STORE SALES = 
DIVIDE(
    SUM(Transactions[Totalprice]),
    DISTINCTCOUNT(Stores[StoreID]
))
```

### Results/Findings

The analysis results are summarised as follows:
1. Customers aged 51-71 account for 43% of total sales.
2. 2024 was an exceptionally peak year and not the baseline for comparison, 2025 represents normalization rather then a true decline.
3. fewer customers came in 2025, but customers that came spent more.
4. EliteMart New Micelle was the top performing store.
5. Electronics is the best performing category in terms of sales.

### Recommendations

Based on the analysis, we recommend the following actions;
- Invest in marketing and promotions to get closer to the sales of the exceptional peak year.
- Focus on expanding and promoting products in the accessories and smartphone sub-category.
- Implement a customer segmentation strategy to target high-LTV customers effectively.






