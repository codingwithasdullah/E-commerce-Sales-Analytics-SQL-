# E-commerce-Sales-Analytics-SQL-
Designed and implemented an E-commerce Sales Analytics database using SQL. Built tables for users, products, orders, payments, and reviews. Wrote queries to analyze best-selling products, revenue per category, and customer lifetime value, showcasing data-driven decision making.
# 🛒 E-commerce Sales Analytics (SQL Project)

## 📌 Project Overview
This project is a mini database design and analytics solution for an **E-commerce platform**.  
It helps to analyze **best-selling products, revenue per category, and customer lifetime value**.

## 📂 Database Schema
- **Users**: Stores customer details.  
- **Products**: Stores product details and category.  
- **Orders**: Stores purchase details (who bought what and when).  
- **Payments**: Stores transaction details.  
- **Reviews**: Stores customer feedback and ratings.

## ⚡ SQL Features Covered
✔ Database & Table Creation  
✔ Primary and Foreign Keys  
✔ Data Insertion  
✔ Aggregations (SUM, COUNT)  
✔ Joins (INNER JOIN)  
✔ Business Queries  

## 📊 Example Queries
### 1. Best-Selling Products
```sql
SELECT p.product_name, SUM(o.quantity) AS total_sold
FROM Orders o
JOIN Products p ON o.product_id = p.product_id
GROUP BY p.product_name
ORDER BY total_sold DESC
LIMIT 5;
