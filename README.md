📊 Executive Sales Performance Dashboard
🔹 Project Overview

This project focuses on building an end-to-end Business Intelligence solution using Power BI. It includes data modeling, DAX calculations, time intelligence, and an executive-level dashboard to deliver actionable business insights.

The dashboard provides a comprehensive view of sales performance, helping stakeholders make data-driven decisions.

🎯 Objectives
Build a star schema data model
Create DAX measures for KPIs
Implement time intelligence calculations
Design an interactive executive dashboard
Generate business insights for decision-making

🗂️ Dataset Description

The dataset consists of three main tables:

🔸 Fact Table

Orders

Order ID

Order Date

Customer ID

Product ID

Sales

Profit

Quantity

🔸 Dimension Tables

**Customers**

Customer ID

Customer Name

Region

Segment

**Products**

Product ID

Category

Sub-Category

🔸 Calendar Table
Date
Year
Month
Month Number

🧩 Data Model
Implemented a Star Schema
Relationships:

Orders → Customers (Customer ID)

Orders → Products (Product ID)

Orders → Calendar (Order Date)

📐 DAX Measures
Total Sales = SUM(Orders[Sales])

Total Profit = SUM(Orders[Profit])

Profit Margin = DIVIDE([Total Profit], [Total Sales])

Total Orders = COUNT(Orders[Order ID])

Previous Month Sales = 
CALCULATE(
    [Total Sales],
    DATEADD(Calendar[Date], -1, MONTH)
)

Growth % = 
VAR Prev = [Previous Month Sales]
RETURN DIVIDE([Total Sales] - Prev, Prev)

Category Contribution % = 
DIVIDE(
    [Total Sales],
    CALCULATE([Total Sales], ALL(Products[Category]))
)

📊 Dashboard Features
🔹 KPIs

Total Sales: 2.30M

Total Profit: 286K

Profit Margin: 12.47%

Growth %: 3.8%

Total Orders: 9994


🔹 Visuals
📈 Sales Trend (Monthly)

📊 Profit by Category

📊 Sales by Region

🍩 Segment Distribution

📋 Top 10 Customers

🔹 Filters (Slicers)
Year

Month

Region

Category

Segment

📈 Key Insights
Sales show moderate growth (3.8%) with fluctuations
Peak performance observed in November (seasonality)
West region generates the highest revenue (~2.10M)
Technology category is the most profitable (~145K)
Consumer segment (~50.5%) drives the majority of sales

💡 Business Recommendations
Focus on high-performing regions (West & East)
Improve performance in South region
Invest more in Technology category
Optimize Furniture category (low profitability)
Leverage seasonal peaks (November)
Strengthen Consumer segment strategy

📦 Deliverables
Power BI File (.pbix)
Dashboard Screenshots
Data Model Screenshot
DAX Measures Document
Business Insight Report (PDF)

🚀 Tools & Technologies
Power BI
DAX (Data Analysis Expressions)
Excel (Data Source)

📌 Conclusion

This project demonstrates the complete workflow of a Business Intelligence Developer, from data modeling to executive storytelling. The dashboard enables stakeholders to quickly understand performance and take strategic actions.

🙌 Author

[Hrushikesh Khedkar]
