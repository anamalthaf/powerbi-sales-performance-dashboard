# 📊 Power BI Sales Performance Dashboard (UAE)

This project presents an interactive Power BI dashboard designed to analyze sales performance across revenue, order volume, average order value, and month-over-month growth.  
The dashboard supports data-driven business decision-making across products and regions.

## 🔍 Dashboard Preview
![Sales Dashboard Preview](screenshots/dashboard_preview.png)

## 🎯 Business Questions Answered
- How is total revenue trending month-over-month?
- Which products and categories generate the highest revenue?
- How does current performance compare to previous months?
- Which regions contribute the most to overall sales?

## 🧰 Tools Used
- Power BI (data modeling, DAX, visualization)
- Excel (data cleaning and preparation)

## 📐 Data Model
- Fact table: Sales  
- Dimension tables: Date, Product, Region  
- Star schema for optimized performance and scalability

## 📈 Key KPIs
- Total Revenue
- Total Orders
- Average Order Value (AOV)
- Month-over-Month Growth %
- Top Performing Products

## 💡 Key Insights (Example)
- Revenue demonstrates clear month-over-month trends, highlighting seasonal demand patterns.
- A small number of products contribute a significant share of total revenue.
- Certain regions consistently outperform others, indicating potential focus areas for expansion.
- MoM growth analysis helps identify performance dips and recovery periods.

## 🧮 Sample DAX Measures
Below are examples of core DAX measures used in the dashboard.

```DAX
Total Revenue =
SUM(Sales[Revenue])

MoM Growth % =
DIVIDE(
    [Total Revenue] - CALCULATE([Total Revenue], PREVIOUSMONTH(Date[Date])),
    CALCULATE([Total Revenue], PREVIOUSMONTH(Date[Date]))
)

