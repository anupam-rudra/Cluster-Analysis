# 📊 Dataset Description

## Online Retail Dataset(Online Retail.xlsx1)

This project uses the **Online Retail Dataset**, which contains transactional data from a UK-based online retail company. The dataset includes all transactions occurring between **December 2010 and December 2011**.

The company mainly sells unique all-occasion gifts and many of its customers are wholesalers.

This dataset is commonly used for **customer segmentation, RFM analysis, and recommendation system research**.

---

# 📁 Dataset Source

Source: UCI Machine Learning Repository

Dataset Link:
https://archive.ics.uci.edu/ml/datasets/Online+Retail

---

# 📊 Dataset Overview

| Attribute | Details |
|----------|---------|
| Dataset Type | Transactional Data |
| Time Period | Dec 2010 – Dec 2011 |
| Number of Rows | ~541,909 transactions |
| Number of Columns | 8 |
| Domain | E-commerce |

---

# 📋 Feature Description

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| InvoiceNo | String | Unique invoice number for each transaction |
| StockCode | String | Unique product identifier |
| Description | String | Name or description of the product |
| Quantity | Integer | Number of units purchased |
| InvoiceDate | Datetime | Date and time of the transaction |
| UnitPrice | Float | Price of a single product unit |
| CustomerID | Float | Unique customer identifier |
| Country | String | Country where the customer resides |

---

# 📦 Example Record

| InvoiceNo | StockCode | Description | Quantity | InvoiceDate | UnitPrice | CustomerID | Country |
|----------|-----------|-------------|----------|-------------|-----------|------------|---------|
| 536365 | 85123A | WHITE HANGING HEART T-LIGHT HOLDER | 6 | 2010-12-01 | 2.55 | 17850 | United Kingdom |

---

# 🧹 Data Quality Notes

Some preprocessing is required before analysis because the dataset contains:

- Missing **CustomerID** values
- Negative **Quantity** values (product returns)
- Negative **UnitPrice** values
- Duplicate invoices

These issues were handled during the **data preprocessing stage** of the project.

---

# 📊 Feature Engineering

To perform customer segmentation, an additional feature was created:

```
TotalPrice = Quantity × UnitPrice
```

This represents the **total transaction value**.

---

# 📈 RFM Analysis Features

Customer segmentation is based on **RFM metrics**:

| Metric | Description |
|------|-------------|
| Recency | Days since the customer's last purchase |
| Frequency | Number of transactions made by the customer |
| Monetary | Total amount spent by the customer |

These features help identify **customer value and purchasing behavior**.

---



# 📚 References

UCI Machine Learning Repository  
https://archive.ics.uci.edu/ml/datasets/Online+Retail
