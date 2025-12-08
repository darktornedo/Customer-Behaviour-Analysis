# 🧠 Customer Behaviour & Churn Analysis (Python + Power BI)

---

## 📝 Project Overview
This project analyzes customer behaviour for an e-commerce platform using Python for in-depth Exploratory Data Analysis (EDA) and Power BI for an interactive Customer Churn & Retention Dashboard.

The dataset consists of 250,000 records and originally 13 columns, later expanded to 18 columns with additional engineered fields such as:
```
customer_id
price
quantity
gender
churn
age
return
product_category
payment_method
```

The main objective is to:
- Understand who the customers are (demographics & purchasing patterns)
- Analyze what they buy and how they pay
- Identify drivers of churn and retention behaviour
- Build a dashboard that helps businesses monitor churn and customer value over time

---

## ⚙️ Tech Stack
### 🔹 Python (EDA & Data Preparation)
- Jupyter Notebook
- NumPy – numerical computations
- Pandas – data cleaning, feature engineering & aggregation
- Matplotlib & Seaborn – visual analytics

### 🔹 Power BI (Dashboard & Business View)
- Data import from cleaned CSV
- DAX measures for KPIs (churn rate, CLV, revenue, repeat rate, etc.)
- Interactive visuals: churn trends, segmentation, cohorts, retention & CLV

--- 

## 🧹 Data Preparation & Feature Engineering
### 1. Data Import & Overview (Python)
- Loaded dataset (250k rows × 13 columns) into Pandas.
- Inspected data types, structure, and missing values.

### 2. Data Cleaning (Python)
- Removed duplicate records.
- Handled missing values where necessary.
- Standardized column names and formats.
- Converted purchase_date to proper datetime type.

### 3. Feature Engineering (Python)
- Created order_value = product_price × quantity.
- Derived time-based features: year, month, day_name.
- Created age_group buckets (e.g., 18–25, 26–35, 36–50, 50+).
- Generated churn flag (churn) to classify customers as Churned or Active.
- Built cohort features:
   ```
   cohort_month – month of first purchase per customer
   cohort_index – months since cohort start (for retention analysis)
   ```
The cleaned and enriched dataset (now 18 columns) was exported as a CSV and used as the source file for Power BI.

---

## 🔍 EDA Workflow (Python)
### 1. Data Exploration
- Summary statistics for numerical features (price, quantity, order value, age).
- Value counts for categorical features (product_category, payment_method, gender, returns, churn).

### 2. Univariate Analysis
- Distribution of customer age, order value, and quantity.
- Count plots for gender, product_category, payment_method, returns, and churn.

### 3. Bivariate Analysis
- Gender vs Churn – checked if churn behaviour differs by gender.
- Age Group vs Churn – identified the most churn-prone age segments.
- Product Category vs Order Value – which categories drive more revenue.
- Payment Method vs Frequency – preferred methods and their volume.
- Correlation heatmap for numeric features to detect relationships.

### 4. Outlier Detection
- Use IQR Method to detect anomalies in product_price, quantity, and order_value.

### 5. Churn Behaviour Analysis
- Compared spending patterns of churned vs retained customers.
- Analyzed return behaviour and its impact on churn.
- Investigated how engagement (number of orders) differs between active and churned users.

--- 

## 📊 Power BI Workflow
### 1. Data Import & Modeling
- Loaded enriched CSV into Power BI.
- Created necessary relationships and cleaned data view.

### 2. DAX Measures (KPIs)
#### Created measures for:
- Total Customers
- Active & Churned Customers
- Churn Rate
- Total Revenue & Revenue Lost to Churn
- Average Order Value (AOV)
- Customer Lifetime Value (CLV)
- Repeat Purchase Rate
- Cohort Retention & Purchase Frequency

### 3. Dashboard Development Process
- Designed a 2-page interactive dashboard:
  -Page 1: High-level churn overview
  -Page 2: Retention, cohorts & customer lifetime value
- Added slicers for advanced filtering (date, age group, category, etc.).
- Applied a clean layout and consistent color theme.

---

## 🖼️ Dashboard Preview
### 📌 Page 1 – Customer Churn Analysis

![Churn Overview](Customer_dashboard_page1.jpg)

### 📌 Page 2 – Customer Risk Analysis

![Customer Retention](Customer_dashboard_page2.jpg)

---

## 📈 Key Insights
### From the combined Python EDA + Power BI dashboard, some major insights include:
- Top Product Categories: Electronics and Home products show the highest purchase volume and revenue contribution.
- Payment Behaviour: Credit Card and PayPal are the dominant payment methods among customers.
- Customer Demographics: The majority of customers fall in the 25–45 age range, making it the most active spending group.
- Returns & Churn: Customers with frequent returns exhibit a higher churn probability, suggesting dissatisfaction or expectation mismatch.
- Churn Behaviour:
  - Loyal customers tend to make frequent, moderate-value purchases across multiple categories.
  - Churned customers typically show inconsistent engagement, fewer orders, and a higher tendency to return products.
- Retention Patterns (Cohorts): Cohort analysis revealed that a significant portion of customers stop purchasing after a few months, indicating opportunities for targeted re-engagement campaigns early in the customer lifecycle.

---

## 💡 Conclusion
### This project demonstrates a complete analytics workflow:
- Python EDA for deep data understanding, cleaning, and feature engineering.
- Power BI dashboard for turning analysis into an interactive, business-friendly product.
- It provides decision-makers with:
- Clear visibility into who is churning,
- Understanding of why they churn, and
- Insights on how to improve retention and revenue through better targeting and experience management.
- For an aspiring Data Analyst, this project showcases:
- Strong EDA capabilities (Python)
- Practical feature engineering
- Business-oriented dashboard design (Power BI)
- Ability to translate data into actionable insights

---

## 👩‍💻 Author
**Kumkum Pal**
