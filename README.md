# 🛒 Customer Shopping Behavior Analysis

<p align="center">
  <img src="assets/cover.png" alt="Project Cover" width="800">
</p>

## 📘 Project Overview
This project analyzes **customer shopping behavior** using transactional data from **3,900 purchases** across various product categories.  
The primary goal is to uncover insights into:
- Spending patterns  
- Customer segments  
- Product preferences  
- Subscription behavior  

These insights aim to guide **data-driven business decisions** and improve marketing, sales, and customer retention strategies.

---

## 🧾 Dataset Summary
- **Rows:** 3,900  
- **Columns:** 18  

### Key Features
- **Customer Demographics:** Age, Gender, Location, Subscription Status  
- **Purchase Details:** Item Purchased, Category, Purchase Amount, Season, Size, Color  
- **Shopping Behavior:** Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type  
- **Missing Data:** 37 missing values in `Review Rating` column

---

## 🐍 Exploratory Data Analysis (Python)
Performed initial data preparation and cleaning using **Python (pandas, numpy, matplotlib, seaborn)**.

### Steps:
- **Data Loading:** Imported dataset using `pandas`.  
- **Exploration:** Used `df.info()` and `df.describe()` for structure and statistics.  
- **Missing Data:** Imputed missing `review_rating` values using the **median rating per product category**.  
- **Column Standardization:** Converted column names to `snake_case`.  
- **Feature Engineering:**
  - Created `age_group` by binning customer ages.
  - Derived `purchase_frequency_days` from timestamps.
- **Redundancy Check:** Verified that `discount_applied` and `promo_code_used` were overlapping; dropped the latter.  
- **Database Integration:** Loaded the cleaned DataFrame into **PostgreSQL** for SQL-based business analysis.

---

## 🧮 Data Analysis (PostgreSQL)
Conducted structured SQL queries to extract key business insights.

### Key Analyses
1. **Revenue by Gender** – Compared total revenue by male vs. female customers.  
2. **High-Spending Discount Users** – Identified customers who used discounts but spent above average.  
3. **Top 5 Products by Rating** – Found products with the highest average review ratings.  
4. **Shipping Type Comparison** – Compared average purchase amounts for Standard vs. Express shipping.  
5. **Subscribers vs. Non-Subscribers** – Analyzed revenue and average spending differences.  
6. **Discount-Dependent Products** – Identified top 5 products with highest discount purchase ratios.  
7. **Customer Segmentation** – Classified customers into New, Returning, and Loyal categories.  
8. **Top 3 Products per Category** – Determined top-selling products within each category.  
9. **Repeat Buyers & Subscriptions** – Checked correlation between purchase frequency and subscription likelihood.  
10. **Revenue by Age Group** – Calculated revenue contribution by age segment.

---

## 📊 Dashboard (Power BI)
An **interactive Power BI dashboard** was created to visualize:
- Total revenue trends  
- Customer segmentation  
- Product category performance  
- Subscription behavior  
- Shipping preferences  

The dashboard enables stakeholders to interactively explore KPIs and insights derived from Python and SQL analyses.

---

## 💡 Business Recommendations
Based on the findings, several strategic recommendations were made:

1. **Boost Subscriptions** – Promote exclusive benefits to increase subscription conversions.  
2. **Customer Loyalty Programs** – Reward frequent buyers to transition them into the “Loyal” segment.  
3. **Review Discount Policy** – Balance between sales uplift and margin control.  
4. **Product Positioning** – Highlight top-rated and best-selling products in marketing campaigns.  
5. **Targeted Marketing** – Focus efforts on high-revenue age groups and Express-shipping customers.

---

## ⚙️ Tech Stack
| Tool | Purpose |
|------|----------|
| **Python (pandas, numpy, seaborn, matplotlib)** | Data cleaning, preprocessing, and EDA |
| **PostgreSQL** | Business analysis through SQL queries |
| **Power BI** | Interactive dashboard and visualization |
| **GitHub** | Version control and project documentation |

---

## 🚀 How to Run the Project
1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/customer-shopping-behavior.git
   cd customer-shopping-behavior
