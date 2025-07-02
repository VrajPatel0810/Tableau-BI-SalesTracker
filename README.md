
# 📊 End-to-End Sales Insights Project (SQL + Tableau)

This project is a comprehensive end-to-end business intelligence solution that analyzes retail sales data using **MySQL (SQL)** and visualizes key performance metrics using **Tableau dashboards**. It was completed in two distinct phases to reflect both independent analysis and stakeholder-driven improvements.

---

## 🚀 Project Overview

The aim was to simulate real-world business decision-making using data by creating dashboards that support revenue and profitability insights. The project includes:

- **Structured data ingestion using MySQL**
- **Custom SQL queries for insights**
- **Interactive Tableau dashboards for storytelling**
- **Stakeholder feedback loop for iterative development**

---

## 🔄 Two-Phase Workflow

### 🟦 Phase 1: Revenue Dashboard – Executive Overview

Built the initial dashboard focused on revenue metrics:

- Monthly revenue trends
- Currency-wise and market-wise sales
- Key revenue KPIs
- Dynamic filtering by region, year, currency

### 🟧 Phase 2: Profit Dashboard – Stakeholder-Informed Design

After gathering feedback, the second dashboard focused on deeper insights into profitability:

- Profit & profit margin metrics
- Region and product-level profit breakdown
- Monthly profitability trend
- Top performing products

These dashboards simulate an actual analyst-stakeholder collaboration loop.

---

## 🛠️ Tech Stack

- **SQL / MySQL** – Data querying and logic
- **Tableau** – Data visualization and dashboard design
- **Tableau Prep** *(optional)* – Minor data preparation
- **GitHub** – Version control and documentation

---

## 🗂️ Project Files

- `db_dump.sql`: MySQL database with sales data
- `Revenue.twb`: Tableau workbook for revenue insights (Phase 1)
- `Profit Analysis.twb`: Tableau workbook for profit insights (Phase 2)
- `README.md`: Project documentation

---

## 📦 How to Set Up the Project Locally

1. **Install MySQL** and import the `db_dump.sql` file:
    ```sql
    SOURCE path/to/db_dump.sql;
    ```
2. Open Tableau and connect to your local MySQL server.
3. Load the `.twb` files for interactive dashboards.
4. Explore filters, KPIs, and trends built into the dashboards.

---

## 🧠 SQL Data Exploration

Sample SQL queries used for analysis:

- **Show all customer records**
    ```sql
    SELECT * FROM customers;
    ```

- **Show distinct product codes sold in Chennai**
    ```sql
    SELECT DISTINCT product_code FROM transactions WHERE market_code='Mark001';
    ```

- **Revenue in 2020**
    ```sql
    SELECT SUM(transactions.sales_amount)
    FROM transactions
    INNER JOIN date ON transactions.order_date = date.date
    WHERE date.year = 2020
      AND (transactions.currency = 'INR' OR transactions.currency = 'USD');
    ```

- **Profit margin formula (used in Tableau):**
    ```
    Profit = sales_amount - cost
    Profit Margin = Profit / sales_amount
    ```

---

## ✅ Key Outcomes

- Developed two interactive Tableau dashboards with business KPIs
- Demonstrated SQL proficiency in extracting time-based and market-specific insights
- Applied stakeholder feedback to enhance dashboard usability
- Strengthened data storytelling and BI project lifecycle understanding

---

## 💼 Use Cases

- Executive reporting (high-level KPI tracking)
- Sales strategy optimization
- Regional performance analysis
- Product-level profitability monitoring

---
## Output
![image](https://github.com/user-attachments/assets/4909a332-f11e-417c-8d9c-5ebd627b447c)
![image](https://github.com/user-attachments/assets/27ba2794-b58d-4645-bd2f-e5a31072db40)


