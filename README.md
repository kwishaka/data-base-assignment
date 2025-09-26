# PL/SQL Window Functions – Ukwishaka Sandrine

## 📌 Business Problem
SmartMart, a retail company operating in Rwanda, wants to analyze sales performance across different regions.  
Managers need to identify top products per region, monitor monthly sales growth, classify customers into quartiles, and calculate moving averages for forecasting.

---

## 🗂️ Database Schema
We designed three related tables:

- **customers**(customer_id PK, customer_name, region)  
- **products**(product_id PK, product_name, category)  
- **transactions**(transaction_id PK, customer_id FK, product_id FK, sale_date, amount, total_price, order_number)

### ER Diagram
![ER Diagram](docs/er_diagram.png)

---

## 🎯 Success Criteria
1. **Top 5 products per region and quarter** → `RANK()`  
2. **Running monthly totals** → `SUM() OVER()`  
3. **Month-over-month growth** → `LAG()` / `LEAD()`  
4. **Customer quartiles** → `NTILE(4)`  
5. **3-month moving averages** → `AVG() OVER()`  

---

## ⚙️ SQL Scripts
Located in the `sql/` folder:

- `q1_top5_products.sql` → Top products by revenue per region/quarter  
- `q2_running_totals.sql` → Running monthly totals  
- `q3_mom_growth.sql` → Month-over-month growth (%)  
- `q4_customer_quartiles.sql` → Customer segmentation  
- `q5_moving_average.sql` → 3-month moving average  

---

## 📸 Screenshots
All screenshots are stored in the `screenshots/` folder.  
Examples:
- ![Top 5 Products](screenshots/q1_top5_products.png)  
- ![Running Totals](screenshots/q2_running_totals.png)  

---

## 📊 Results & Analysis

### Descriptive – What happened?
- Kigali region showed the highest sales, especially in beverages and electronics.  
- Top 5 products contributed over 40% of total revenue in each quarter.  

### Diagnostic – Why?
- Seasonal promotions in Q3 boosted beverage sales.  
- High-value customers (quartile 1) are responsible for most revenue, showing dependence on a small customer group.  

### Prescriptive – What next?
- Target quartile 2–3 customers with promotions to move them into higher spending groups.  
- Use 3-month moving averages for better inventory forecasting.  
- Expand product promotions beyond Kigali to balance regional sales.  

---

## 🛠️ How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/plsql-window-functions-ukwishaka-sandrine.git
