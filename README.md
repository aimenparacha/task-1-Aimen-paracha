#  E-Commerce Exploratory Data Analysis (EDA)

> DecodeLabs Industrial Training Kit · Batch 2026 · Project 2

A comprehensive Exploratory Data Analysis (EDA) project performed on a real-world e-commerce dataset containing **1,200 customer transactions** spanning **January 2023 to June 2025**.

This project focuses on uncovering hidden business insights, identifying operational inefficiencies, analyzing revenue trends, and understanding customer purchasing behavior using statistical and visual analysis techniques.



#  Project Objectives

- Analyze customer purchasing behavior
- Identify revenue trends and seasonal patterns
- Detect operational inefficiencies
- Discover key revenue-driving factors
- Evaluate customer acquisition channels
- Perform statistical and correlation analysis


#  Executive Summary

### Key Business Insights

- 41.4% of orders were either cancelled or returned
- Revenue distribution is heavily right-skewed
- Instagram generated the highest customer referrals
- Premium products had the strongest impact on revenue
- Revenue consistently peaked during June
- CouponCode data contained 25.75% missing values



#  Dataset Description

| Field | Type | Description |
|---|---|---|
| OrderID | String | Unique order identifier |
| Date | DateTime | Order date |
| CustomerID | String | Unique customer identifier |
| Product | Categorical | Product category |
| Quantity | Integer | Units ordered |
| UnitPrice | Float | Price per unit |
| PaymentMethod | Categorical | Payment method used |
| OrderStatus | Categorical | Delivery status |
| ItemsInCart | Integer | Items browsed before purchase |
| CouponCode | Categorical | Discount code used |
| ReferralSource | Categorical | Customer acquisition source |
| TotalPrice | Float | Final order value |

### Dataset Information

- **Rows:** 1,200
- **Columns:** 14
- **Time Period:** Jan 2023 – Jun 2025
- **Missing Data:** CouponCode column (25.75%)



#  Analysis Performed

## 1. Descriptive Statistics

- Mean, Median, Standard Deviation
- Minimum & Maximum values
- Five-number summary
- Distribution analysis

### Observation
The `TotalPrice` column showed a right-skewed distribution:

- Mean: **$1,054**
- Median: **$824**

This indicates the presence of high-value transactions influencing the average.



## 2. Distribution Analysis

Performed frequency analysis on:

- Product categories
- Payment methods
- Referral sources
- Order statuses
- Quantity purchased

### Key Observation
Only **19.2%** of orders were successfully delivered, indicating potential operational issues.



## 3. Outlier Detection (IQR Method)

### Statistical Values

- Q1 = $410.52
- Q3 = $1,578.48
- IQR = $1,167.95
- Upper Fence = $3,330.41

### Result
8 outliers were detected and verified as legitimate premium transactions rather than data errors.


## 4. Trend Analysis

Monthly revenue trends were analyzed across 30 months.

### Revenue Peaks

- June 2024 → **$68,069**
- May 2023 → **$63,837**

### Seasonal Insight
Revenue consistently dipped during April and peaked during June.



## 5. Correlation Analysis (Pearson Correlation)

| Relationship | Correlation (r) | Strength |
|---|---|---|
| UnitPrice → TotalPrice | 0.717 | Strong |
| Quantity → TotalPrice | 0.615 | Moderate |
| ItemsInCart → Quantity | 0.650 | Moderate |
| ItemsInCart → TotalPrice | 0.393 | Weak |

### Key Insight
`UnitPrice` was identified as the strongest revenue predictor.


# Key Findings

##  Operational Fulfilment Gap
41.4% of orders were cancelled or returned, representing a major operational risk.

##  Revenue Distribution
Revenue is significantly right-skewed, meaning average-based strategies may not accurately represent customer behavior.

##  Best Acquisition Source
Instagram generated the highest number of customer referrals.

##  Premium Products Drive Revenue
Higher-priced products contributed most strongly to overall revenue growth.

##  Seasonal Trends
Revenue consistently increased during June, suggesting recurring seasonal demand.

##  Missing Discount Data
CouponCode contained 25.75% missing values, limiting discount attribution analysis.



#  Recommendations

| Priority | Recommendation | Expected Impact |
|---|---|---|
| High | Investigate cancellation & return causes | Revenue recovery |
| High | Fix CouponCode data pipeline | Better discount analysis |
| Medium | Segment customers by AOV | Targeted marketing |
| Medium | Launch June marketing campaigns earlier | Revenue amplification |
| Low | Measure referral-source ROI | Budget optimization |


#  Tools & Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Chart.js**
- **HTML/CSS**
- **Excel**

#  EDA Concepts Applied

- Descriptive Statistics
- Univariate Analysis
- Distribution Analysis
- Outlier Detection (IQR)
- Correlation Analysis
- Time-Series Trend Analysis
- Missing Value Analysis


├── Dataset_for_Data_Analytics.xlsx
├── README.md
└── screenshots/
