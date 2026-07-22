# 🛒 Customer Satisfaction Prediction for an E-commerce Company

## 📌 Project Overview

This project aims to predict whether a customer is satisfied with their most recent purchase using machine learning techniques.

The dataset was obtained from Kaggle and represents an online retail company with three warehouses that fulfill customer orders. By analyzing order characteristics, delivery information, seasonal factors, and customer behavior, the project builds classification models to identify the key drivers of customer satisfaction.

---
## 💼 Business Problem

Customer satisfaction is a key indicator of business success in the e-commerce industry. Negative shopping experiences can lead to customer churn, lower retention rates, and reduced brand loyalty.

However, customer satisfaction is influenced by multiple operational factors such as delivery performance, shipping costs, warehouse distance, and seasonal demand. Without understanding these factors, businesses may struggle to identify customers who are likely to become dissatisfied and improve their services proactively.

This project develops a predictive model to identify unhappy customers and uncover the operational factors that have the greatest impact on customer satisfaction.

---

## ❓ Business Questions

This project aims to answer the following business questions:

- Which operational factors have the greatest influence on customer satisfaction?
- Which machine learning model provides the best predictive performance?
- How can the prediction results support business decisions to improve customer experience?

---
## 🚀 Workflow
```mermaid
flowchart LR
    A[Data Collection] --> B[Exploratory Data Analysis]
    B --> C[Data Cleaning]
    C --> D[Train-Test Split]
    D --> E[Encoding]
    E --> F[Random Oversampling]
    F --> G[Standard Scaling]
    G --> H[Model Training]
    H --> I[Model Evaluation]
    I --> J[Feature Importance Analysis]
    J --> K[Business Insights & Recommendations]
    K --> L[GitHub Portfolio]
```
---
## 🎯 Objectives

- Perform exploratory data analysis (EDA) to understand the dataset.
- Clean and preprocess raw data.
- Handle missing values, duplicates, and outliers.
- Engineer and encode features for machine learning.
- Address class imbalance using Random Oversampling.
- Build multiple classification models.
- Compare model performance using various evaluation metrics.
- Interpret model predictions using feature importance analysis.
- Provide actionable business recommendations.

---

## 📂 Dataset

**Source:** [Kaggle](https://www.kaggle.com/code/muhammadshahrayar/data-cleaning-eda-of-retail-dataset/input)

### Dataset Information

- 500 observations
- 16 original features
- Binary target variable:
  - **is_happy_customer**
    - True = Happy customer
    - False = Unhappy customer

### Dataset Features

| Feature | Used in Model | Description |
|----------|---------------|-------------|
| order_id | ❌ | Unique identifier for each order. |
| customer_id | ❌ | Unique identifier for each customer. |
| date | ❌ | Date the order was placed (YYYY-MM-DD). |
| nearest_warehouse | ✅ | Name of the warehouse closest to the customer. |
| shopping_cart | ❌ | List of purchased items and quantities. |
| order_price | ✅ | Total price of items before discounts and delivery charges (AUD). |
| delivery_charges | ✅ | Delivery fee charged for the order (AUD). |
| customer_lat | ❌ | Customer's latitude. |
| customer_long | ❌ | Customer's longitude. |
| coupon_discount | ✅ | Percentage discount applied to the order. |
| order_total | ❌ | Final order amount after discounts and delivery charges (used for data validation, not as a predictive feature). |
| season | ✅ | Season in which the order was placed. |
| is_expedited_delivery | ✅ | Whether expedited delivery was requested. |
| distance_to_nearest_warehouse | ✅ | Distance (km) between the customer and the nearest warehouse. |
| latest_customer_review | ❌ | Customer's latest review text. |
| is_happy_customer | 🎯 Target | Customer satisfaction label (True = Happy, False = Unhappy). |
---

## 🔍 Exploratory Data Analysis

The exploratory analysis includes:

- Dataset overview
- Missing value detection
- Duplicate checking
- Descriptive statistics
- Distribution analysis
- Outlier detection
- Category distribution
- Target class distribution

---

## 🧹 Data Cleaning

The following preprocessing steps were applied:

- Removed irrelevant columns
  - order_id
  - customer_id
  - date
  - shopping_cart
  - customer_lat
  - customer_long
  - latest_customer_review

- Removing records where order values ​​do not match the order_total value
- Detecting and handling outliers in necessary columns
- Corrected inconsistent categorical values
- One-Hot Encoding
  - season
  - nearest_warehouse
- Ordinal Encoding
  - is_expedited_delivery
  - is_happy_customer
- Standard Scaling (for Logistic Regression and SVM)
- Random Oversampling on the training set to address class imbalance

---

## 🤖 Machine Learning Models

Three classification models were trained and evaluated.

- Logistic Regression
- Random Forest Classifier
- Support Vector Machine (SVM)

---

## 📊 Model Evaluation

Models were compared using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix

The best-performing model was selected based on the overall evaluation metrics rather than a single metric.

---

## 📈 Feature Importance Analysis

To improve model interpretability, feature importance was analyzed using:

- Logistic Regression coefficients
- SHAP values

The analysis revealed that the most influential features include:

- is_expedited_delivery
- delivery_charges
- season
- distance_to_nearest_warehouse

---

## 💡 Business Insights

Key findings include:

- **Expedited delivery** has the **strongest** influence on customer satisfaction prediction.
- **Delivery charges** are positively associated with satisfied customers.
- Customer satisfaction varies across **different seasons**.
- Customers **farther from warehouses** are slightly more likely to become **dissatisfied**.
- Pricing-related variables contribute less than delivery-related variables.

---

## 📌 Business Recommendations

Based on the analysis, the company should consider:

- Improve the reliability of express delivery services.
- Optimize logistics for customers located far from warehouses.
- Develop operational plans to address seasonal demand fluctuations.
- Research the reasons why premium delivery services achieve higher customer satisfaction.
- Prioritize logistics improvements over aggressive discount campaigns.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SHAP
- Imbalanced-learn

---
## 🚀 Workflow

```
Data Collection
      │
      ▼
Exploratory Data Analysis
      │
      ▼
Data Cleaning
      │
      ▼
Train-Test Split
      │
      ▼
Feature Encoding
      │
      ▼
Random Oversampling
      │
      ▼
Standard Scaling
      │
      ▼
Model Training
      │
      ▼
Model Evaluation
      │
      ▼
Feature Importance Analysis
      │
      ▼
Business Insights and Recommendations
```
---

## 📚 Key Learning Outcomes

Through this project, I practiced:

- End-to-end data preprocessing
- Exploratory data analysis (EDA)
- Handling imbalanced datasets
- Building classification models
- Model evaluation and comparison
- Model interpretation using SHAP
- Translating machine learning results into business recommendations

---

## 👤 Author

**Tran Anh**

Final-year International Business student passionate about Data Analytics.
- LinkedIn: www.linkedin.com/in/anh-trần-thị-minh-481789291
- GitHub: https://github.com/trananh662005-dotcom
- Email: trananh662005@gmail.com
