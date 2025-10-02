# 🛍️ Task 7 - Sales Summary using Python & SQLite

This project is part of my **Data Analyst Internship - Task 7**.  
The objective is to create a small SQLite database, query sales information using Python, and visualize the results with a bar chart.

---

## 📌 Objective
- Use **SQLite** inside Python to analyze sales data.
- Get a **basic sales summary**:
  - Total quantity sold per product
  - Total revenue per product
  - Overall totals
- Display results using **print statements** and a **bar chart**.

---

## 🛠 Tools & Libraries
- **Python 3**
- **SQLite3** (built-in with Python)
- **pandas**
- **matplotlib**

---
---

## 📊 Steps Performed
1. **Created SQLite database** `sales_data.db` with a `sales` table.
2. **Inserted sample sales data** (Shoes, T-shirt, Jeans, Cap).
3. **Queried sales summary by product** using SQL:
   ```sql
   SELECT product,
          SUM(quantity) AS total_qty,
          SUM(quantity * price) AS revenue
   FROM sales
   GROUP BY product;
