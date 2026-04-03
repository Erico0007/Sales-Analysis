# Bike Sales Data Cleaning & Analysis Project

## 📌 Overview
This project focuses on cleaning, transforming, and analyzing a bike sales dataset containing customer demographics, product details, pricing, and profitability metrics.  
The goal is to build a clean, reliable dataset and extract meaningful business insights through exploratory data analysis (EDA).

---

## 🧹 1. Data Cleaning Steps

### ✔️ Column Name Standardization
- Removed leading/trailing spaces
- Replaced spaces with underscores
- Ensured consistent naming across all fields

### ✔️ String Cleanup
- Trimmed whitespace in text fields
- Fixed inconsistent spacing in Country/State fields
- Corrected typos (e.g., “Decmber” → “December”)

### ✔️ Currency Conversion
Converted the following columns from string to numeric:
- `Unit_Cost`
- `Unit_Price`
- `Profit`
- `Cost`
- `Revenue`

Steps included:
- Removing `$` symbols  
- Removing commas  
- Stripping whitespace  
- Converting to `float`

### ✔️ Missing Values
- Identified missing Day, Product_Description, and Order_Quantity
- Dropped or imputed depending on analysis requirements

### ✔️ Duplicate Handling
- Removed exact duplicate rows
- Verified repeated Sales_Order entries

### ✔️ Age Group Standardization
Created a new `Age_Group_Standardized` column based on `Customer_Age`:
- Youth (<25)
- Young Adults (25–34)
- Adults (35–64)
- Seniors (65+)

### ✔️ Date Conversion
- Converted `Date` to datetime format
- Extracted Year, Month, Day for analysis

---

## 📊 2. Analysis Performed

### 🔹 Sales & Profitability
- Total revenue and profit by product model
- Profit margin calculations
- Identification of zero-cost and zero-price transactions

### 🔹 Customer Demographics
- Purchases by age group
- Gender-based purchasing trends
- Age group vs product preference

### 🔹 Geographic Insights
- Revenue by country and state
- Regional product popularity

### 🔹 Time-Based Trends
- Daily revenue trends for December 2021
- High/low sales days
- Holiday-related purchase patterns

### 🔹 Product-Level Insights
- Most purchased bike sizes
- Order quantity distribution
- High-margin product categories

### 🔹 Data Quality Checks
- Detection of inconsistent cost/price relationships
- Identification of unusually high profit margins
- Impact of zero-cost/zero-price transactions

---

## 📁 3. Project Files

| File | Description |
|------|-------------|
| `notebook.ipynb` | Full cleaning + analysis notebook |
| `uncleaned_data.csv` | Original dataset |
| `cleaned_data.csv` | Cleaned dataset (optional) |
| `README.md` | Project documentation |
| `Data_Analysis_Questions.pdf` | Analysis questions summary |

---

## 🛠️ 4. Tools & Libraries Used
- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib / Seaborn** (optional for visuals)
- **VS Code Data Wrangler** (for interactive cleaning)

---

## 🚀 5. How to Run the Notebook

1. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn
