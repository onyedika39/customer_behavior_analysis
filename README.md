# **Customer Shopping Behavior Analysis**

## **1. Project Overview**

This project analyses customer shopping behavior using transactional data from **3,900 purchases** across multiple product categories.  
The goal is to identify trends in customer demographics, spending patterns, discount usage, product preferences, and subscription behavior to support data-driven business decisions.

This end-to-end project covers:  
**Python → EDA → Data Cleaning → SQL (Postgre) → KPI Analysis → Power BI Dashboard → Business Recommendations**

---

## **2. Dataset Summary**

- **Rows:** 3,900  
- **Columns:** 18  

### **Key Features Include:**
- **Customer demographics:** gender, age, age group, location, subscription status  
- **Purchase details:** item purchased, category, purchase amount, season, size, color  
- **Shopping behavior:** discount applied, promo code used, previous purchases, purchase frequency  
- **Product feedback:** review rating  
- **Logistics:** shipping type  

- **Missing Data:** 37 missing values found in `review_rating`

---

## **3. Exploratory Data Analysis (Python)**

Initial data preparation and cleaning were executed in Python using **pandas**.

### **Key Steps**

### ✔ Data Loading & Initial Exploration
- Loaded CSV into a pandas DataFrame  
- Used `df.info()` and `df.describe()` to understand dataset structure and distributions  

### ✔ Handling Missing Data
- Checked for null values in all columns  
- Imputed missing `review_rating` values using **median rating by product category**  

### ✔ Column Standardisation
- Renamed all columns to **snake_case** for readability and consistency  

### ✔ Feature Engineering
- Created `age_group` by binning customer ages  
- Generated `purchase_frequency_days` using purchase timestamps  
- Verified redundancy between `discount_applied` and `promo_code_used`  
- Dropped `promo_code_used` due to overlap  

### ✔ Database Integration
- Connected Python to **MySQL**  
- Loaded the cleaned DataFrame into MySQL for structured analytical querying  

---

## **4. Data Analysis using SQL (MySQL)**

A series of structured SQL queries were run to answer core business questions, including:

1. **Revenue by Gender** – Total revenue comparison between male and female customers  
2. **High-Spending Discount Users** – Identified customers who applied discounts yet exceeded average spend  
3. **Top 5 Products by Review Rating**  
4. **Shipping Comparison** – Average purchase amounts for Standard vs. Express shipping  
5. **Subscribers vs. Non-Subscribers** – Revenue and average spend by subscription status  
6. **Discount-Dependent Products** – Top 5 items with highest discount usage rate  
7. **Customer Segmentation** – Classified customers into **New**, **Returning**, and **Loyal**  
8. **Top 3 Products per Category** – Identified using window functions  
9. **Repeat Buyers & Subscription Likelihood** – Subscription patterns among customers with >5 purchases  
10. **Revenue by Age Group** – Identified high-value customer segments  

These MySQL queries validated insights discovered during Python EDA and added more focused business intelligence.

---

## **5. Dashboard in Power BI**

The interactive Power BI dashboard includes:

- Key KPIs (Total Revenue, AOV, Discount Usage %)  
- Revenue by age group, gender, and product category  
- Customer segmentation analysis  
- Product performance and review ratings  
- Shipping trends  
- Discount usage behaviour  

The dashboard is designed to be simple, intuitive, and stakeholder-friendly.

---

## **6. Key Insights**

- Customers aged **25–34** generate the highest revenue  
- Discount usage has a **strong positive effect** on purchase amount  
- Express shipping customers tend to spend more  
- Several high-selling products have **below-average review ratings**  
- Loyal customers contribute significantly to lifetime revenue  
- Subscribers show higher average order value than non-subscribers  

---

## **7. Business Recommendations**

### ✔ Boost Subscriptions
Introduce exclusive perks to encourage customers to subscribe.

### ✔ Customer Loyalty Program
Reward returning customers to increase the number of **Loyal** customers.

### ✔ Refine Discount Strategy
Use discounts strategically to boost conversions without hurting margins.

### ✔ Improve Low-Rated High-Demand Products
Investigate issues with heavily purchased but poorly rated items.

### ✔ Targeted Marketing Campaigns
Focus efforts on:
- Age group **25–34**  
- Express shipping users  
- Loyal customers  

---

## **8. Business Impact**

If implemented, these recommendations could lead to:

- Increased customer retention  
- Higher subscription rates  
- More effective marketing strategies  
- Improved product quality  
- Stronger long-term revenue growth  

---

## **9. What I Learned**

Through this project, I gained hands-on experience in:

- Python data cleaning & EDA  
- Feature engineering  
- Writing analytical SQL queries in MySQL  
- Customer segmentation and behavioural analysis  
- Power BI dashboard development  
- Translating insights into actionable business recommendations  
- Presenting data in a structured, stakeholder-friendly format  

---

## **10. Future Improvements**

- Add machine learning segmentation or churn prediction  
- Connect Power BI to a live SQL database  
- Perform sentiment analysis on review comments  
- Deploy a dashboard web app using Streamlit  
- Automate ETL workflows using Python  

---

## **11. Contact Details**

If you'd like to connect or have questions about this project:
 
- **Email:** *onyedikakenechukwu7@gmail.com*  
- **LinkedIn:** www.linkedin.com/in/onyedika-kenechukwu-3b3151309 

Feel free to reach out always happy to discuss data, analytics, and dashboards!

---
