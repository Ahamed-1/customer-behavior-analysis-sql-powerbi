# Customer Shopping Behavior Analysis

An end-to-end data analytics portfolio project analyzing retail customer shopping behavior using Python, SQL, and Power BI.

## Project Overview

This project explores transactional data from 3,900 retail purchases to uncover insights into customer spending patterns, product preferences, discount behavior, and subscription trends — the kind of analysis a data analyst would be expected to deliver in a real business setting.

**Core Business Question:** How can a retail company use customer shopping data to improve engagement, optimize marketing, and drive revenue?

## Tools & Technologies

- **Python (Google Colab)** — Data cleaning, EDA, feature engineering
- **PostgreSQL** — Structured querying and business analysis
- **Power BI** — Interactive dashboard and visual storytelling

## What I Did

### 1. Data Preparation (Python)
- Loaded and explored the raw dataset using pandas
- Handled 37 missing values in the `review_rating` column by imputing with category-level medians
- Renamed columns to snake_case for consistency
- Engineered two new features: `age_group` (binned from age) and `purchase_frequency_days`
- Verified that `discount_applied` and `promo_code_used` were redundant and dropped the latter
- Exported the cleaned data into PostgreSQL for SQL analysis

### 2. Data Analysis (SQL)

Wrote 10 business-driven SQL queries covering:

| # | Business Question |
|---|---|
| 1 | Total revenue by gender |
| 2 | High-spending customers who still used discounts |
| 3 | Top 5 products by average review rating |
| 4 | Average spend: Standard vs Express shipping |
| 5 | Subscriber vs non-subscriber spend comparison |
| 6 | Products with highest discount dependency |
| 7 | Customer segmentation: New, Returning, Loyal |
| 8 | Top 3 products per category (window functions) |
| 9 | Repeat buyers and subscription likelihood |
| 10 | Revenue contribution by age group |

### 3. Dashboard (Power BI)
- Built an interactive dashboard with slicers for gender, category, subscription status, and shipping type
- Key KPIs: 3.9K customers, $59.76 average purchase amount, 3.75 average review rating
- Visuals include revenue by category, sales by age group, and subscription distribution

## Key Findings

- Male customers generated significantly more revenue ($157,890) than female customers ($75,191)
- 839 customers used discounts but still spent above the average — a high-value segment worth retaining
- 80% of the customer base falls into the "Loyal" segment (3,116 out of 3,900)
- Subscribers and non-subscribers spend almost the same on average (~$59) — subscription perks may not be differentiated enough
- Young Adults are the top revenue-generating age group at $62,143
- Hat, Sneakers, and Coat have the highest discount dependency (~49–50%)

## Business Recommendations

- **Boost subscriptions** by offering exclusive perks — current subscribers show no spending advantage, suggesting the program needs stronger incentives
- **Reward loyal customers** with a tiered loyalty program to retain the 3,116 who already shop regularly
- **Revisit discount strategy** for high-dependency products like Hat and Sneakers — heavy discounting may be eroding margins
- **Target Young Adults and Middle-aged segments** in campaigns — they drive the most revenue
- **Promote top-rated products** (Gloves, Sandals, Boots) more prominently in marketing materials

## Dataset

- 3,900 rows × 18 columns
- Key fields: Age, Gender, Location, Item Purchased, Category, Purchase Amount, Season, Shipping Type, Discount Applied, Review Rating, Subscription Status, Previous Purchases

