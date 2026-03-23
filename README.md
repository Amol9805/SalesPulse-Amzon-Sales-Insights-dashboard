#  Amazon Sales Analysis Dashboard (MySQL, Power BI)

## 🔷 Project Overview

This project focuses on analyzing Amazon sales data across multiple branches to uncover insights related to **product performance, sales trends, customer behavior, and customer satisfaction**.

An **interactive Power BI dashboard** was developed using a structured **star schema model** and DAX measures to enable dynamic filtering, drill-down analysis, and business decision support.

---

## 🔷 Dataset Information

* **Total Records:** 1000 transactions
* **Branches:** Mandalay, Yangon, Naypyitaw
* **Columns:** 17

### Key Features:

* Sales & Financials → Total, VAT, COGS, Gross Income
* Customer Info → Customer Type, Gender
* Product Info → Product Line
* Time Info → Date, Time, Month, Day, Time of Day
* Feedback → Rating

---

## 🔷 Data Preparation

### ✔ Data Wrangling

* Checked for null values (none found)
* Ensured proper data types
* Cleaned and structured dataset

### ✔ Feature Engineering

* **timeofday** → Morning, Afternoon, Evening
* **dayname** → Day of week
* **monthname** → Month

---

## 🔷 Data Modeling (Star Schema)

### ⭐ Fact Table: `Fact_Sales`

Contains:

* Invoice ID, Product Line, Cust_ID
* Payment Method, Branch, 
* Quantity, Unit Price, Total, VAT, COGS, Gross Income
* Rating

###  Dimension Tables:

* `Dim_Product` → Product Line
* `Dim_Customer` → Customer Type, Gender, Cust_ID
* `Dim_Payment` → Payment Method
* `Dim_Location` → Branch, City
* `Dim_Date` → Date, Month, Day, Time of Day

---

## 🔷 Key Metrics (DAX)

* **Total Revenue** = SUM(total)
* **Total Orders** = DISTINCTCOUNT(invoice_id)
* **Total Quantity** = SUM(quantity)
* **Average Rating** = AVERAGE(rating)

---

#  Dashboard Pages & Visualizations

---

## 🟣 1. Product Line Analysis

This page focuses on identifying top-performing and underperforming product categories.

### Visuals Used:

* **Clustered Column Chart** → Top Performing Product Line (Revenue vs Product Line)
* **100% Stacked Column Chart** → Product Performance (Good vs Bad classification)
* **Clustered Bar Chart** → Average Rating by Product Line
* **Donut Chart** → VAT Contribution by Product Line

### Insights:

* Identifies highest revenue-generating product lines
* Compares product performance against average sales
* Evaluates product-wise customer satisfaction

### Screenshot/Demos:
* Example:  ![Dashboard Preview](https://github.com/Amol9805/Amzon-Sales-dashboard/blob/main/ProductionLine.png)
---

## 🟠 2. Sales Analysis

This page provides insights into overall sales performance and trends.

### Visuals Used:

* **Line Chart** → Monthly Revenue Trend
* **Clustered Column Chart** → COGS by Month
* **Clustered Bar Chart** → Revenue by City
* **Clustered Column Chart** → Sales by Time of Day
* **Matrix (Heatmap with Conditional Formatting)** → Sales by Day & Time

### Insights:

* Detects peak sales periods
* Identifies top-performing cities
* Analyzes time-based purchasing behavior

### Screenshot/Demos:
* Example:  ![Dashboard Preview](https://github.com/Amol9805/Amzon-Sales-dashboard/blob/main/ProductionLine.png)
---

## 🟢 3. Customer Analysis

This page focuses on customer segmentation and behavior.

### Visuals Used:

* **Donut Chart** → Revenue Contribution by Customer Type
* **Pie Chart** → Customer Distribution by Gender
* **Donut Chart** → Most Preferred Payment Method
* **Stacked Column Chart** → Gender Distribution Across Branches
* **Stacked Bar Chart** → Product Line Preferences by Gender
* **Clustered Bar Chart** → VAT Contribution by Customer Type

### Insights:

* Member customers contribute slightly higher revenue
* Balanced gender distribution across branches
* E-wallet and cash are dominant payment methods

### Screenshot/Demos:
* Example:  ![Dashboard Preview](https://github.com/Amol9805/Amzon-Sales-dashboard/blob/main/Customer.png)

---

## 🟡 4. Rating Analysis

This page analyzes customer satisfaction patterns.

### Visuals Used:

* **Clustered Column Chart** → Customer Ratings by Time of Day
* **Clustered Bar Chart** → Average Ratings by Day of Week
* **Stacked Column Chart** → Branch-wise Ratings by Time of Day
* **Clustered Bar Chart** → City-wise VAT Contribution

### Insights:

* Ratings are consistent across time periods
* Certain days show slightly higher customer satisfaction
* Branch-level rating variations highlight service differences

### Screenshot/Demos:
* Example:  ![Dashboard Preview](https://github.com/Amol9805/Amzon-Sales-dashboard/blob/main/ProductionLine.png)
---

## 🔷 Interactivity Features

* **Slicers:** Product Line, Customer Type, Gender, Payment Method, Month
* **Cross Filtering:** Interactive filtering across all visuals
* **Dynamic Dashboard:** Real-time insights based on selections

---

## 🔷 Key Business Insights

*  Food & Beverages and Sports categories are top performers
*  E-wallet and Cash are most preferred payment methods
*  Member customers generate higher revenue
*  Naypyitaw shows slightly higher VAT contribution
*  Sales are evenly distributed across time of day
*  Customer ratings remain stable (~7 avg), indicating consistent satisfaction

---

## 🔷 Tools & Technologies

* **Power BI** → Dashboard & Visualization
* **DAX** → Measures & Calculations
* **MySQL** → Data Preparation & Feature Engineering

---

## 🔷 Conclusion

This project demonstrates how Power BI can be used to transform raw sales data into meaningful insights through **data modeling, visualization, and interactivity**. The dashboard enables businesses to monitor performance, understand customer behavior, and optimize sales strategies.

---

## 🔷 Future Enhancements

* Predictive analytics (sales forecasting)
* Customer segmentation using ML models

---


