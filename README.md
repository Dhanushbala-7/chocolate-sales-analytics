# 🍫 Chocolate Sales Analytics — Power BI Dashboard

> A 5-page interactive business intelligence report analyzing $25.49M in global chocolate sales across 2023–2024.

📊 **[View Live Dashboard](YOUR_POWERBI_LINK_HERE)**

---

## Overview

This project simulates a real-world retail analytics scenario for a global chocolate brand operating across 6 countries, 100 stores, and 5 product categories. The goal was to build an executive-ready dashboard that surfaces actionable business insights — not just charts.

---

## Key Metrics

| Metric | Value |
|---|---|
| Total Revenue | $25.49M |
| Total Profit | $10.19M |
| Profit Margin | 40% |
| Total Orders | 1,000,000 |
| Total Customers | 50,000 |
| Avg Order Value | $25.49 |
| Countries | 6 |
| Stores | 100 |
| Period | Jan 2023 – Dec 2024 |

---

## Dashboard Pages

### 1. Executive Overview
- KPI cards with YoY % change (Revenue, Profit, Orders, AOV)
- Monthly revenue trend line (2023–2024)
- Revenue by country, store type, and top brands
- Key business insights panel

### 2. Sales Analysis
- Quantity trend over time
- Category growth: 2023 vs 2024 comparison
- Brand performance by category breakdown
- Discount impact by product category

### 3. Finance & Profit
- Profit trend line across 24 months
- Revenue vs Cost by month
- YTD Revenue and Profit accumulation curves
- Quarterly revenue: 2023 vs 2024

### 4. Customer Insights
- Revenue segmented by age group (18–25 to 60+)
- Loyalty member vs non-loyalty revenue split
- Monthly customer trend
- Revenue by gender

### 5. Store Performance
- Store revenue ranking table (100 stores)
- Revenue by city (Toronto, London, Paris, New York, Sydney, Melbourne, Berlin)
- Orders by country

---

## Key Business Insights

- **Airport channel leads**: Airport stores generate $7.6M — highest among all store types, driven by high-traffic foot traffic patterns
- **46–60 age group gap**: Highest revenue segment ($7.2M) but lowest loyalty penetration — significant retention opportunity
- **February seasonality**: Consistent revenue dip in Feb across both years, addressable through targeted promotions
- **Praline dominates, Milk is growing**: Praline tops category revenue at $3.3M; Milk shows the strongest YoY growth
- **Canada leads by country**: $5.1M — ahead of UK ($4.8M) and USA/France ($4.3M each)

---

## Technical Details

**Tools:** Power BI Desktop, DAX, Power Query

**DAX Measures include:**
- `Total Revenue = SUM(Sales[Revenue])`
- `Total Profit = [Total Revenue] - [Total Cost]`
- `Profit Margin % = DIVIDE([Total Profit], [Total Revenue])`
- `YoY Revenue % = DIVIDE([Total Revenue] - [LY Revenue], [LY Revenue])`
- `YTD Revenue = TOTALYTD([Total Revenue], Dates[Date])`
- `Revenue per Customer = DIVIDE([Total Revenue], DISTINCTCOUNT(Sales[CustomerID]))`

**Data Model:**
- Star schema with central fact table (Sales)
- Dimension tables: Customers, Products, Stores, Dates, Countries
- Cross-page slicers for Category, Country, and Year

---

## Screenshots

| Overview | Sales | Finance |
|---|---|---|
| ![Overview](screenshots/overview.png) | ![Sales](screenshots/sales.png) | ![Finance](screenshots/finance.png) |

| Customers | Store |
|---|---|
| ![Customers](screenshots/customers.png) | ![Store](screenshots/store.png) |

---

## How to Use

1. Click the [Live Dashboard](YOUR_POWERBI_LINK_HERE) link to interact with the report
2. Use the **Category**, **Country**, and **Year** slicers to filter all pages simultaneously
3. Navigate pages using the left sidebar icons
4. Download the `.pbix` file to explore the data model and DAX measures locally

---

## Author

**Dhanush Balamurali** — Aspiring Data Analyst
- 🔗 https://www.linkedin.com/in/dhanush-b-78b79a284/
- 📧 dhanushbalamurali02@gmail.com

---

*Built with Power BI Desktop | Data sourced from [Kaggle / synthetic retail dataset]*
