# 🚀 Customer Revenue & RFM Analysis for E-commerce

## 📌 Overview
This project analyzes the **Online Retail dataset (541,909 transactions)** to understand customer purchasing behavior, revenue trends, top products, and high-value customers. It also prepares **RFM features** and a **future 90-day revenue target** for Customer Lifetime Value (CLV) analysis.

## 📈 Dataset
[!Dataset](https://www.kaggle.com/datasets/vijayuv/onlineretail)

---

## 🎯 Objectives
- Analyze customer and sales behavior
- Identify top products and countries
- Explore repeat customer patterns
- Create **Recency, Frequency, and Monetary (RFM)** features
- Prepare data for future CLV analysis

---

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