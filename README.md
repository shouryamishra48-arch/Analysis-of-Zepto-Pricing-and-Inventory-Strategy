# Analysis of Zepto Pricing & Inventory Strategy
## Table of Contents
- [Project Overview](#Project-Overview)
- [Dataset](#dataset)
- [Tools and Technologies](#Tools-and-Technologies)
- [Analysis Workflow](#Analysis-Workflow)
- [Key Insights](#Key-Insights)
- [Visualizations](#Visualizations)
- [Challenges and Solutions](#Challenges-and-Solutions)
## 📌 Project Overview
This project delivers an end-to-end analytics solution using Python, SQL, and Power BI to analyze Zepto-style quick-commerce retail data. The goal is to uncover pricing inefficiencies, margin leakage, discount behavior, stock risks, and replenishment gaps to support data-driven operational and pricing decisions. The project demonstrates complete data cleaning, validation, feature engineering, and dashboard development.
## 📂 Dataset 
Source: Kaggle
File Used: zepto_v2.csv
Format: CSV
Rows & Columns: 3732 rows × 9 columns

Key Features
- category → Product category
- name → Product name
- mrp → Maximum retail price
- discountPercent → % discount applied
- discountedSellingPrice → Selling price after discount
- available_qty → Available stock per SKU
- out_of_stock → 0/1 flag for stockout status
- weightInGms → Product weight in grams
## 🛠️ Tools & Technologies
Languages & Libraries
- Python 3.x
    - Pandas → Data cleaning & transformation
    - NumPy → Numerical processing

Database Tools
- MySQL Workbench
    - Data validation
    - Schema creation
    - Integrity checks

Visualization Tools
- Power BI Desktop
    - DAX
    - Power Query
    - Multi-page interactive dashboard
## 🔍 Analysis Workflow
1. Data Cleaning (Python)
- Loaded raw CSV data
- Fixed inconsistent column names & types
- Removed duplicates and invalid rows
- Converted discount, pricing, and weight fields
- Engineered new fields (discount_%, price_per_gram, stockout_flag)

2. Data Validation (SQL)
- Verified dataset row counts & formats
- Checked for missing and negative values
- Ensured category integrity
- Confirmed price/discount correctness

3. Exploratory Analysis
- Pricing distribution
- Discount patterns
- Stock availability trends
- Category-level performance

4. Dashboard Development (Power BI)
Built a 3-page business insights dashboard:

📄 Page 1 — Pricing & Discount Insights
- Avg Discount %
- Category-wise discount comparison
- Price vs discount relationships

📄 Page 2 — Pricing & Margin Insights
- Price per gram analysis
- Top 10 overpriced items
- Top 10 underpriced items
- Category profitability indicators

📄 Page 3 — Inventory & Stock Risk
- Stockout count by category
- Average available quantity
- Low-stock summary (1 row per category)
- Category slicers for deeper analysis
## 📊 Key Insights
- Pricing & Discount
    - Several categories display inefficient discounting patterns
    - Some product weights are misaligned with price-per-gram, revealing pricing mismatches

- Margin & Profitability
    - Identified overpriced and underpriced SKUs
    - Exposed margin leakage areas across categories

- Inventory & Stock Management
    - Categories like Munchies, Cooking Essentials, and Packaged Food show high stockout rates
    - Majority of categories have low average available quantities, indicating replenishment delays
    - Product-level low-stock alerts enable proactive inventory planning
  ## Challenges and Solutions
1️⃣ Challenge — Python Dependency & Module Errors
- Modules like sqlite3 and incorrectly typed package names caused installation errors during environment setup.
✅ Solution:
- Verified the Python version, removed unnecessary installations, and relied on built-in libraries while using correct installation commands for required packages.
2️⃣ Challenge — MySQL Import Errors (“Unknown column ‘None’…”)
- Importing the cleaned dataset into MySQL Workbench failed due to datatype mismatches, invalid NULL values, and unexpected headers.
✅ Solution:
- Re-exported the dataset with standardized column names, correct datatypes, and without additional metadata. Successfully re-imported using a corrected CSV structure.
3️⃣ Challenge — Incorrect Aggregation in Power BI Visuals
- Power BI incorrectly interpreted Boolean fields (out_of_stock) as percentages and used averages instead of sums, leading to misleading visuals (e.g., all values showing 100%).
✅ Solution:
- Created strict numeric columns (e.g., stockout_flag), applied explicit aggregation rules, and rebuilt visuals using validated measures for accurate insights.
## 📸 Visualizations

The dashboard includes:
- KPI Cards
- Column Charts
- Category Slicers
- Low-Stock Summary Table
- Price-per-gram distribution
- Pricing Alignment Scatter Chart
- Available Quantity Line Chart
- Overpriced vs Underpriced SKU tables


   
<img width="1308" height="732" alt="Screenshot 2025-11-10 211904" src="https://github.com/user-attachments/assets/ed348f72-e052-48c6-a91d-7d278a7ec0a2" />

<img width="1305" height="729" alt="Screenshot 2025-11-10 211848" src="https://github.com/user-attachments/assets/d216ad38-4bd8-448c-b76f-71e4e8ab30a2" />

<img width="1309" height="729" alt="image" src="https://github.com/user-attachments/assets/37cbdf86-805f-47b7-9297-c101b6c546dc" />

