# 🇵🇰 Pakistan E-Commerce Sales Analytics | SQL & Power BI

## 📌 Project Overview

This project is an end-to-end data analytics project focused on analyzing Pakistan's e-commerce sales data using **MySQL and Power BI**.

The project covers the complete analytics workflow, including data exploration, data quality checks, sales analysis, customer analysis, product analysis, advanced SQL queries, data modeling, DAX calculations, and interactive Power BI dashboards.

The main goal of this project is to transform raw e-commerce sales data into meaningful business insights and interactive dashboards that support data-driven decision-making.

---

## 🎯 Project Objectives

The main objectives of this project are:

* Analyze overall e-commerce sales performance
* Calculate key business KPIs
* Identify revenue trends over time
* Analyze product and category performance
* Identify top-performing products
* Analyze customer purchasing behavior
* Identify repeat and one-time customers
* Analyze payment methods and order status
* Measure discount impact on revenue
* Perform advanced SQL analysis using CTEs and Window Functions
* Build interactive Power BI dashboards
* Create DAX measures for business analysis

---

# 🛠️ Tools & Technologies

| Tool        | Purpose                                      |
| ----------- | -------------------------------------------- |
| MySQL       | Data Storage and SQL Analysis                |
| SQL         | Data Exploration and Business Analysis       |
| Power BI    | Data Visualization and Dashboard Development |
| Power Query | Data Cleaning and Transformation             |
| DAX         | KPI and Advanced Calculations                |
| GitHub      | Project Documentation and Version Control    |

---

# 📊 Dataset Information

The dataset contains Pakistan e-commerce sales transaction data.

Key columns include:

* Item ID
* Order ID
* Customer ID
* Order Status
* Order Date
* SKU
* Category
* Price
* Quantity
* Revenue
* Discount
* Payment Method
* Year
* Month
* Customer Since

The dataset was used to perform sales, customer, product, category, payment, discount, and business performance analysis.

---

# 🔍 SQL Analysis

The SQL analysis was performed using MySQL.

## 1. Data Exploration

The following analysis was performed:

* Total rows
* Unique items
* Unique orders
* Unique customers
* Unique SKUs
* Unique categories
* Payment methods
* Order status distribution
* Date range analysis

---

## 2. Data Quality Checks

The dataset was analyzed for:

* Null values
* Blank values
* Duplicate records
* Negative prices
* Invalid quantities
* Negative revenue
* Negative discounts
* Date inconsistencies

---

## 3. Sales Performance Analysis

Key sales KPIs calculated:

* Total Revenue
* Total Orders
* Total Units Sold
* Average Order Value
* Average Price
* Total Discount
* Average Discount

---

## 4. Time-Based Analysis

Sales performance was analyzed by:

* Year
* Month
* Monthly Revenue
* Monthly Orders
* Monthly Units Sold
* Monthly Average Order Value

Advanced time analysis included:

* Previous Month Revenue
* Month-over-Month Growth
* Running Revenue
* Revenue Contribution Percentage
* Highest Revenue Month
* Lowest Revenue Month

---

## 5. Product Analysis

Product performance analysis included:

* Top Products by Revenue
* Top Products by Units Sold
* SKU Revenue Analysis
* SKU Ranking
* Top Products within Each Category
* Product Revenue Contribution
* Products Performing Above Average Revenue

---

## 6. Category Analysis

Category analysis included:

* Revenue by Category
* Units Sold by Category
* Category Revenue Contribution
* Category Ranking
* Top Categories
* Cumulative Category Revenue

---

## 7. Customer Analysis

Customer behavior analysis included:

* Total Customers
* Customer Lifetime Value
* Customer Spending Analysis
* Top Customers by Revenue
* Average Customer Spending
* Repeat Customers
* One-Time Customers
* Customer Segmentation

Customers were segmented into:

* High Value Customers
* Medium Value Customers
* Low Value Customers

---

## 8. Payment & Order Analysis

Business analysis included:

* Orders by Payment Method
* Revenue by Payment Method
* Average Order Value by Payment Method
* Orders by Status
* Revenue by Order Status

---

## 9. Discount Analysis

Discount analysis included:

* Discount Applied vs No Discount
* Orders with Discounts
* Revenue Generated with Discounts
* Total Discount Amount

---

# ⚡ Advanced SQL Techniques Used

This project demonstrates the use of advanced SQL concepts including:

* Common Table Expressions (CTEs)
* Subqueries
* Window Functions
* LAG()
* RANK()
* DENSE_RANK()
* PARTITION BY
* Running Totals
* CASE Statements
* Aggregate Functions
* DISTINCTCOUNT Logic
* NULLIF()
* Data Validation Queries

---

# 📊 Power BI Dashboard

The Power BI dashboard was built by connecting MySQL data to Power BI.

The complete workflow:

MySQL Database
↓
Power BI Connection
↓
Power Query Transformation
↓
Data Modeling
↓
Date Table
↓
Relationships
↓
DAX Measures
↓
Interactive Dashboards

---

# 📈 Dashboard Pages

## 1. Executive Overview

This dashboard provides a high-level view of overall business performance.

### KPIs

* Total Revenue
* Total Orders
* Total Customers
* Total Units Sold
* Average Order Value
* Total Discount

### Visualizations

* Monthly Revenue Trend
* Revenue by Category
* Revenue by Payment Method
* Revenue by Order Status

### Filters

* Year
* Month
* Category
* Payment Method

---

## 2. Product & Category Analysis

This dashboard focuses on product and category performance.

### KPIs

* Total Revenue
* Total Units Sold
* Total Products
* Average Price

### Visualizations

* Top 10 Products by Revenue
* Revenue by Category
* Units Sold by Category
* Category Revenue Contribution
* Category Performance Table

### Filters

* Year
* Category
* Payment Method

---

## 3. Customer & Business Analysis

This dashboard focuses on customer behavior and business performance.

### KPIs

* Total Customers
* Repeat Customers
* One-Time Customers
* Total Revenue

### Visualizations

* Customer Segmentation
* Top 10 Customers by Revenue
* Revenue by Payment Method
* Discount Impact on Revenue
* Orders by Status

### Filters

* Year
* Customer Segment
* Payment Method

---

# 📐 Data Modeling

A Date Table was created to support time intelligence analysis.

Relationship:

Date Table (1) → Sales (*)

The Date Table includes:

* Date
* Year
* Month Number
* Month Name
* Quarter

The Month Name column was sorted using Month Number.

---

# 🧮 Key DAX Measures

Some important DAX measures created:

### Total Revenue

```DAX
Total Revenue =
SUM(Sales[Revenue])
```

### Total Orders

```DAX
Total Orders =
DISTINCTCOUNT(Sales[Order ID])
```

### Total Customers

```DAX
Total Customers =
DISTINCTCOUNT(Sales[Customer ID])
```

### Total Units Sold

```DAX
Total Units Sold =
SUM(Sales[Quantity])
```

### Average Order Value

```DAX
Average Order Value =
DIVIDE(
    [Total Revenue],
    [Total Orders],
    0
)
```

### Repeat Customers

```DAX
Repeat Customers =
COUNTROWS(
    FILTER(
        VALUES(Sales[Customer ID]),
        CALCULATE(
            DISTINCTCOUNT(Sales[Order ID])
        ) > 1
    )
)
```

### One-Time Customers

```DAX
One-Time Customers =
COUNTROWS(
    FILTER(
        VALUES(Sales[Customer ID]),
        CALCULATE(
            DISTINCTCOUNT(Sales[Order ID])
        ) = 1
    )
)
```

---

# 💡 Key Business Questions Answered

This project helps answer important business questions such as:

1. What is the total revenue generated?
2. How many orders were placed?
3. How many unique customers made purchases?
4. Which category generates the highest revenue?
5. Which products generate the most revenue?
6. Which month generated the highest revenue?
7. What is the monthly revenue trend?
8. Which payment method generates the highest revenue?
9. How many customers are repeat customers?
10. How many customers are one-time customers?
11. Which customers generate the highest revenue?
12. How do discounts impact revenue?
13. Which order statuses generate the most revenue?
14. What is the Average Order Value?
15. What is the Month-over-Month revenue growth?

---

# 📁 Project Structure

```text
Pakistan-Ecommerce-Sales-Analytics/
│
├── Data/
│   └── pakistan_ecommerce_sales.csv
│
├── SQL/
│   └── Pakistan_Ecommerce_SQL_Analysis.sql
│
├── Power BI/
│   └── Pakistan_Ecommerce_Sales_Analytics.pbix
│
├── Dashboard/
│   ├── Executive_Overview.png
│   ├── Product_Category_Analysis.png
│   └── Customer_Business_Analysis.png
│
└── README.md
```

---

# 📸 Dashboard Preview

## Executive Overview

Add screenshot here:

```text
Dashboard/Executive_Overview.png
```

---

## Product & Category Analysis

Add screenshot here:

```text
Dashboard/Product_Category_Analysis.png
```

---

## Customer & Business Analysis

Add screenshot here:

```text
Dashboard/Customer_Business_Analysis.png
```

---

# 📚 Skills Demonstrated

### SQL

* Data Exploration
* Data Cleaning
* Data Validation
* Aggregations
* GROUP BY
* HAVING
* Subqueries
* CTEs
* Window Functions
* LAG()
* RANK()
* DENSE_RANK()
* CASE Statements

### Power BI

* MySQL Connection
* Power Query
* Data Transformation
* Data Modeling
* Relationships
* Date Tables
* DAX
* KPI Cards
* Interactive Dashboards
* Slicers
* Business Insights

---

# 🚀 Project Outcome

This project demonstrates the complete end-to-end data analytics workflow from SQL data analysis to interactive business intelligence reporting.

The project combines advanced SQL techniques with Power BI data modeling and DAX calculations to transform raw e-commerce transaction data into meaningful insights and interactive dashboards.

---

# 👨‍💻 Author

**Malik Muhammad Ali Aslam**

Aspiring Data Analyst | SQL | Power BI | Python | Excel
GitHub: malikALIaslam
LinkedIn: Muhammad Ali
