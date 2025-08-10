# dashboard-task3
# Retail Sales Performance Dashboard

## 📌 Project Overview
This project is part of **Task 4: Dashboard Design** for the Data Analyst Internship.  
The goal was to design an **interactive Power BI dashboard** using a retail transaction dataset to provide clear insights for business stakeholders.

---

## 📊 Dataset Information
**Dataset Name:** Retail Transaction Dataset  
**Columns:**
- CustomerID – Unique customer identifier
- ProductID – Unique product identifier
- Quantity – Number of units purchased
- Price – Price per unit
- TransactionDate – Date of transaction
- PaymentMethod – Mode of payment (Cash, Card, etc.)
- StoreLocation – Location of the store
- ProductCategory – Category of the product
- DiscountApplied(%) – Discount percentage applied
- TotalAmount – Total transaction amount

**Data Source:** Sample dataset from Kaggle (Retail Transactions)

---

## 🎯 KPIs Created
1. **Total Sales (₹)** – Total revenue generated from all transactions  
2. **Total Quantity Sold** – Sum of all product quantities sold  
3. **Total Customers** – Unique number of customers  
4. **Average Discount (%)** – Average discount applied across transactions  

---

# 📈 Dashboard Features
- **KPI Cards** displaying:
  - Total Sales
  - Total Quantity Sold
  - Total Customers
  - Average Discount
- **Visuals**:
  - Sales Trend Over Time (Line Chart)
  - Sales by Product Category (Bar Chart)
  - Payment Method Distribution (Donut Chart)
- **Slicers** for:
  - Date Range
  - Product Category
  - Payment Method
- **Consistent color theme** for professional presentation
- **Drill-down functionality** in time-based charts

---

## 🧮 Key DAX Measures
```DAX
-- Total Sales
Total Sales = SUM('Retail_Transaction_Dataset'[TotalAmount])

-- Total Quantity Sold
Total Quantity = SUM('Retail_Transaction_Dataset'[Quantity])

-- Total Customers
Total Customers = DISTINCTCOUNT('Retail_Transaction_Dataset'[CustomerID])

-- Average Discount
Average Discount = AVERAGE('Retail_Transaction_Dataset'[DiscountApplied(%)])
