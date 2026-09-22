# Cafe Sales End-to-End Data Analytics Case Study

## Executive Summary
This case study presents a full end-to-end data analytics workflow on a transactional cafe sales dataset. The project encompasses raw data auditing, cleaning and transformation via Excel Power Query, exploratory data analysis (EDA), KPI derivation, interactive reporting in Power BI Desktop, and strategic business recommendations.

---

## 1. Problem Statement
The cafe management needed visibility into top-line revenue performance, customer purchasing behavior, product-level sales, channel efficiency, and point-of-sale (POS) data logging accuracy. The raw transaction records contained structural inconsistencies, duplicate rows, missing fields, and unformatted entries that prevented reliable business reporting.

---

## 2. Dataset Overview
- **Source:** Kaggle Cafe Transaction Data
- **Total Records:** ~9,485 unique customer transactions (post-cleaning)
- **Key Fields:** Transaction ID, Transaction Date, Item, Quantity, Price Per Unit, Total Spent, Payment Method, Location

---

## 3. Data Cleaning & Transformation (Task 1)
Using **Excel Power Query**, the following data cleansing steps were performed:
- **Deduplication:** Identified and removed duplicate transaction records.
- **Handling Missing Values:** Audited and handled missing entries in critical fields such as Payment Method and Location, categorizing unaccounted logs as `UNKNOWN` for audit tracking.
- **Type Casting & Standardization:** Converted transaction dates to standard `YYYY-MM-DD` format and formatted monetary values (`Price_Per_Unit`, `Total_Spent`) as currency.
- **Data Validation:** Reconciled math fields (`Quantity * Price_Per_Unit = Total_Spent`) to ensure financial accuracy.
- ![dirty_cafe_data.png)(images/dashboard_view.png)
- ![cleaned_cafe_data.png](images/dashboard_view.png)

---

## 4. Exploratory Data Analysis & KPIs (Task 2)
### Core Performance Metrics
- **Total Revenue:** ~$85K ($84,822)
- **Total Orders:** 9,485 unique transactions
- **Average Order Value (AOV):** $8.94
- **Total Units Sold:** 28,636 items

### Core Analytical Insights
1. **Product Revenue Leadership:** High-margin food lines (**Salad** and **Sandwich**) generate the highest overall revenue share, outperforming standalone beverage lines.
2. **Channel Distribution Balance:** Revenue generation is split evenly between **In-store** (~50.5%) and **Takeaway** (~49.5%) locations.
3. **Payment Method Spend Behavior:** Customer spend across verified channels (**Credit Card**, **Digital Wallet**, and **Cash**) remains consistent, averaging ~$8.90 to $9.00 per visit.
4. **POS Data Quality Gaps:** Identified tracking gaps where roughly 25%–30% of sales attribution sat under `UNKNOWN` flags, signaling an operational need for register system maintenance.

---

## 5. Interactive Business Intelligence Dashboard (Task 3)
An executive dashboard was constructed in **Power BI Desktop** featuring custom UI card containers, light gray canvas styling, and interactive slicers.

![SWYNEX_DATA_DASHBOARD.png](images/dashboard_view.png)

### Dashboard Features
- **Dynamic Slicers:** Interactive filtering by Location (`In-store`, `Takeaway`), Payment Channel (`Cash`, `Credit Card`, `Digital Wallet`), and Date Range.
- **Cross-Filtering:** Selecting any visual element updates all on-page charts and KPI cards dynamically.
- **DAX Calculations:** Explicit DAX measures built for revenue, distinct order volume, average order value, and total units.

---

## 6. Strategic Business Recommendations
1. **Promote Combo Bundling:** Pair top-selling food items (Salad, Sandwich) with higher-margin beverages (Coffee, Smoothie) to increase overall basket size.
2. **POS System Audit:** Upgrade point-of-sale terminal software to eliminate `UNKNOWN` payment and location entries, improving transactional tracking.
3. **Optimize Channel Operations:** Maintain equal operational staffing for In-store and Takeaway fulfillment given their balanced 50/50 revenue split.

---

## Tools & Technologies
- **Data Cleaning:** Excel Power Query
- **Exploratory Analysis:** Excel Pivot Tables & Pivot Charts
- **Interactive Dashboard:** Power BI Desktop & DAX
- **Documentation & Version Control:** GitHub
