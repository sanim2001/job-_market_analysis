# Australian Job Market Insights Dashboard (LinkedIn → CSV → MySQL → SQL → Power BI)

Analyze Australian job market demand by title, location, salary, and skill sets (e.g., Python vs R, Tableau vs Power BI) using a reproducible data pipeline.

> **Data source note:** This project demonstrates educational techniques for collecting public job listings information from LinkedIn using Python. Always review and comply with LinkedIn’s Terms of Service and applicable laws before scraping. Prefer official APIs or first‑party data exports whenever possible.

---

##  What this repo contains

- `Australian_Job_Market.ipynb` — Python notebook used to collect job postings from LinkedIn and export to CSV.
- `data_cleanning.sql` — SQL scripts for cleaning/standardizing raw tables after import.
- `SQLQuery.sql` — Example analytics queries (skills, salary bands, geography, trendlines).
- `data/` — (optional) Directory for CSV outputs.
- `powerbi/` — (optional) Directory to store the Power BI `.pbix` file.

---

##  End‑to‑End Pipeline

1. **Scrape** job postings from LinkedIn with Python (requests/BeautifulSoup or Scrapy) → save as **CSV**.
2. **Load** CSV into **MySQL** (raw table).
3. **Clean & standardize** using SQL in `data_cleanning.sql` to produce curated tables/views.
4. **Analyze** with `SQLQuery.sql` (skills demand, salary distribution, location heatmap, time trends).
5. **Visualize** in **Power BI** (DirectQuery/Import from MySQL).

---

## Tech Stack

- **Python**: scraping + CSV export (Jupyter Notebook)
- **Pandas**: quick transformations before DB load
- **MySQL**: storage, cleaning, and analytics
- **SQL**: data quality checks + analytical queries
- **Power BI**: dashboard (filters by title, state/city, skills, date, salary band)



##  Setup & Prerequisites

- Python 3.10+
- MySQL 8.x (server + client)
- Power BI Desktop (Windows) or Power BI Service (for publishing)


---
## Step 1 — Scrape LinkedIn → CSV


##  Step 2 — Load CSV → MySQL

Example schema for a raw table:

Load the CSV (two common options):

**A) MySQL `LOAD DATA`**

**B) Python (pandas + SQLAlchemy)**

## Step 3 — Data Cleaning (SQL)
## Step 4 — Analysis (SQL)
## Step 5 — Power BI Dashboard

---

## Reproduce End‑to‑End

```bash
# 1) Run scraper notebook → writes CSV in ./data
# 2) Create DB + raw table (see DDL above)
# 3) Load CSV into jobs_raw (LOAD DATA or pandas.to_sql)
# 4) Run data_cleanning.sql to build curated views/tables
# 5) Run SQLQuery.sql for analytics sanity checks
# 6) Open powerbi/Australian_Job_Market.pbix (or build new) and point to jobs_clean
```

