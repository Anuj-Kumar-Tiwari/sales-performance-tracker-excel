<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&pause=1000&color=2196F3&center=true&vCenter=true&width=700&lines=Sales+Performance+Tracker;Advanced+Excel+Portfolio+Project;Turning+Raw+Data+into+Business+Insights" alt="Typing SVG" />
</p>

<br/>

![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Power Query](https://img.shields.io/badge/Power_Query-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Pivot Tables](https://img.shields.io/badge/Pivot_Tables-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![DAX](https://img.shields.io/badge/Advanced_Formulas-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)

<br/>

> **Analyzed 9,994 sales orders (2014–2017) across 3 categories and 4 regions using Advanced Excel — uncovering $2.29M in revenue, $286K profit, and 1,871 loss-making orders.**

<br/>

[![LinkedIn](https://img.shields.io/badge/Anuj_Kumar_Tiwari-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/anuj-kumar-tiwari-107704208)
[![GitHub](https://img.shields.io/badge/GitHub-Anuj--Kumar--Tiwari-181717?style=flat-square&logo=github)](https://github.com/Anuj-Kumar-Tiwari)
[![Email](https://img.shields.io/badge/Email-anuujji@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:anuujji@gmail.com)

</div>

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [KPI Summary](#-kpi-summary)
- [Dataset](#-dataset)
- [Excel Techniques Used](#-excel-techniques-used)
- [Dashboard](#-excel-dashboard)
- [Key Insights](#-key-insights)
- [How to Run](#-how-to-run)
- [Tech Stack](#-tech-stack)

---

## 🎯 Project Overview

This is an **end-to-end Advanced Excel project** on the Superstore Sales dataset spanning 4 years (2014–2017). The objective was to clean raw data, apply advanced Excel formulas for KPI extraction, build Pivot Table summaries, and deliver an interactive Excel Dashboard with slicers.

```
📦 Raw Data (CSV)   →   🛠️ Excel (Advanced)   →   📊 Interactive Dashboard
  9,994 rows              Data Cleaning              KPI Cards + Charts
  21 columns              SUMIFS / COUNTIFS          Pivot Tables + Slicers
  4 years                 VLOOKUP / INDEX-MATCH       Monthly Trend Analysis
```

---

## 💰 KPI Summary

<div align="center">

| 📊 Metric | 🔢 Value |
|:---|:---:|
| 💵 Total Revenue | **$2,297,201** |
| 📈 Total Profit | **$286,397** |
| 🧾 Total Orders | **5,009** |
| 📦 Total Quantity Sold | **37,873 units** |
| 💳 Avg Order Value | **$458.61** |
| 📉 Profit Margin | **12.47%** |
| ⚠️ Loss-Making Orders | **1,871** |

</div>

---

## 🗂️ Dataset

The dataset is the **Superstore Sales Dataset** — a widely used retail business simulation dataset containing 4 years of transactional data.

```
Source File:  Sample_-_Superstore.csv   →   Loaded as Raw Data sheet
Cleaned File: Good-Data sheet            →   Used for all analysis
Time Period:  January 2014 – December 2017
Records:      9,994 rows | 21 columns
```

### 📋 Column Reference

| Column | Description |
|--------|-------------|
| Order ID | Unique identifier per customer order |
| Order Date / Ship Date | Transaction and delivery timestamps |
| Ship Mode | Delivery method (Standard, Second, First Class, Same Day) |
| Customer ID / Name | Customer reference details |
| Segment | Consumer / Corporate / Home Office |
| Region | Central / East / South / West |
| Category | Furniture / Office Supplies / Technology |
| Sub-Category | 17 product sub-categories |
| Sales | Revenue per line item |
| Quantity | Units ordered |
| Discount | Discount applied (0–0.8) |
| Profit | Net profit per line item |

---

## 🛠️ Excel Techniques Used

### 1. Data Cleaning (Raw Data → Good-Data)
- Fixed inconsistent date formats in `Ship Date` column
- Removed duplicates and validated data integrity
- Standardized column headers and data types

### 2. SUMIFS / COUNTIFS (SumIFs & Countifs Sheets)
```excel
=SUMIFS('Good-Data'!R:R, 'Good-Data'!O:O, "Furniture")
→ Total Sales for Furniture category: $741,999

=COUNTIFS('Good-Data'!O:O, "Technology")
→ Order count for Technology category

=AVERAGEIFS('Good-Data'!T:T, 'Good-Data'!O:O, "Office Supplies")
→ Avg Discount for Office Supplies
```

### 3. VLOOKUP (Vlookup Sheet)
```excel
=VLOOKUP($C$4, 'Good-Data'!$B:$N, 6, 0)
→ Lookup Customer Name by Order ID

=VLOOKUP($C$4, 'Good-Data'!$B:$N, 7, 0)
→ Lookup Segment by Order ID
```

### 4. INDEX-MATCH (Index & Match Sheet)
```excel
=INDEX('Good-Data'!$G:$G, MATCH($D$4, 'Good-Data'!$N:$N, 0))
→ Product Name lookup by Product ID

=INDEX('Good-Data'!$O:$O, MATCH($D$4, 'Good-Data'!$N:$N, 0))
→ Category lookup by Product ID
```

### 5. Monthly Summary (Monthly Summary Sheet)
- `EXTRACT`-equivalent year/month grouping via Pivot
- YoY Revenue tracking: 2014 → 2015 → 2016 → 2017
- Profit Margin % column: `=Profit / Sales`

### 6. Pivot Tables (Pivot Sheet)
- Region-wise Total Sales breakdown
- Sub-Category Sales ranking (17 sub-categories)
- Monthly Sales split by Category (Furniture vs Office Supplies vs Technology)

---

## 📊 Excel Dashboard

The `Dashboard` sheet consolidates all analysis into a **single-page interactive report** with slicers for filtering by Category, Region, and Year.

| Visual | Type | Key Insight |
|--------|------|-------------|
| YoY Revenue Trend | Line Chart | 2017 was the best year at $733K |
| Sales by Category | Bar Chart | Technology leads at $836K |
| Sales by Region | Donut Chart | West tops at $725K |
| Top Sub-Categories | Horizontal Bar | Phones #1 at $330K |
| Monthly Summary Table | Pivot Table | March is consistently strong |
| Profit Margin by Category | KPI Card | Technology: 17.4% margin |

### Slicers / Filters
- 📅 Year (2014 / 2015 / 2016 / 2017)
- 🏷️ Category (Furniture / Office Supplies / Technology)
- 🌍 Region (Central / East / South / West)

---

## 💡 Key Insights

```
🏆  TOP CATEGORY     →  Technology ($836,154 revenue — highest)
💹  BEST MARGIN      →  Technology (17.4%) & Office Supplies (17.0%)
⚠️  LOW MARGIN       →  Furniture (only 2.5% profit margin)
📉  LOSS LEADERS     →  Tables (-$17,725) & Bookcases (-$3,473) in profit
🌍  TOP REGION       →  West ($725,458) followed by East ($678,781)
👥  TOP SEGMENT      →  Consumer (50.5% of total revenue)
📅  BEST YEAR        →  2017 ($733,215 — 51.4% growth over 2014)
🏙️  TOP STATE        →  California ($457,688) then New York ($310,876)
📦  TOP SUB-CAT      →  Phones ($330,007) & Chairs ($328,449)
🔴  LOSS ORDERS      →  1,871 out of 9,994 orders are loss-making
```

---

## 🚀 How to Run

### Step 1 — Open in Excel

```
1. Open Sales_Performance_Tracker.xlsx in Microsoft Excel
2. Enable macros if prompted (required for slicers)
3. Navigate to the Dashboard sheet for the full interactive view
```

### Step 2 — Explore Individual Sheets

```
Raw Data      →  Original uncleaned dataset (9,994 rows)
Good-Data     →  Cleaned dataset used for all formulas
Monthly Summary →  Year-month aggregated KPIs with Pivot
SumIFs        →  Category-level sales, profit & discount analysis
Countifs      →  Order count per category
Vlookup       →  Customer/order lookup tool (enter Order ID in C4)
Index & Match →  Product lookup tool (enter Product ID in D4)
Pivot         →  Region, Sub-Category & Monthly breakdown tables
Dashboard     →  Interactive KPI Dashboard with slicers
```

### Step 3 — Refresh Data (Optional)

```
1. Replace Sample_-_Superstore.csv with updated data file
2. Go to: Data → Refresh All
3. Dashboard updates automatically via Pivot Table connections
```

---

## 🗃️ Project Structure

```
📁 Sales-Performance-Tracker/
│
├── 📊 Sales_Performance_Tracker.xlsx    # Main Excel workbook (9 sheets)
│   ├── Raw Data                          # Original Superstore dataset
│   ├── Good-Data                         # Cleaned & validated data
│   ├── Monthly Summary                   # Year-Month KPI aggregation
│   ├── SumIFs                            # SUMIFS formula analysis
│   ├── Countifs                          # COUNTIFS formula analysis
│   ├── Vlookup                           # VLOOKUP lookup tool
│   ├── Index & Match                     # INDEX-MATCH lookup tool
│   ├── Pivot                             # Pivot Table breakdowns
│   └── Dashboard                         # Interactive KPI Dashboard
│
├── 📄 Sample_-_Superstore.csv           # Source data file
├── 📝 README.md                          # This documentation
└── 📋 Sales_Performance_Report.pdf       # Project analysis report
```

---

## 🛠️ Tech Stack

<div align="center">

| Tool | Purpose |
|------|---------|
| ![Excel](https://img.shields.io/badge/-Microsoft%20Excel-217346?logo=microsoft-excel&logoColor=white&style=flat-square) | Core analysis, formulas, dashboard |
| **SUMIFS / COUNTIFS** | Multi-condition aggregation |
| **VLOOKUP / INDEX-MATCH** | Dynamic data lookups |
| **Pivot Tables** | Summary & cross-tab reporting |
| **Power Query** | Data cleaning & transformation |
| **Excel Charts** | Line, Bar, Donut visualizations |

</div>

---

## 📬 Connect with Me

<div align="center">

If you found this project useful, feel free to ⭐ **star the repo** and connect!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Anuj_Kumar_Tiwari-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/anuj-kumar-tiwari-107704208)
[![GitHub](https://img.shields.io/badge/GitHub-Anuj--Kumar--Tiwari-181717?style=for-the-badge&logo=github)](https://github.com/Anuj-Kumar-Tiwari)
[![Email](https://img.shields.io/badge/Gmail-anuujji@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:anuujji@gmail.com)

<br/>

*Made with ❤️ by Anuj Kumar Tiwari — Data Analyst Portfolio Project*

</div>
