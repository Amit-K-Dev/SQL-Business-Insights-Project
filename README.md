# 📊 SQL Business Insights Project – Sales Dataset

## 🔍 Project Overview

This project analyzes a structured **sales dataset using PostgreSQL** to uncover key business insights related to revenue, profitability, customer behavior, and product performance.

The objective was to simulate a **real-world relational database environment** and perform advanced SQL analysis using:

- Joins
- Aggregations
- CTEs
- Window Functions
- Customer segmentation logic

This project reflects how a **Data Analyst explores and analyzes business data** to support data-driven decision making.

---

# 🗄️ Database Structure

The dataset follows a relational schema consisting of four tables:

| Table | Description |
|------|-------------|
| `customers` | Customer information |
| `products` | Product details including cost and selling price |
| `orders` | Order-level data |
| `order_details` | Transaction-level product quantities |

The database contains:

- **20 customers**
- **15 products**
- **100 orders**
- **300 order line items**

---

# 📊 Entity Relationship Diagram (ERD)

Customers (1) —— (Many) Orders  
Orders (1) —— (Many) OrderDetails  
Products (1) —— (Many) OrderDetails  

![ER Diagram](screenshots/erd.png)

---

# 📎 Dataset Generation

The dataset was **programmatically generated using PostgreSQL functions**.

Techniques used:

- Random customer assignment using `RANDOM()`
- Random date generation within **2024**
- Random region selection using **ARRAY indexing**
- Multiple order line items generated using `generate_series()`

This approach simulates **realistic transactional business data** while maintaining relational integrity using **foreign key constraints**.

---

# 📈 Key Business Metrics Analyzed

## 💰 Revenue & Profit

- **Total Revenue:** 10,359,200
- **Total Profit:** 3,388,000
- **Profit Margin:** ~32.7%

---

## 🏆 Product Performance

- **Top Revenue Product:** Laptop Pro 15
- **Revenue Contribution:** ~49% of total revenue

Product ranking calculated using:

- `RANK()`
- `DENSE_RANK()`

---

## 👤 Customer Analysis

- **Top Customer (CLV):** Arjun Rao – 892,700
- **Repeat Customers:** 19 out of 20
- **Revenue from Repeat Customers:** 96%
- **Profit from Repeat Customers:** ~97%

---

## 🛒 Average Order Value (AOV)

- **Average Order Value:** 103,592

This indicates **high-ticket purchasing behavior**, likely driven by **premium electronic products**.

---

## 📊 Pareto Analysis (Top 10% Customers)

- **Top 10% customers contribute ~16% of revenue**

This suggests revenue is **distributed across many customers**, reducing concentration risk.

---

# 📷 Sample Query Outputs

## 🔹 Total Revenue & Order Summary

![Total Revenue](screenshots/total_revenue.png)

---

## 🔹 Product Revenue Ranking (Window Function – RANK)

![Product Ranking](screenshots/product_ranking.png)

---

## 🔹 Customer Lifetime Value (CLV)

![Customer CLV](screenshots/customer_clv.png)

---

## 🔹 Revenue Contribution: Repeat vs One-Time Customers

![Customer Segmentation](screenshots/repeat_vs_onetime_revenue.png)

---

## 🔹 Pareto Analysis – Top 10% Customers

![Pareto Analysis](screenshots/pareto_top_10_percent.png)

---

# 🧠 SQL Concepts Used

Key SQL concepts applied in this project:

### Joins
- `INNER JOIN`
- Multi-table joins across relational schema

### Aggregations
- `SUM()`
- `COUNT()`
- `AVG()`

### Grouping
- `GROUP BY`
- `HAVING`

### CTEs
- `WITH` clause for readable query structure

### Window Functions

- `RANK()`
- `DENSE_RANK()`
- `NTILE()`

### Other Techniques

- Date functions
- Revenue & margin calculations
- Customer segmentation logic
- Pareto analysis

---

# 🎯 Business Insights

Key insights from the analysis:

- **Repeat customers drive the majority of revenue and profit**
- The business appears **retention-driven rather than acquisition-driven**
- Revenue is **moderately diversified across customers**
- A small number of **high-value products generate significant revenue**
- There is strong opportunity to **convert one-time buyers into repeat customers**

---

# 🛠️ Tools Used

| Tool | Purpose |
|-----|--------|
| PostgreSQL | Database creation and SQL analysis |
| VS Code | Query development |
| SQLTools Extension | PostgreSQL query execution |

---

# 📁 Project Structure

```
SQL-Business-Insights-Project/
│
├── 1_database_setup.sql
├── 2_data_inserts.sql
├── 3_business_queries.sql
├── README.md
└── screenshots/
    ├── total_revenue.png
    ├── product_ranking.png
    ├── customer_clv.png
    ├── repeat_vs_onetime_revenue.png
    ├── pareto_top_10_percent.png
    └── erd.png

```

---

# 🚀 Future Improvements

Potential extensions for deeper analysis:

- Cohort analysis
- Customer retention analysis
- Time-series revenue trends
- Profit margin trends by product category
- Integration with **Power BI or Tableau dashboards**

---

# 👨‍💻 Author

**Amit Kumar**  
Aspiring Data Analyst
