# 🍔 DoorDash-Style User Churn Prediction & Behavior Analysis

This project simulates a real-world churn prediction pipeline for a food delivery platform, inspired by the Consumer Data Analyst role at DoorDash. It combines user behavior analysis, machine learning, and dashboarding to uncover retention insights and identify at-risk users.

---

## 📊 Project Overview

**Goal:** Predict user churn and surface actionable insights to support retention and growth efforts.

**What I Did:**
- Simulated user & order datasets resembling DoorDash
- Engineered behavioral features (promo usage, delivery time, etc.)
- Created a probabilistic churn label based on real-world patterns
- Trained a churn prediction model (Random Forest)
- Evaluated performance (Accuracy: 74%, ROC AUC: 0.79)
- Built an interactive dashboard using Looker Studio

---

## 📁 Dataset

Simulated datasets:
- `Users.csv` – user_id, signup_date, platform, location
- `Orders.csv` – order_id, user_id, order_date, amount, delivery time, promo use, order time

---

## 🔧 Feature Engineering

| Feature               | Description                                 |
|-----------------------|---------------------------------------------|
| total_orders          | Number of orders placed                     |
| avg_order_amount      | Average spend per order                     |
| avg_delivery_time     | Average time taken for delivery             |
| promo_usage_rate      | % of orders with promo codes                |
| late_night_pct        | % of orders placed during late night hours |
| days_since_last_order | Inactivity metric for each user            |

---

## 🧠 Churn Modeling

Churn was defined probabilistically using:
- Days since last order
- Delivery delays
- Promo sensitivity
- Low order frequency

**Model Used**: Random Forest Classifier  
**ROC AUC**: 0.79  
**Precision (Churned)**: 71%  
**Recall (Churned)**: 62%

---

## 📈 Dashboard

The final dashboard (built in Looker Studio) includes:
- Churn rate by platform & location
- Delivery time vs churn
- Promo sensitivity vs churn
- User-level churn risk explorer

---

## ✅ Key Takeaways

- Users with high delivery times and low promo usage are more likely to churn
- Mobile users retain better than Web users
- Most churned users placed <3 orders
