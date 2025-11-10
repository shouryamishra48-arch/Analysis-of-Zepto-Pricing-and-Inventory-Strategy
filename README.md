# Analysis of Zepto Pricing & Inventory Strategy
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
