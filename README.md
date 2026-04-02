# 🛒 Customer Purchase Behaviour Analysis

## 📌 Project Overview
Analyzed 3,900 customer transactions across product categories to uncover 
insights into spending patterns, customer segments, product preferences, 
and subscription behavior using Python, MySQL, and Power BI.

---

## 📊 Dataset Summary
- **Rows:** 3,900 | **Columns:** 18
- **Key Features:** Customer demographics, purchase details, 
  shopping behavior (discounts, shipping, subscriptions)
- **Missing Data:** 37 values in Review Rating — imputed using 
  category-wise median

---

## ⚙️ Tools & Technologies
| Tool | Usage |
|------|-------|
| Python (Pandas, NumPy) | Data cleaning & EDA |
| SQLAlchemy + PyMySQL | Python → MySQL connection |
| MySQL | Business SQL queries |
| Power BI | Interactive dashboard |

---

## 🔧 Data Processing Steps (Python)
- Loaded dataset using `pd.read_csv()`
- Handled 37 missing values in `Review Rating` using 
  **category-wise median** via `groupby().transform()`
- Renamed columns to **snake_case** for consistency
- **Feature Engineering:**
  - Created `age_group` column using `pd.qcut()` 
    (Young Adult / Adult / Middle Aged / Senior)
  - Created `purchase_frequency_days` column from frequency labels
- Verified `discount_applied` and `promo_code_used` were identical — 
  dropped `promo_code_used`
- Connected Python to **MySQL** using SQLAlchemy and loaded 
  cleaned data into `customer_behavior` database

---

## 🗄️ SQL Business Questions Answered (11 Queries)

| # | Question |
|---|----------|
| Q1 | Total revenue by Male vs Female customers |
| Q2 | Customers who used discount but spent above average |
| Q3 | Top 5 products by average review rating |
| Q4 | Average purchase amount: Standard vs Express shipping |
| Q5 | Subscriber vs Non-subscriber spend comparison |
| Q6 | Top 5 products with highest discount usage % |
| Q7 | Customer segmentation: New / Returning / Loyal (CTE + CASE) |
| Q8 | Top 3 categories by total products purchased |
| Q9 | Top 3 products within each category (Window Function) |
| Q10 | Repeat buyers (>5 purchases) vs subscription status |
| Q11 | Revenue contribution by age group |

---

## 📈 Key SQL Insights
- **Male customers** generated **₹1,57,890** vs Female **₹75,191**
- **839 customers** used discounts but still spent above average
- **Loyal customers: 3,116** | Returning: 701 | New: 83
- **Young Adults** are the highest revenue age group — ₹62,143
- **Express shipping** users spend slightly more ($60.48) 
  vs Standard ($58.46)
- Top discount-dependent product: **Hat** (50% discount rate)

---

## 📊 Power BI Dashboard
Built an interactive dashboard showing:
- KPIs: 3.9K Customers | $59.76 Avg Purchase | 3.75 Avg Rating
- Revenue by Category & Age Group
- Sales by Category
- Subscription Status Distribution (27% Yes | 73% No)
- Filters: Gender, Category, Shipping Type, Subscription

---

## 💡 Business Recommendations
- **Boost Subscriptions** — Promote exclusive subscriber benefits
- **Loyalty Programs** — Reward repeat buyers to retain "Loyal" segment
- **Review Discount Policy** — Balance sales boost vs margin control
- **Product Positioning** — Highlight Gloves, Sandals, Boots (top rated)
- **Targeted Marketing** — Focus on Young Adults (highest revenue group)

---

## 👤 Author
**Aditya Kumar**  
Data Analyst | [GitHub](https://github.com/adityak024)
```
