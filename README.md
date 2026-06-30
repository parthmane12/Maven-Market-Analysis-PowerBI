# Maven Market Analysis | End-to-End Business Intelligence Dashboard using Power BI

> An end-to-end Business Intelligence project built with Power BI that transforms raw retail data into actionable business insights through interactive dashboards covering Sales, Orders, Returns, Customers, Stores, and Products.

---

# Home Page

<p align="center">
  <img src="images/Home_Page.png" width="100%">
</p>

The Home Page serves as the central navigation hub of the dashboard, providing users with an intuitive starting point for exploring different aspects of Maven Market's business performance. Custom navigation buttons allow seamless movement between report pages, creating an application-like user experience while maintaining a consistent visual theme throughout the report.

The dashboard consists of seven interactive pages:

- Home
- Sales Analysis
- Orders Overview
- Returns Analysis
- Customers Insights
- Stores Performance
- Product Analysis

---

# Executive Summary

Maven Market is a multinational grocery retail chain operating across the United States, Canada, and Mexico. The organization collects large volumes of transactional, customer, product, and store-level data, making it difficult to monitor business performance using raw spreadsheets alone.

The objective of this project was to transform this raw retail data into an interactive Business Intelligence solution capable of answering key business questions related to sales performance, customer behavior, product profitability, store efficiency, and product returns.

Using **Power BI Desktop**, the complete analytics workflow was developed, including data cleaning, transformation, modeling, DAX calculations, and dashboard design. Data from multiple sources was consolidated into a star schema model, enabling efficient analysis across multiple business dimensions.

The final dashboard consists of **seven interactive pages**, allowing business users to monitor KPIs, identify trends, evaluate performance, and make data-driven decisions through dynamic filtering and drill-down capabilities.

### Overall Dashboard Highlights

| KPI | Value |
|------|-------|
| Total Sales | **$1.76M** |
| Total Profit | **$1.05M** |
| Profit Margin | **59.67%** |
| Products Sold | **833K Units** |
| Products Returned | **8K Units** |
| Return Rate | **0.99%** |
| Customer Retention Rate | **85.99%** |
| Total Stores | **24** |

The dashboard enables stakeholders to:

- Monitor business performance in real time
- Identify top-performing products and regions
- Evaluate customer purchasing behavior
- Analyze product return patterns
- Compare store performance
- Optimize inventory decisions
- Support strategic business planning using data

---

# Business Problem

Retail organizations generate millions of transaction records across different locations, customers, and products. While this data contains valuable insights, it becomes increasingly difficult for decision-makers to extract meaningful information without an effective reporting system.

The Maven Market dataset contains information related to:

- Customer purchases
- Product catalog
- Sales transactions
- Product returns
- Store information
- Regional hierarchy

Without an integrated analytics platform, answering important business questions becomes time-consuming and inefficient.

Examples include:

- Which products generate the highest revenue?
- Which regions contribute most to profit?
- Which products experience the highest return rates?
- Which customer segments drive the majority of sales?
- Which stores require operational improvements?
- How has business performance changed over time?

This project addresses these challenges by providing an interactive Power BI dashboard that transforms raw operational data into meaningful business insights.

---

# Project Objectives

The primary objective of this project is to design an end-to-end Business Intelligence solution that enables stakeholders to monitor and analyze Maven Market's overall business performance.

The dashboard focuses on the following objectives:

### Sales Analysis

- Analyze sales trends across months and years
- Compare regional sales performance
- Identify top-selling products
- Evaluate customer segment contribution
- Measure profitability using key KPIs

### Orders Overview

- Analyze order volume trends
- Understand purchasing patterns
- Compare order size across products
- Evaluate order distribution by country

### Returns Analysis

- Measure return rate
- Identify frequently returned products
- Analyze return trends across regions and months
- Evaluate return performance by product brand

### Customer Insights

- Analyze customer demographics
- Measure customer retention and churn
- Identify high-value customers
- Compare purchasing behavior across member card types

### Stores Performance

- Compare store performance
- Evaluate profitability by store type
- Analyze sales across states and regions
- Study the relationship between store size and revenue

### Product Analysis

- Identify best-selling products
- Discover high-margin products
- Detect slow-moving inventory
- Compare product performance across regions

---

# Dataset Overview

The project uses the **Maven Market** retail dataset, which simulates the operations of a multinational grocery chain.

The dataset contains transactional and dimensional data covering customers, products, stores, returns, and regional information across multiple countries.

### Dataset Tables

| Table | Description |
|--------|-------------|
| Transactions 1997 | Sales transactions for 1997 |
| Transactions 1998 | Sales transactions for 1998 |
| Customers | Customer demographic information |
| Products | Product catalog and pricing |
| Stores | Store information and attributes |
| Regions | Geographic hierarchy |
| Returns | Returned products |
| Calendar | Date dimension created for time intelligence |

The project integrates these datasets into a unified data model to support interactive reporting and advanced business analysis.

---

# Tech Stack

The project was developed using the following technologies:

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Dashboard development and visualization |
| **Power Query Editor** | Data cleaning, transformation, and ETL |
| **DAX (Data Analysis Expressions)** | Calculated columns, measures, and KPIs |
| **Microsoft Excel** | Source dataset management |

---

# Data Preparation

Data preparation was performed using **Power Query Editor** before loading the data into the Power BI model.

The following preprocessing steps were carried out to ensure data quality and consistency:

- Appended transaction datasets from 1997 and 1998 into a unified transaction table.
- Merged queries to enrich transactional data with additional business information.
- Corrected and standardized data types across all tables.
- Handled blank and missing values where necessary.
- Created custom columns to support business analysis.
- Removed unnecessary fields to optimize the data model.
- Standardized date formats for consistent reporting.
- Built a dedicated Calendar table to enable time intelligence analysis.
- Verified data integrity after transformation.
- Prepared clean datasets for efficient modeling and reporting.

These preprocessing steps ensured that the dashboard was built on reliable, analysis-ready data.

---

# Data Modeling

> **Insert Data Model Screenshot Here**

```
images/Data_Model.png
```

A **Star Schema** data model was designed to improve report performance, simplify filtering, and support scalable analytics.

### Fact Tables

- Transactions
- Returns

### Dimension Tables

- Customers
- Products
- Stores
- Regions
- Calendar

The model uses one-to-many relationships between dimension tables and fact tables, enabling efficient cross-filtering throughout the dashboard.

The Calendar table was created specifically to support time intelligence calculations such as monthly and yearly sales trends.

This modeling approach improves query performance while keeping the dashboard organized, maintainable, and scalable.

---

# DAX Measures

Several custom DAX measures were created to calculate business KPIs and enhance analytical capabilities.

## Sales Metrics

- Total Sales
- Total Profit
- Profit Margin %

## Customer Metrics

- Customers (1997)
- Customers (1998)
- Retention Rate
- Churn Rate

## Returns Metrics

- Return Rate
- Total Products Returned
- Most Returned Product
- Most Returned Brand

## Store Metrics

- Total Stores
- Average Sales per Store
- Store Age

## Product Metrics

- Average Selling Price

These measures provide dynamic calculations that automatically respond to report filters and slicers, enabling flexible and interactive analysis across the dashboard.

---

# Repository Structure

```text
Maven-Market-Analysis/
│
├── Dashboard.pbix
├── Dashboard.pdf
├── README.md
│
├── dataset/
│   ├── Customers.csv
│   ├── Products.csv
│   ├── Stores.csv
│   ├── Regions.csv
│   ├── Returns.csv
│   └── Transactions.csv
│
└── images/
    ├── Home.png
    ├── Data_Model.png
    ├── Sales_Analysis.png
    ├── Orders_Overview.png
    ├── Returns_Analysis.png
    ├── Customers_Insights.png
    ├── Stores_Performance.png
    └── Product_Analysis.png
```

---

**Next:** Dashboard Walkthrough — Home Page, Sales Analysis, and Orders Overview.
