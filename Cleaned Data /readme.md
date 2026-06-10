
# Step 4: Data Cleaning & Validation

This section documents the cleaning and validation performed on the datasets used in the **AI‑Augmented Data Cleaning & Validation Project**.  
It ensures that missing values, duplicates, and anomalies were handled consistently, creating reliable inputs for analysis and modeling.

---

## 📘 What Was Done in This Section
- Inspected each dataset for **missing values, duplicates, and anomalies**.
- Applied **dataset‑specific cleaning strategies** (e.g., placeholders for missing timestamps, unique mapping for geolocation).
- Validated **relationships between datasets** (customers ↔ orders ↔ items ↔ payments ↔ reviews).
- Standardized formats (timestamps, categorical values, zip code prefixes).
- Saved cleaned versions into a dedicated **`cleaned_data` directory**.

---

## 📂 Dataset‑Specific Actions

### Customers Dataset
- Checked for missing zip prefixes.  
- Dropped duplicates.  
- Validated customer IDs against orders.  
- Standardized zip code format.

### Orders Dataset
- Filled missing timestamps with descriptive placeholders (`Not Approved`, `Not Shipped`, `Not Delivered`).  
- Converted all date fields to datetime.  
- Dropped duplicates.  
- Flagged undelivered and unshipped orders for analysis.

### Order Items Dataset
- Dropped duplicates.  
- Validated foreign keys (orders, products, sellers).  
- Converted shipping limit date to datetime.  
- Flagged negative freight values.

### Order Payments Dataset
- Dropped duplicates.  
- Validated order IDs.  
- Converted payment values to float.  
- Flagged invalid/zero payments.

### Order Reviews Dataset
- Filled missing titles/messages with `"No Title"` / `"No Comment"`.  
- Converted timestamps to datetime.  
- Dropped duplicates.  
- Validated order IDs.

### Products Dataset
- Filled missing categories with `"Unknown"`.  
- Filled missing lengths, descriptions, photos with `0`.  
- Filled missing dimensions/weight with `0`.  
- Standardized category names to lowercase.  
- Flagged products with invalid dimensions/weight.

### Sellers Dataset
- Dropped duplicates.  
- Validated seller IDs against items.  
- Standardized zip code prefixes.  
- Flagged 1,027 invalid zip codes and replaced with `"Unknown"`.

### Geolocation Dataset
- Dropped 261,831 duplicate rows.  
- Created a unique mapping (`df_geo_unique`) with one entry per zip prefix.  
- Standardized zip code prefixes.  
- Validated against customer and seller zip codes.

### Data Dictionary
- Used as a reference baseline; no cleaning required.

---

## 📘 Why This Section Matters
- Ensures **data integrity** before analysis.  
- Provides **consistent, recruiter‑friendly documentation** of cleaning decisions.  
- Creates a **cleaned_data repository** for reproducible workflows.  
- Highlights **analytical thinking** in handling real‑world anomalies.

---

## ✅ Next Step
With cleaned datasets saved, the project now moves to **Step 5: Exploratory Data Analysis (EDA)**, where descriptive statistics, relationships, and visualizations will be generated to uncover business insights.
