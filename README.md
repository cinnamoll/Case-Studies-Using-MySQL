# 🚀 8-Week SQL Challenge – Problem Summaries & SQL Skills

This document summarizes **8 real-world SQL case studies** from the **[8 Week SQL Challenge](https://8weeksqlchallenge.com/)** by Danny Ma.  
Each case study focuses on a different business domain and requires a specific set of SQL techniques – from basic aggregation to advanced window functions, data cleaning, and recursive CTEs.

---

## 📚 Case Study Overview

| Case | Title | Domain |
|------|-------|--------|
| #1 | Danny's Diner | Restaurant / Customer Analytics |
| #2 | Pizza Runner | Food Delivery / Logistics |
| #3 | Foodie-Fi | Subscription / Digital Product |
| #4 | Data Bank | Banking / Finance & Data Storage |
| #5 | Data Mart | Retail / Sustainability Impact |
| #6 | Clique Bait | E‑commerce / Digital Marketing |
| #7 | Balanced Tree Clothing | Retail / Product & Sales Analytics |
| #8 | Fresh Segments | Digital Marketing / Audience Segmentation |

---

## 1️⃣ Danny's Diner – Customer Loyalty Analysis

**Problem:**  
A small Japanese restaurant wants to understand customer visiting patterns, spending behavior, and favourite menu items to improve its loyalty program.

**Key SQL Skills:**
- `JOIN` (multiple tables)
- `GROUP BY` & aggregate functions (`SUM`, `COUNT`)
- Window functions: `ROW_NUMBER()`, `RANK()`
- `CASE WHEN` for conditional logic
- Date functions (`DATEDIFF` / date arithmetic)
- Common Table Expressions (`CTE`)

---

## 2️⃣ Pizza Runner – Food Delivery Optimization

**Problem:**  
A pizza delivery startup needs help cleaning messy data and analyzing runner performance, order timing, ingredient optimization, and pricing.

**Key SQL Skills:**
- **Data cleaning**: handling `null`, `NaN`, inconsistent text data
- **String manipulation**: `SPLIT_PART`, `REGEXP`, removing `km`, `minutes` suffixes
- **Data type conversion**: string → numeric, string → timestamp
- Aggregates & `GROUP BY`
- `JOIN` across 6+ tables
- Window functions for ranking
- Subqueries & CTEs
- **Recursive thinking** for ingredient lists

---

## 3️⃣ Foodie-Fi – Subscription Analytics

**Problem:**  
A food streaming service wants to understand customer subscription journeys, plan upgrades, churn patterns, and build a monthly payment schedule.

**Key SQL Skills:**
- Date functions (`DATE_PART`, `DATE_DIFF`, `AGE`)
- Window functions with `LEAD()` / `LAG()` for plan transitions
- **Conditional aggregation** (e.g., counting customers on a specific date)
- Percentage calculations (`ROUND`, `* 100.0`)
- **Recursive CTE** (for generating payment rows month by month)
- Handling **trial → paid → churn** sequences
- Complex `CASE` logic for pricing rules

---

## 4️⃣ Data Bank – Banking & Data Storage

**Problem:**  
A neo‑bank allocates cloud data storage based on customer transactions. Tasks include node reallocation, running balances, and simulating interest for data growth.

**Key SQL Skills:**
- **Running balance** using `SUM() OVER (ORDER BY date)`
- Percentile calculations: `PERCENTILE_CONT()` (median, 80th, 95th)
- Date arithmetic & grouping by month
- Aggregates with `FILTER` or `CASE`
- **Temporary tables** for multi‑step simulations
- Interest calculation (daily, non‑compounding / compounding)
- Window functions with `RANGE` or `ROWS`

---

## 5️⃣ Data Mart – Sales Impact of Sustainability Change

**Problem:**  
An online supermarket introduced sustainable packaging in June 2020. Analyze the impact on sales across regions, platforms, and customer segments.

**Key SQL Skills:**
- **Data cleansing**: converting strings to dates, extracting week/month/year, handling `null`
- `CASE` mapping for `age_band` and `demographic`
- **Before‑after analysis** using fixed date windows (`WHERE` with date ranges)
- Calculating growth/reduction rates (actual & percentage)
- Comparing year‑over‑year (2020 vs 2019/2018)
- `GROUP BY` with multiple dimensions
- Rolling totals / moving averages (optional)

---

## 6️⃣ Clique Bait – E‑commerce Funnel Analysis

**Problem:**  
A seafood e‑commerce store wants to analyse digital behaviour: page views, cart adds, purchases, and campaign effectiveness.

**Key SQL Skills:**
- **Funnel analysis**: views → cart → purchase (with event types)
- `COUNT(DISTINCT visit_id)` & conditional aggregation
- **Percentage calculations** (e.g., % of visits with purchase)
- `JOIN` across 5 tables
- **Window functions** for sequence numbers
- Creating **comma‑separated lists** with `STRING_AGG()`
- Campaign period mapping (`BETWEEN` dates)
- Uplift analysis (with vs without impression/click)

---

## 7️⃣ Balanced Tree Clothing – Product & Sales Analytics

**Problem:**  
A clothing company needs a financial report: total revenue, discounts, product penetration, and most common product combinations.

**Key SQL Skills:**
- Percentiles (`PERCENTILE_CONT`) for transaction revenue
- **Product penetration**: `COUNT(DISTINCT txn_id) / total transactions`
- **Combination analysis**: self‑join or array functions to find common product trios
- `GROUP BY` ROLLUP / CUBE (or manual grouping)
- Recursive CTE (for bonus: reconstruct product hierarchy)
- Window functions with `RANK()` / `DENSE_RANK()`
- Average discount value per transaction

---

## 8️⃣ Fresh Segments – Digital Marketing Segmentation

**Problem:**  
Analyze interest metrics (composition, index, ranking) for a client’s customer base to understand audience segments and detect anomalies.

**Key SQL Skills:**
- **Data cleansing**: convert `month_year` to date, handle nulls
- Anti‑joins (`LEFT JOIN` with `WHERE ... IS NULL`)
- **Time‑series analysis**: which interests appear in all months?
- Cumulative percentage (`SUM() OVER (ORDER BY ...)`)
- Standard deviation, min, max, rolling average
- **Business logic validation**: compare `month_year` vs `created_at`
- Window functions for ranking and percentile

---

## 🔗 Original Challenge

All case studies and datasets are provided by **Danny Ma** –  
👉 [8 Week SQL Challenge Official Website](https://8weeksqlchallenge.com/)

---

> *This summary is for learning and portfolio purposes. All rights belong to the original challenge author.*
