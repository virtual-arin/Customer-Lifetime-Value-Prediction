# 🚀 Customer Revenue & RFM Analysis for E-commerce

## 📌 Overview
This project analyzes the **Online Retail dataset (541,909 transactions)** to understand customer purchasing behavior, revenue trends, top products, and high-value customers. It also prepares **RFM features** and a **future 90-day revenue target** for Customer Lifetime Value (CLV) analysis.

## 📈 Dataset
![Dataset](https://www.kaggle.com/datasets/vijayuv/onlineretail)

---

## 🎯 Objectives
- Analyze customer and sales behavior
- Identify top products and countries
- Explore repeat customer patterns
- Create **Recency, Frequency, and Monetary (RFM)** features
- Prepare data for future CLV analysis

---

1. What is the distribution of cancelled invoices?

![Cancelled invoices](https://github.com/virtual-arin/Customer-Lifetime-Value-Prediction/blob/main/images/cancelled_invoices.png)

**The data has 9288 cancelled invoices**

2. How has revenue changed over time?

![Total revenue over time](https://github.com/virtual-arin/Customer-Lifetime-Value-Prediction/blob/main/images/total_revenue_over_time.png)

**Revenue remains relatively stable until getting a massive spike**

3. Which top 10 countries generate the most revenue?

![Top revenue generating countries](https://github.com/virtual-arin/Customer-Lifetime-Value-Prediction/blob/main/images/top_10_revenue_countries.png)

**United Kingdom generates the highest revenue**

4. Which products generate the highest revenue?

![Top revenue generating products](https://github.com/virtual-arin/Customer-Lifetime-Value-Prediction/blob/main/images/top_products_by_revenue.png)

**The paper craft little birdie generates the highest revenue.**

5. Which products are sold the most (by quantity)?

![Top products by quantity sold](https://github.com/virtual-arin/Customer-Lifetime-Value-Prediction/blob/main/images/top_products_by_quantity_sold.png)

**PAPER CRAFT , LITTLE BIRDIE and MEDIUM CERAMIC TOP STORAGE JAR are sold the most.**

6. Which month has the highest revenue?

![Monthly Revenue](https://github.com/virtual-arin/Customer-Lifetime-Value-Prediction/blob/main/images/monthly_revenue.png)

**Overall monthly revenue steadily increases before peaking in November.**

7. Which weekday performs best?

![Revenue share by weekday](https://github.com/virtual-arin/Customer-Lifetime-Value-Prediction/blob/main/images/revenue_share_by_weekday.png)

**Thursday and Tuesday generate the largest shares of revenue**

8. How many products are usually bought in an order?

![Item per order](https://github.com/virtual-arin/Customer-Lifetime-Value-Prediction/blob/main/images/items_per_order.png)

**Order quantities are usually low but feature extreme outliers.**

9. Who are the top customers by revenue?

![Customer by revenue](https://github.com/virtual-arin/Customer-Lifetime-Value-Prediction/blob/main/images/customers_by_revenue.png)

**Customer with CustomerID (14646.0) is the top customer**

10. How many repeat vs one-time customers are there?

![Repeat vs Onetime](https://github.com/virtual-arin/Customer-Lifetime-Value-Prediction/blob/main/images/repeat_vs_onetime_customers.png)

**The data shows 65.6% Repeat customers and 34.4% One time customers.**

11. Which numerical features have the strongest relationship with TotalPrice, and what does that tell us about customer spending?

![Heatmap](https://github.com/virtual-arin/Customer-Lifetime-Value-Prediction/blob/main/images/correlation_heatmap.png)

**The plot shows a strong positive correlation of 0.91 between Quantity and TotalPrice, with other features showing near zero correlation to each other.**

12. How is CLV distributed across customers?

![CLV Distribution](https://github.com/virtual-arin/Customer-Lifetime-Value-Prediction/blob/main/images/clv_distribution.png)

**The customer lifetime value distribution is highly right-skewed, showing that the majority of customers generate low value, leaving few high value outliers.**

13. Which numerical features have the strongest relationship with CLV?

!(CLV Heatmap)(https://github.com/virtual-arin/Customer-Lifetime-Value-Prediction/blob/main/images/correlation_heatmap2.png)

**Monetary value and CLV show the strongest positive correlation at 0.65, meaning that higher spending strongly predicts a greater overall customer lifetime value.**

## 🧹 Data Preprocessing
- Removed cancelled invoices
- Removed invalid quantity and price values
- Dropped missing `CustomerID`
- Handled missing descriptions
- Created `TotalPrice = Quantity × UnitPrice`

---

## 📊 Analysis Performed
- Monthly revenue trend
- Top-selling products
- Highest revenue products
- Revenue by country
- Weekday sales analysis
- Repeat vs one-time customers
- Correlation analysis

---

## 🛠️ Tech Stack
- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

---

## 📈 Key Insights
- A small group of customers contributes most of the revenue.
- Repeat customers generate higher revenue than one-time buyers.
- Sales show clear seasonal patterns.
- The UK contributes the majority of sales revenue.

---

## 🔮 Future Improvements
- Add RFM customer segmentation
- Build an interactive Power BI/Tableau dashboard
- Train a machine learning model for CLV prediction
- Deploy the analysis as a web application