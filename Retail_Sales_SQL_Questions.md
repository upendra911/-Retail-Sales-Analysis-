
# 📘 SQL Questions for Retail Sales Analysis

Below are 10 essential SQL queries used to analyze the `sales` table from a cleaned retail dataset. These queries are written for use in **SQL Server Management Studio (SSMS)**.

---

### 🔹 Q1. Total Sales by Category

```sql
SELECT category, SUM(total_sale) AS total_sales
FROM sales
GROUP BY category
ORDER BY total_sales DESC;
```

📷 *Output Screenshot:*  
![Q1 Output](screenshots/q1_output.png)

---

### 🔹 Q2. Top 5 Customers by Total Spend

```sql
SELECT TOP 5 customer_id, SUM(total_sale) AS total_spent
FROM sales
GROUP BY customer_id
ORDER BY total_spent DESC;
```

📷 *Output Screenshot:*  
![Q2 Output](screenshots/q2_output.png)

---

### 🔹 Q3. Average Age of Customers by Gender

```sql
SELECT gender, AVG(age) AS avg_age
FROM sales
GROUP BY gender;
```

📷 *Output Screenshot:*  
![Q3 Output](screenshots/q3_output.png)

---

### 🔹 Q4. Monthly Sales Trend

```sql
SELECT FORMAT(sale_date, 'yyyy-MM') AS sale_month, SUM(total_sale) AS monthly_sales
FROM sales
GROUP BY FORMAT(sale_date, 'yyyy-MM')
ORDER BY sale_month;
```

📷 *Output Screenshot:*  
![Q4 Output](screenshots/q4_output.png)

---

### 🔹 Q5. Most Sold Product Category (by Quantity)

```sql
SELECT category, SUM(quantity) AS total_quantity
FROM sales
GROUP BY category
ORDER BY total_quantity DESC;
```

📷 *Output Screenshot:*  
![Q5 Output](screenshots/q5_output.png)

---

### 🔹 Q6. Sales by Time of Day (Morning, Afternoon, Evening)

```sql
SELECT 
    CASE 
        WHEN DATEPART(HOUR, sale_time) < 12 THEN 'Morning'
        WHEN DATEPART(HOUR, sale_time) < 17 THEN 'Afternoon'
        ELSE 'Evening'
    END AS time_of_day,
    SUM(total_sale) AS total_sales
FROM sales
GROUP BY 
    CASE 
        WHEN DATEPART(HOUR, sale_time) < 12 THEN 'Morning'
        WHEN DATEPART(HOUR, sale_time) < 17 THEN 'Afternoon'
        ELSE 'Evening'
    END;
```

📷 *Output Screenshot:*  
![Q6 Output](screenshots/q6_output.png)

---

### 🔹 Q7. Gender-wise Sales Distribution

```sql
SELECT gender, SUM(total_sale) AS total_sales
FROM sales
GROUP BY gender;
```

📷 *Output Screenshot:*  
![Q7 Output](screenshots/q7_output.png)

---

### 🔹 Q8. Average Price per Unit by Category

```sql
SELECT category, AVG(price_per_unit) AS avg_price
FROM sales
GROUP BY category;
```

📷 *Output Screenshot:*  
![Q8 Output](screenshots/q8_output.png)

---

### 🔹 Q9. High-Value Transactions (Total Sale > 1000)

```sql
SELECT * 
FROM sales
WHERE total_sale > 1000;
```

📷 *Output Screenshot:*  
![Q9 Output](screenshots/q9_output.png)

---

### 🔹 Q10. Profit Calculation (Total Sale - COGS)

```sql
SELECT 
    transactions_id,
    total_sale,
    cogs,
    (total_sale - cogs) AS profit
FROM sales;
```

📷 *Output Screenshot:*  
![Q10 Output]("C:\Users\uppi2\OneDrive\Pictures\Screenshots\Screenshot 2025-04-30 204636.png")

---

📁 **Tip:** Place the screenshots inside a `screenshots/` folder in your repo and ensure the image paths match the file names.
