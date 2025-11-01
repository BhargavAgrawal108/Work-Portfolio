## 👋 About Me  

Hey! I’m **Bhargav Agrawal** — a Finance professional by education and a data storyteller by passion.  
I love exploring how numbers can narrate business performance and guide smarter decisions.  

Currently working in **Financial Planning & Analysis (FP&A)**, I blend my finance background (B.Com, M.Com) with analytics tools like **Power BI**, **Excel**, and **DAX** to simplify complex data into meaningful insights.  

I also manage my own personal investments and have a keen interest in topics like **retirement planning**, **insurance**, and **wealth growth** — blending finance with real-life strategy.  
Outside of finance and dashboards, you’ll find me experimenting in the **kitchen**  — cooking is my creative escape!  

---
#  Buy This**
**https://bhargav108.gumroad.com/l/cahdh**

**https://bhargav108.gumroad.com/l/qqpee**
---

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

## Dashboard Screenshot

https://github.com/BhargavAgrawal108/Work-Portfolio/blob/main/Screenshots/Project%20-%20Retail%20store%20snip.png?raw=true

https://github.com/BhargavAgrawal108/Work-Portfolio/blob/main/Screenshots/Project%202.png?raw=true

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

## Connect With Me  

 **LinkedIn:**  - https://www.linkedin.com/in/bhargav-agrawal-6b60b01a1/  
 **Email:** - Bhargav108108@gmail.com

 ---
 
✨ *Thanks for stopping by! I’m always open to collaborations, analytics discussions, and new learning opportunities.*

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
---
