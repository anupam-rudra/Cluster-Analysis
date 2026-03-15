# 🛒 E-Commerce Customer Segmentation using RFM Analysis and K-Means Clustering

## 📌 Project Overview
Customer segmentation is a powerful technique used by businesses to understand customer behavior and target marketing strategies effectively.

In this project, we analyze an e-commerce transaction dataset and segment customers based on their purchasing behavior using **RFM Analysis** and **K-Means Clustering**.

The goal is to identify different types of customers such as:

- High-value customers
- Loyal customers
- At-risk customers
- Low-engagement customers

This helps businesses improve **marketing strategies, retention, and personalization**.

---

# 📊 Dataset

Dataset: **Online Retail Dataset**

The dataset contains transactional data from a UK-based online retail store.

### Features

| Column | Description |
|------|-------------|
| InvoiceNo | Unique transaction ID |
| StockCode | Product code |
| Description | Product name |
| Quantity | Number of items purchased |
| InvoiceDate | Date of transaction |
| UnitPrice | Price per item |
| CustomerID | Unique customer ID |
| Country | Customer country |

---

# ⚙️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

# 📈 Project Workflow

```
Load Dataset
      ↓
Data Cleaning
      ↓
Handle Missing Values
      ↓
Feature Engineering
      ↓
RFM Analysis
      ↓
Feature Scaling
      ↓
K-Means Clustering
      ↓
Cluster Evaluation
      ↓
Visualization
      ↓
Business Insights
```

---

# 🧹 Data Preprocessing

The following preprocessing steps were performed:

- Removed missing **CustomerID**
- Removed negative **Quantity** and **UnitPrice**
- Converted **InvoiceDate** to datetime format
- Created **TotalPrice** feature

```
TotalPrice = Quantity × UnitPrice
```

---

# 📊 RFM Analysis

RFM stands for:

| Metric | Meaning |
|------|------|
| Recency | Days since last purchase |
| Frequency | Number of purchases |
| Monetary | Total money spent |

These metrics help understand **customer value and engagement**.

---

# 🔍 Feature Scaling

Clustering algorithms are sensitive to feature scale.

We used **StandardScaler** to normalize the RFM features so that each feature contributes equally to clustering.

---

# 📉 Finding Optimal Clusters

The **Elbow Method** was used to determine the optimal number of clusters.

The method evaluates **Within Cluster Sum of Squares (WCSS)** for different values of *K*.

The elbow point indicates the best number of clusters.

---

# 🤖 K-Means Clustering

After determining the optimal cluster count, we applied **K-Means clustering** to segment customers.

Each customer is assigned to a cluster based on similarity in purchasing behavior.

---

# 📊 Cluster Visualization

Clusters were visualized using **scatter plots** to observe the separation between customer groups.

Example visualization:

- Frequency vs Monetary Value
- Cluster color indicates customer segment

---

# 📊 Cluster Interpretation

| Cluster | Customer Type | Description |
|------|------|------|
| Cluster 0 | High Value Customers | Frequent purchases and high spending |
| Cluster 1 | Loyal Customers | Moderate spending but frequent purchases |
| Cluster 2 | At Risk Customers | Previously active but inactive recently |
| Cluster 3 | Low Value Customers | Low purchase frequency and spending |

---

# 💡 Business Insights

This segmentation can help businesses:

- Target **premium customers** with loyalty rewards
- Re-engage **inactive customers**
- Offer discounts to **price-sensitive segments**
- Personalize marketing campaigns

