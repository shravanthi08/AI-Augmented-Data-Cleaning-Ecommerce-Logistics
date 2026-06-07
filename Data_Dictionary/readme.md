# Data Dictionary

This section documents the structure and relationships of the datasets used in the **AI‑Augmented Data Cleaning & Validation Project**.  
It serves as a reference map for understanding how different files connect, guiding cleaning, validation, and analysis.

---

## 📘 What Was Done in This Section
- Created a dedicated **Data_Dictionary directory** to organize dataset documentation.
- Added individual Markdown files for each dataset (`customers_dataset`, `orders_dataset`, `order_items_dataset`, etc.).
- Wrote **About sections** for each dataset, describing:
  - Purpose of the file
  - Primary keys and important columns
  - Relationships with other datasets
  - Notes on missing values, duplicates, or anomalies
- Summarized the original `Data_dictionary.xlsx` file as a baseline reference.

---

## 📂 Contents
- **customers_dataset.md** → Customer demographics and location details; links to orders.  
- **orders_dataset.md** → Central table of customer orders; connects to items, payments, and reviews.  
- **order_items_dataset.md** → Line‑item details; bridges orders, products, and sellers.  
- **order_payments_dataset.md** → Payment transactions per order; supports multiple installments.  
- **order_reviews_dataset.md** → Customer feedback and ratings linked to orders.  
- **products_dataset.md** → Product catalog with categories and attributes.  
- **sellers_dataset.md** → Seller information including IDs and location.  
- **geolocation_sample_dataset.md** → Maps zip codes to city/state for customers and sellers.  
- **Data_dictionary.xlsx** → Original reference file provided with the dataset.  

---

## 📘 Why This Section Matters
- Provides a **clear map of the dataset** before cleaning.  
- Ensures **relationships are well‑understood** (orders ↔ customers ↔ items ↔ payments ↔ reviews).  
- Helps identify **data quality issues** early (missing timestamps, duplicate IDs, inconsistent categories).  
- Acts as a **recruiter‑friendly showcase** of documentation and analytical thinking.  

---



