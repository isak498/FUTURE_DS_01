# FUTURE_DS_01 — Business Sales Performance Analytics

## 📌 Project Overview
This project analyzes 2 years (2022–2024) of retail sales data covering 73,100 transactions across 5 stores, 4 regions, and 5 product categories. The goal is to uncover revenue trends, identify top and weak performers across categories/regions, and evaluate the effectiveness of the business's discount and promotion strategy.

This was completed as **Task 1** of the Data Science & Analytics Internship at **Future Interns**.

---

## ❓ Problem Statement
The business needed answers to the following questions, which were not visible from raw transactional data alone:

- Is revenue growing year-over-year, or staying flat?
- Which product categories and regions drive the most (and least) revenue?
- Is the current discount/promotion strategy actually increasing sales, or just reducing margin?
- Are there seasonal or external (weather) patterns worth planning around?
- Which stores are top performers, and is that driven by the store itself or by region?

Without structured analysis, the business had no clear way to prioritize where to focus growth efforts or where money was being spent without a return.

---

## ✅ Solution Approach
A two-stage analysis was performed:

1. **Python (Pandas)** was used to load, clean, and prepare the raw dataset — fixing data types, engineering a Revenue and Net Revenue metric (since the raw data only contained Units Sold and Price), and exporting a clean dataset.
2. **Power BI** was used to build a 4-page interactive dashboard answering the business questions visually, followed by a written business insights report translating the findings into concrete recommendations.

This mirrors how a real analytics engagement is run — code for cleaning and reproducibility, BI tooling for stakeholder-facing visualization, and a written report for decision-makers who won't open the dashboard themselves.

---

## 🛠️ Tools Used
- **Python** (Pandas, NumPy) — data cleaning, type correction, feature creation (Revenue, Net Revenue, Discount Amount)
- **Power BI** — interactive 4-page dashboard
- **Jupyter Notebook** — exploratory analysis and documentation of cleaning steps

---

## 🧹 Data Cleaning Summary
- Verified dataset integrity: 0 missing values, 0 duplicate rows across 73,100 rows
- Converted `Date` column from text to proper datetime format
- Created `Revenue` (Units Sold × Price), `Discount_Amount`, and `Net_Revenue` (Revenue − Discount) since the raw dataset had no direct sales/revenue field
- Standardized column names (removed spaces/special characters) for compatibility with Power BI
- Exported cleaned dataset as `cleaned_sales_data.csv` for use in the dashboard


---


## 📊 Dashboard Preview

### Page 1 — Sales Overview
<img width="719" height="402" alt="image" src="https://github.com/user-attachments/assets/1548a589-4547-4b56-8467-3c02aaebaa40" />

KPI cards (Gross Revenue, Net Revenue, Discount, Units Sold), monthly revenue trend, revenue by year/quarter, discount distribution.

### Page 2 — Category & Product Analysis
<img width="717" height="406" alt="image" src="https://github.com/user-attachments/assets/b283f569-eed4-4d42-aa81-d1597e43292f" />
Revenue and units sold by category, discount impact by category, gross vs net revenue comparison.

### Page 3 — Regional Performance
<img width="719" height="406" alt="image" src="https://github.com/user-attachments/assets/d2604135-cd8e-4a71-9446-61b34c32ffd0" />
Revenue and units by region, region-category breakdown, store performance.

### Page 4 — Seasonal & External Factors
<img width="719" height="404" alt="image" src="https://github.com/user-attachments/assets/2d1670a7-f5ed-400f-aa40-960dc86cc5e6" />
Revenue by season, weather impact, holiday/promotion effectiveness.

---

## 🔍 Key Insights (Summary)
- Revenue is stable but nearly flat year-over-year (2022 vs 2023)
- Furniture is the top category; Electronics is the weakest
- East region outperforms all others; West is the weakest — though gaps are minimal across the board
- **Holiday/Promotion days generated less revenue than normal days** — the most critical finding, suggesting the current promotional strategy isn't working
- Winter is the strongest season; Sunny weather correlates with peak sales

📄 Full findings and actionable recommendations: [business_insights.md]

---
