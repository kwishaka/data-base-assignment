   Ukwishaka Sandrine

 Business Problem
SmartMart, a retail company operating in Rwanda, wants to analyze sales performance across different regions.  
Managers need to identify top products per region, monitor monthly sales growth, classify customers into quartiles, and calculate moving averages for forecasting.

---

 🗂️ Database Schema
We designed three related tables:

- customers(customer_id PK, customer_name, region)  
- products(product_id PK, product_name, category)  
- transactions(transaction_id PK, customer_id FK, product_id FK, sale_date, amount, total_price, order_number
![Alt text](C:\Users\HP\OneDrive\Desktop\screenshot/to/<img width="471" height="301" alt="customers" src="https://github.com/user-attachments/assets/2d33a437-af19-4544-b733-06a1e64ae86b" />
)![Alt text]C:\Users\HP\OneDrive\Desktop\screenshot(/to/<img width="437" height="227" alt="product" src="https://github.com/user-attachments/assets/c0fef379-dfc6-4668-aee5-1718ab67af66" />
)
![Alt text](C:\Users\HP\OneDrive\Desktop\screenshot/to/<img width="898" height="353" alt="transactions" src="https://github.com/user-attachments/assets/8ec6e828-b755-4563-9d71-0edf112c300b" />
)

---

 Success Criteria
1. Top 5 products per region and quarter** → `RANK()` ![Alt text](C:\Users\HP\OneDrive\Desktop\screenshot/to/<img width="938" height="538" alt="ranks" src="https://github.com/user-attachments/assets/aeb63015-99c4-4b37-b23c-510f84c6dd60" />
)
2.  
3. Running monthl!
4. [Alt text](C:\Users\HP\OneDrive\Desktop\screenshot/to/<img width="947" height="570" alt="runnings" src="https://github.com/user-attachments/assets/4504dfd0-bfd0-4ae1-a285-dec4240ac0aa" />
)
y totals** → `SUM() OVER()`
5. ![Alt text](C:\Users\HP\OneDrive\Desktop\screenshot/to/<img width="793" height="547" alt="moving average" src="https://github.com/user-attachments/assets/df5ab9bc-4a0c-471e-813b-a602a3449371" />
)
6. Month-over-month growth** → `LAG()` / `LEAD()`
7.   ![Alt text<img width="997" height="544" alt="month growth" src="https://github.com/user-attachments/assets/8b872c11-1985-4ecb-bc60-8b3c095f2295" />
](/to/image.png)

8. Customer quartiles** → `NTILE(4)`
9. ![Alt text](/to/)<img width="838" height="484" alt="quatieles" src="https://github.com/user-attachments/assets/6299feb1-9132-4e62-8039-16f2a4c50524" />


10. 3-month moving averages** →
11. ![Alt text](/C:\Users\HP\OneDrive\Desktop\screenshotto/<img width="793" height="547" alt="moving average" src="https://github.com/user-attachments/assets/8b91234b-aa12-46c6-8b82-b0cca4ad34ea" />
)

12.
13. ![Alt text](C:\Users\HP\OneDrive\Desktop\screenshot/to/<img width="793" height="547" alt="moving average" src="https://github.com/user-attachments/assets/a9db626a-cede-4993-a966-d7484896b566" />
)



---



 Top products by revenue per region/quarter  
 Running monthly totals  
 Month-over-month growth (%)  
 Customer segmentation  
 3-month moving average  

---

 Analysis

# Descriptive – What happened?
- Kigali region showed the highest sales, especially in beverages and electronics.  
- Top 5 products contributed over 40% of total revenue in each quarter.  
becouse
- Seasonal promotions in Q3 boosted beverage sales.  
- High-value customers (quartile 1) are responsible for most revenue, showing dependence on a small customer group.  

this will read to
- Target quartile 2–3 customers with promotions to move them into higher spending groups.  
- Use 3-month moving averages for better inventory forecasting.  
- Expand product promotions beyond Kigali to balance regional sales.  

---

