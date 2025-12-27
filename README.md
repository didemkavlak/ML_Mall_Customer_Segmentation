# 🛍️ Mall Customer Segmentation using K-Means

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Pandas](https://img.shields.io/badge/Library-Pandas-150458)
![Seaborn](https://img.shields.io/badge/Visualization-Seaborn-green)

## 📌 Project Overview
This project applies **Unsupervised Machine Learning** techniques to segment customers of a shopping mall based on their purchasing behavior and annual income.

Using the **K-Means Clustering** algorithm, I identified 5 distinct customer profiles. These insights allow the marketing team to develop targeted strategies, optimizing the marketing budget and increasing customer conversion rates.

---

## 📖 Business Problem
The Mall management wants to understand their customers better to optimize marketing spending.

* **The Challenge:** The "one-size-fits-all" marketing approach is inefficient and yields low ROI.
* **The Goal:** To divide the customer base into distinct groups (segments) based on **Annual Income** and **Spending Score**.
* **The Value:** By understanding these groups, the mall can target "High Income but Low Spenders" differently from "loyal VIPs."

---

## 📊 The Dataset
The dataset is obtained from Kaggle: [Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)

It contains the following features:
* **CustomerID:** Unique ID assigned to the customer (Dropped during preprocessing).
* **Gender:** Gender of the customer.
* **Age:** Age of the customer.
* **Annual Income (k$):** Annual Income of the customer.
* **Spending Score (1-100):** Score assigned by the mall based on customer behavior and spending nature.

---

## 🛠️ Methodology & Approach

I followed the **CRISP-DM** methodology for this project:

1.  **Data Preprocessing:**
    * Dropped `CustomerID` as it adds no analytical value.
    * **Feature Scaling:** Applied `StandardScaler` to normalize `Annual Income` and `Spending Score` to ensure K-Means calculates distances correctly.

2.  **Modeling:**
    * **Algorithm:** K-Means Clustering.
    * **Finding K:** Used the **Elbow Method** to determine the optimal number of clusters. The WCSS (Within-Cluster Sum of Square) graph showed a clear "elbow" at **K=5**.

3.  **Visualization:**
    * Created 2D Scatter plots and 3D Interactive plots (using Plotly) to visualize the separation of clusters.

---

## 📈 Results & Customer Segments

The model identified **5 distinct customer segments**:

> **[Insert your segmentation graph image here]**
> ![Customer Segments](segmentation_result.png)

| Segment Name | Profile Description | Marketing Strategy |
| :--- | :--- | :--- |
| **🌟 VIP (Champions)** | **High Income - High Score** | These are the most valuable customers. **Strategy:** Loyalty programs, exclusive event invitations, early access to new collections. |
| **💰 Frugal High Earners** | **High Income - Low Score** | They have money but don't spend it. **Strategy:** Focus on "Quality" and "Brand Value" in ads. Promote luxury items. |
| **🎯 Standard** | **Medium Income - Medium Score** | The largest group. **Strategy:** General discount coupons, membership offers, standard promotions. |
| **🛍️ Impulsive Spenders** | **Low Income - High Score** | Low income but loves to spend. **Strategy:** "Buy 1 Get 1 Free" deals, seasonal sales, affordable payment plans. |
| **📉 Cautious** | **Low Income - Low Score** | Careful with money. **Strategy:** Target only during major clearance sales or budget-friendly campaigns. |

