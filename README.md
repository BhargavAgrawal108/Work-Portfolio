# Work-Portfolio
Power BI project showcasing financial performance analysis and interactive dashboards for FP&amp;A use cases. Includes revenue trends, expense tracking, profitability metrics, and key financial KPIs for business insights.

# Retail Store Insights Dashboard – Power BI Project

## Overview

The **Retail Store Insights Dashboard** is an interactive Power BI project designed to analyze retail performance across countries, sales regions, and cities.  
It provides a 360° view of key business metrics — revenue, profit, returns, and sales trends — to help management make data-driven decisions efficiently.

---

## Objectives
- Track and visualize **Total Revenue**, **Profit**, **Quantity Sold**, and **Profit Margin**.
- Compare **Monthly and Weekly trends** for revenue, profit, and returns.
- Monitor **Revenue vs Target** performance to evaluate progress.
- Identify top and low-performing brands with **return rate analysis**.
- Enable **dynamic insights** through slicers for year, region, and city.

---

## Dashboard Highlights

| Section | Description |
|----------|-------------|
| **KPI Cards** | Displays Total Revenue, Total Profit, Quantity Sold, and Profit Margin. |
| **Monthly Metrics** | Shows monthly revenue, returns, and profit compared to the previous month. |
| **Revenue vs Target** | Gauge visual tracking progress toward sales goals. |
| **Weekly & Quarterly Trends** | Visualizes sales and profit performance across time. |
| **Brand Analysis Table** | Breaks down Total Transactions, Profit, Margin, and Return Rate by brand. |
| **Geographical Insights** | Pie chart to show revenue contribution by country. |
| **Slicers** | Interactive filters for Year, Region, City, and Country. |

---

## Key Learnings & Techniques
- Developed **DAX measures** for KPIs and Time Intelligence (MTD, YTD, Previous Month).
- Used **conditional formatting** for visual emphasis on positive/negative trends.
- Created dynamic titles and tooltips for a more engaging user experience.
- Applied **clean UI design** principles for better readability and visual storytelling.
- Designed an effective **data model** supporting flexible slicer interactions.

---

## Tools & Technologies
- **Power BI Desktop**
- **Power Query Editor** (for data transformation)
- **DAX (Data Analysis Expressions)**  
- **Excel / CSV data source**

---

## Data Model
The dataset follows a **Star Schema**:
- **Fact Table:** Transactions (Revenue, Quantity, Profit, Returns)
- **Dimension Tables:** Date, Product, Brand, Country, Region, City

---

## Key Measures (Examples)
```DAX
Total Revenue = SUM('Sales'[Revenue])
Total Profit = SUM('Sales'[Profit])
Profit Margin % = DIVIDE([Total Profit], [Total Revenue], 0)

MTD Revenue = TOTALMTD([Total Revenue], 'Date'[Date])
Previous Month Revenue = CALCULATE([Total Revenue], PREVIOUSMONTH('Date'[Date]))

Weekend Transactions = 
CALCULATE(
    COUNTROWS('Sales'),
    FILTER('Sales', WEEKDAY('Sales'[Date], 2) >= 6)
)
