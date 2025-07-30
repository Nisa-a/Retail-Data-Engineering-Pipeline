# 🛍️ Retail Data Engineering Pipeline

This project builds a data pipeline using Python and SQLite to process, transform, and store retail data related to customer purchases, transactions, and inventory. The full pipeline is implemented within a Jupyter Notebook using pandas, seaborn, and sqlite3.

---

## 📚 Project Overview

This project simulates the responsibilities of a data engineer at a retail company. It covers the complete ETL (Extract, Transform, Load) process:

- **Data Extraction** from multiple CSV files
- **Data Exploration** and cleaning, including handling missing values, correcting data types, and detecting duplicates
- **Data Transformation** through merging, filtering, aggregation, and encoding
- **Data Loading** into a structured SQLite relational database

The final result is a clean and integrated dataset that supports meaningful business insights like revenue by department, customer behavior, and inventory performance.

---

## 📊 Datasets

**Source:** Kaggle (3 separate datasets)

- `customer_shopping_data.csv`: Contains demographic and transactional behavior of retail customers
- `scanner_data.csv`: Contains item-level sales transaction data
- `data.csv`: Contains retail inventory details like size, department, and units

**Features include:**

- Customer: Age, Gender, Purchase Date
- Transaction: SKU, Price, Quantity, Date
- Inventory: Department, Size, Units in stock

---

## ⚙️ Techniques & Processing

- Data ingestion with `pandas`
- Cleaning operations:
  - Type conversion (e.g., dates, numeric columns)
  - Removing duplicates
  - Handling missing values using mode imputation
- Data Transformation:
  - Merging datasets using `inventory_id` and `transaction_id`
  - Feature engineering (`total_sales`, `price_per_unit_sold`)
  - Filtering (e.g., high-value purchases, time-based trends)
  - Encoding categorical features (e.g., Gender)
- SQLite-based relational schema creation
  - Tables: `Customer_details`, `Transactions`, `Inventory`
  - One-to-many relationships modeled properly
- Data loading using `.to_sql()` from pandas

---

## 🧪 Output & Analysis

The processed data enables queries and insights such as:

- Top-performing departments by revenue
- High-value customer segments
- Time-series analysis of purchases by year
- Inventory analysis per store location

---

## 📁 Files in This Repo

- `notebooks/data_pipeline.ipynb`: Jupyter Notebook with all steps and outputs
- `data/customer_shopping_data.csv`: Raw customer data
- `data/transactions.csv`: Raw transaction data
- `data/inventory_data.csv`: Raw inventory data
- `db/customer_purchase_data.db`: SQLite database containing final processed data
- `README.md`: This description file
- `requirements.txt`: Dependencies for running the project

---

## 🛠️ Tech Stack

- Python 3.9+
- pandas, numpy
- seaborn, matplotlib
- sqlite3
- Jupyter Notebook

---
