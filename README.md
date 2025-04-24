# 🍷 Wine Subscription Classifier – Predicting "Halfway There" Opt-Ins

This project explores how to use customer data to predict which users are most likely to subscribe to a wine promotion launched by a meal delivery service. The offer, "Halfway There", delivers a half bottle of wine from small California vineyards every Wednesday — a smart cross-sell move to boost customer engagement and revenue.

The goal: Build a simple, interpretable machine learning model that helps target the right customers with minimal waste.

---

## 🧠 Problem

Customers aren’t explicitly asked whether they’re interested in the promotion — but their behavior tells a story.  
Can we use past interactions to predict which customers are likely to opt in?

---

## 📊 Data

The dataset includes ~2,000 records from customers who were offered the promotion. Features include:

- Order volume and value
- Email domain (as a proxy for profile)
- Engagement data (time on site, photos viewed)
- Support touchpoints
- Personalization metrics

---

## 🎯 Goal

- Predict binary outcome: "Subscribed" or "Did not subscribe"
- Understand key behavioral drivers of subscription
- Optimize targeting to reduce marketing waste

---

## 🛠️ Models Used

- **Logistic Regression**
- **Decision Tree**
- **CART** (best performer)

The CART model achieved:
- **Training accuracy:** 89.7%
- **Testing accuracy:** 84.7%
- **Minimal overfitting**, with a train-test gap of just ~5%

---

## 🔍 Key Findings

- **Email domain** emerged as the strongest predictor — possibly due to socioeconomic or tech engagement patterns.
- **Average time per site visit** and **total photos viewed** were strong indicators of interest and intent.
- **Cancellations before noon** were highly negatively correlated with subscription — flagging churn-prone users.
- **Followed Recommendations %**, while intuitively important, showed surprisingly low predictive power — might be due to encoding or noise.

---

## ⚠️ What Could Be Improved

###  Modeling
- Expand to **ensemble models** like Random Forest or Gradient Boosting for better accuracy and robustness.
- Consider **logistic regression with regularization (Lasso)** to reduce noise and overfitting.

### Feature Engineering
- Early transformation of skewed variables would improve model stability.
- Consider removing or re-scaling weak features.

### Interpretability
- Visualizations (decision tree plots, SHAP values) could help explain predictions to stakeholders.
- Add confidence intervals for outputs to support real-world decision-making.

---

## 📁 Repository Structure

data/        → Promotion data 
notebooks/   → Jupyter notebook with charts/graphs/comments(`Apprentice_Chef_Dataset.xlsx`)
output/      → Jupyter notebook with results in html format → Download to view ('ML-Classification-Project.html')
README.md    → you're reading it

