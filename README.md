# AdventureWorks-Sales-Performance-Dashboard-Using-Power-BI
A full end-to-end Business Intelligence project built in Power BI Desktop — transforming raw CSV files into an interactive, multi-page sales dashboard with DAX-powered KPIs, geographic analysis, product drill-downs, and customer intelligence.

---
 
## 🗂️ Table of Contents
 
- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Data Sources](#data-sources)
- [Data Model](#data-model)
- [Dashboard Pages](#dashboard-pages)
- [DAX Measures](#dax-measures)
- [Key Findings](#key-findings)
- [Tools & Skills](#tools--skills)
- [File Structure](#file-structure)
- [How to Use](#how-to-use)
- [Author](#author)
---
 
## Project Overview
 
AdventureWorks is a global manufacturing company producing cycling equipment and accessories. 
The management team needed a structured way to monitor business performance across sales, revenue, profit, returns, regions, products, and customers — all they provided was a folder of raw CSV files.
 
| Dimension | Detail |
|-----------|--------|
| Source files | 8 raw CSV files |
| Dashboard pages | 4 interactive pages |
| DAX measures | 40+ calculated columns and measures |
| Data model | Star schema — 1 fact table, 5 dimension tables |
| Time period | January 2020 — June 2022 |
| Geographic coverage | 6 countries across 3 continents |
 
---
 
## Problem Statement
 
Without a BI layer, the business was operating on intuition:
 
- No unified view of revenue, profit, or return performance
- No way to compare regional or territory-level sales
- No product-level insight into what was driving — or hurting — the business
- No customer segmentation or high-value customer identification
- Decisions made without data
  
**The objective:** Use Power BI Desktop to connect, model, and visualize the data — then answer the four critical business questions: how are we performing, where, on which products, and with which customers?
 
---
 
## Data Sources
 
All data was provided as flat CSV files — no pre-built database or relationships.
 
| File | Type | Description |
|------|------|-------------|
| `Sales_Data_2020.csv` | Fact | Transaction records — year 2020 |
| `Sales_Data_2021.csv` | Fact | Transaction records — year 2021 |
| `Sales_Data_2022.csv` | Fact | Transaction records — year 2022 |
| `Product_Lookup.csv` | Dimension | Product catalog — SKU, name, cost, price |
| `Customer_Lookup.csv` | Dimension | Customer demographics — name, gender, income, occupation |
| `Territory_Lookup.csv` | Dimension | Sales territories — region, country, continent |
| `Product_Categories_Lookup.csv` | Dimension | Category hierarchy |
| `Product_subCategories_Lookup.csv` | Dimension | subcategory hierarchy |
| `Returns_Data.csv` | Fact | Return transactions by product and territory |
 
**Data preparation (Power Query):** All files were connected, cleaned, and transformed — including data type standardization, null handling, duplicate removal, and column renaming for consistency.
 
---
 
## Data Model
 
A **Data model** was built in Power BI's model view, with all tables connected through defined one-to-many relationships.
 
``
 
**Relationship rules:** All relationships are one-to-many, with single filter direction flowing from dimension to fact tables.
 
---
 
## Dashboard Pages
 
### Page 1 — Executive Summary
The top-level KPI view. Tracks revenue, profit, orders, and return rate with month-over-month comparisons, monthly targets, and sparkline trends. Includes a product/order matrix and date slicer.
 
**Key visuals:** KPI cards with MoM%, line chart (revenue trend), bar chart (orders by category), matrix (product performance), slicers (date, KPI type)
 
### Page 2 — Map
Geographic revenue distribution across all active sales territories. Bubble map scaled by revenue, filterable by continent and date.
 
**Key visuals:** ArcGIS bubble map, territory filter slicer
 
### Page 3 — Product Detail
Drill into individual product performance. Gauge charts track current month orders, revenue, and returns against targets. Line and area charts show historical trends per product.
 
**Key visuals:** Gauge charts (orders / revenue / returns vs target), line chart (trend over time), area chart, product name slicer
 
### Page 4 — Customer Detail
Customer-level intelligence. Revenue per customer, occupation and income-level breakdowns, top customer table, and metric selection via field parameters.
 
**Key visuals:** KPI cards, donut charts (by occupation / income), top customer table, revenue sparkline, field parameter slicer
 
---
 

## Key Findings
 
**Bikes drive nearly all revenue.** Bikes generate $23.6M — 94.8% of total revenue — despite representing only 55% of total orders. This concentration is a strategic risk.
 
**North America and Pacific dominate geographically.** The USA ($9.39M) and Australia ($9.06M) together account for over 72% of revenue. European markets remain significantly underdeveloped relative to their potential.
 
**Return rate exceeds its target.** The overall return rate is 2.17% against a 2.00% target. Accessories (2.44%) and Clothing (2.47%) have the highest rates — both above the company average.
 
**Revenue consistently beats monthly targets.** Monthly revenue has hit or surpassed the $1.77M target in most periods, with overall growth of +107% from January 2020 to June 2022.
 
**Top customers generate outsized value.** The highest-revenue customer ($15,999) represents 10× the average customer value ($1,431). Professionals and Skilled Manuals account for 54% of total revenue.
 
---
 
## Tools & Skills
 
| Tool / Skill | Usage |
|---|---|
| **Power BI Desktop** | Full dashboard environment |
| **Power Query (M Language)** | Data connection, cleaning, and transformation |
| **DAX** | 40+ calculated columns and measures |
| **data modeling** | Relational data modeling |
| **Time Intelligence** | MoM, MTD, and period comparison functions |
| **Conditional Formatting** | Dynamic KPI color logic |
| **Field Parameters** | User-controlled metric switching |
| **ArcGIS Maps** | Geographic territory visualization |
| **Data Storytelling** | Business narrative and insight communication |
 
---
 
## File Structure
 
```
adventureworks-sales-dashboard/
│
│
├── 📊 Adventure_Works_Project.pbix       # Power BI report file
├── 📑 AdventureWorks_Dashboard_PPT.pptx  # Project presentation
└── 📄 README.md                          # This file
```
 
---
 
## How to Use
 
1. **Clone or download** this repository
2. Open `Adventure_Works_Project.pbix` in **Power BI Desktop** (free download from Microsoft)
3. Explore all four report pages using the navigation buttons on each page
4. Use the date slicers, product selectors, and field parameters to interact with the dashboard
> **Note:** Power BI Desktop is required to open the `.pbix` file. The dashboard is optimized for 1920×1080 resolution.
 
---
 
## Author
 
**Mohammed Drihmi** — Data Analyst 

Passionate about turning raw data into business decisions. This project demonstrates end-to-end analytical thinking: from data cleaning and model design to segmentation, insight generation, and executive communication.

 
*AdventureWorks Sales Performance Dashboard · Power BI Desktop *
