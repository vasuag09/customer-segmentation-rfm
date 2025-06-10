# 🛍️ Customer Segmentation with RFM Analysis and K-Means Clustering

This project performs **customer segmentation** using **RFM (Recency, Frequency, Monetary)** analysis and **K-Means clustering** on the [Online Retail Dataset](https://www.kaggle.com/datasets/vijayuv/onlineretail). The goal is to group customers based on purchasing behavior for marketing strategies, loyalty analysis, and business insights.

---

## 📁 Dataset

- **Source**: Kaggle - Online Retail Dataset
- **Fields Used**:
  - `InvoiceNo`
  - `InvoiceDate`
  - `CustomerID`
  - `Quantity`
  - `UnitPrice`
  - `Country`

---

## 📊 RFM Analysis Overview

- **Recency**: Days since the last purchase
- **Frequency**: Number of unique purchases
- **Monetary**: Total spending

### Steps:
1. Clean data (remove nulls, canceled orders, etc.)
2. Compute RFM metrics using SQL/pandas
3. Assign RFM scores using quantiles
4. Map customers into segments (e.g., Champions, At Risk)
5. Visualize segment distribution and R×F vs M heatmap

---

## 🤖 K-Means Clustering

Used K-Means to group customers based on:
- `Quantity`
- `UnitPrice`

### Preprocessing:
- Removed `CustomerID` from features (used only as identifier)
- Scaled features using `StandardScaler`
- Explored log-transformed values due to skewed data
- Visualized clusters and centroids in scatter plots

---

## 📈 Visualizations

- RFM segment count bar chart
- Heatmap of average monetary value by R and F scores
- K-Means cluster plot (Quantity vs UnitPrice)
- Elbow Method to determine optimal number of clusters

![image](https://github.com/user-attachments/assets/139dfaba-1fe1-454c-91d2-c370935ad02c)

---

## 🧠 Key Learnings

- `CustomerID` should **not** be used as a feature in clustering
- K-Means is sensitive to feature scales → use `StandardScaler` or log-transform
- RFM metrics give meaningful insight into customer behavior
- Visualization helps detect outliers and improve feature engineering

---

## 💻 Tech Stack

- **Language**: Python
- **Libraries**: pandas, numpy, matplotlib, seaborn, scikit-learn
- **Tools**: Jupyter Notebook, SQL (for initial RFM), Excel (optional)

---

## 📂 File Structure

