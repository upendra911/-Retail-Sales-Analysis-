# 🛍️ Retail Sales Analysis (SQL-Based Project)

This project presents a cleaned retail sales dataset analyzed using SQL Server Management Studio (SSMS). The goal is to extract meaningful insights from sales transactions by running a set of well-crafted SQL queries.

---

## 📁 Dataset Overview

The dataset includes retail transaction data with the following fields:

- `transactions_id` — Unique ID for each sale
- `sale_date` — Date of the sale
- `sale_time` — Time of the sale
- `customer_id` — Unique ID for each customer
- `gender` — Customer gender
- `age` — Customer age (nulls handled)
- `category` — Product category (Clothing, Beauty, Electronics)
- `quantity` — Units sold 
- `price_per_unit` — Selling price per item
- `cogs` — Cost of Goods Sold
- `total_sale` — Total revenue from the transaction

---

## 🧼 Data Cleaning

- Replaced null values in the `age` column using a default value.
- Removed rows containing null values in any other columns.

Final table name: **`sales`**

---

## 📊 Key SQL Queries & Insights

Here are 10 powerful SQL queries used to analyze the dataset:

| #  | Question                                       |
|----|------------------------------------------------|
| 1  | Total sales by category                        |
| 2  | Top 5 customers by total spend                 |
| 3  | Average age of customers by gender             |
| 4  | Monthly sales trend                            |
| 5  | Most sold product category (by quantity)       |
| 6  | Sales by time of day (morning/afternoon/etc.)  |
| 7  | Gender-wise sales distribution                 |
| 8  | Average price per unit by category             |
| 9  | High-value transactions (total sale > 1000)    |
| 10 | Profit per transaction (total_sale - cogs)     |

> ✅ All queries are written in standard **T-SQL** compatible with **SQL Server Management Studio**.

---

## 📂 Files in Repository

| File                     | Description                              |
|--------------------------|------------------------------------------|
| `cleaned_sales_data.csv` | The cleaned dataset                      |
| `SQL_Queries.sql`        | All 10 SQL queries                       |
| `query_outputs.xlsx`     | Query results for easy viewing           |
| `README.md`              | You are here                             |

---

## 🚀 How to Use

1. Clone or download the repository.
2. Import `cleaned_sales_data.csv` into your SQL Server environment.
3. Run `SQL_Queries.sql` in SSMS.
4. Explore results or use `query_outputs.xlsx` for quick insights.

---

## 📌 Tools Used

- SQL Server Management Studio (SSMS)
- Microsoft Excel (for output presentation)
- Python (optional for data prep)

---

## 🧠 Insights Gained

- Clothing is the top-selling category by both revenue and quantity.
- Sales are concentrated during morning hours.
- High-value transactions offer large profit margins.
- Female customers make up a significant portion of spending.

---

## 📬 Contact

Feel free to open issues or pull requests. For questions, reach out via GitHub Discussions or contact the project maintainer.

---
