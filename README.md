# KINO — E-Commerce BI Dashboard
### Power BI Dashboard for a Karachi-Based E-Commerce Startup

---

## Overview

This project is a multi-page Business Intelligence dashboard built in **Microsoft Power BI** for a Karachi-based e-commerce startup operating across 7 districts. The dashboard tracks the company's financial turnaround from 2025 to 2027 — covering revenue growth, delivery cost optimization, regional performance, and sales patterns.

The business grew net profit **10.9x** over three years, with profit margin improving from **43.6% → 78.9%**, driven largely by reducing per-order delivery costs from **Rs 500 → Rs 120**.

---

## Dashboard Pages

| Page | Description |
|---|---|
| **Turnaround Story** | Year-over-year financial performance; shows the company's profitability journey from 2025–2027 |
| **Growth Analysis** | Regional breakdown across Karachi's 7 districts; category and segment comparisons |
| **Operations** | Delivery cost trends, refund analysis, and expense breakdown |
| **Sales Patterns** | Festival vs. regular sales, salary week vs. regular week order behaviour |

---

## Key Results

| Metric | Value |
|---|---|
| Total Revenue (3 years) | Rs 49.5M |
| Total Net Profit | Rs 33.2M |
| Overall Profit Margin | 67.1% |
| Total Orders | 18,000 |
| Avg Order Value Growth | 6x (Rs 749 → Rs 4,508) |
| Delivery Cost Reduction | Rs 500 → Rs 120 per order |
| Order Acceptance Rate | 89.5% |
| Refund Rate | 10.5% |

---

## Data Model

Star schema architecture with the following tables:

**Fact Tables**
- `fact_turnaround_2025_2027` — primary analytical table (18,000 records)
- `fact_order_details` — line-item transaction data (35,000 records)
- `summary_monthly_performance` — pre-aggregated monthly KPIs

**Dimension Tables**
- `dim_customers` — 5,000 customers, demographic and location data
- `dim_orders` — order metadata, timing, and sales type
- `dim_products` — 100 SKUs across 5 categories
- `DateTable` — time intelligence for YoY comparisons

Total data volume: ~75,000 records across all tables (~18 MB)

---

## DAX Implementation

40+ DAX measures across 7 categories:

- **Revenue Metrics** — Total revenue, annual revenue, YoY growth
- **Profit Metrics** — Net profit, gross profit, profit margin
- **Order Metrics** — Total orders, average order value, profitability rate
- **Cost Metrics** — Delivery cost, product cost, cost ratio
- **Quality Metrics** — Refund rate, acceptance rate
- **Segmentation Metrics** — Festival vs. regular, salary week vs. regular week
- **Time Intelligence** — Period comparisons, monthly trends

---

## Tech Stack

- **Microsoft Power BI Desktop**
- **DAX** (Data Analysis Expressions)
- **Power Query (M)** — ETL pipeline for data cleaning and transformation
- **Star Schema** data modeling
- **CSV** source files

---

## Repo Structure

```
kino-bi-dashboard/
├── README.md
├── dashboard/
│   └── KINO_Dashboard.pbix          # Main Power BI file
├── data/
    ├── dim_customers.csv
    ├── dim_orders.csv
    ├── dim_products.csv
    ├── fact_order_details.csv
    ├── fact_turnaround_2025_2027.csv
    └── summary_monthly_performance.csv

```

---

## How to Open

1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
2. Clone or download this repository
3. Open `dashboard/KINO_Dashboard.pbix` in Power BI Desktop
4. Data is embedded — no additional setup required

---

## Dataset

The dataset is also available on Kaggle:
[KINO E-Commerce Karachi Pakistan](https://www.kaggle.com/datasets/bilalali06/kino-ecommerce-karachi-pakistan)

---

## Author

**Shreya Pramod Sakhare**  
Department of Business — University of Europe for Applied Sciences, Potsdam, Germany

*Built as part of a group project with two colleagues at UE Germany.*

---

## Note

The dataset used in this project is simulated to represent realistic e-commerce behaviour and is intended for academic and portfolio purposes.
