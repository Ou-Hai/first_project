# 📦 Supply Chain & Operational Insights Optimization

## 📚 Table of Contents  
- [📦 Project Description](#-project-description)  
- [📊 Objectives](#-objectives)  
- [🧩 Dataset Overview](#-dataset-overview)  
- [🔗 Source](#-source)  
- [🛠️ Tech Stack & Tools](#️-tech-stack--tools)  
- [🔧 Data Processing](#-data-processing)  
- [🧪 Hypotheses](#-hypotheses)  
- [📈 Analysis Summary (To Be Completed)](#-analysis-summary-to-be-completed)

---

## 📦 Project Description  
This project analyzes a supply chain dataset containing customers, orders, order items, product details, and payment information.  
The goal is to understand logistics performance, shipping cost drivers, product characteristics, and revenue distribution across categories.

The workflow includes data cleaning, feature engineering, and validating business hypotheses using Python and Tableau.

---

## 📊 Objectives  
✔️ Build an integrated analysis-ready supply chain dataset  
✔️ Investigate logistics efficiency and delivery performance  
✔️ Analyze product attribute impact on shipping cost and timing  
✔️ Identify high-value categories and revenue drivers  
✔️ Validate six hypotheses using statistical and visual methods  

---

## 🧩 Dataset Overview  

Five relational datasets are used in this project:

| Dataset | Description |
|--------|-------------|
| **df_Customers** | Customer demographic and geographic data |
| **df_Orders** | Order timestamps and lifecycle information |
| **df_OrderItems** | Product-level pricing and shipping details |
| **df_Products** | Product dimensions, weight, and category |
| **df_Payments** | Payment values and payment types |

---

## 🔗 Source  
All five CSV files were sourced from **Kaggle**.

---

## 🛠️ Tech Stack & Tools  

<p align="left">
  <img src="https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/pandas-Data%20Analysis-150458?logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/numpy-Numerical%20Computing-013243?logo=numpy&logoColor=white" />
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white" />
  <img src="https://img.shields.io/badge/Matplotlib-Visualization-11557C" />
  <img src="https://img.shields.io/badge/Tableau-Dashboard-1F5FB2?logo=tableau&logoColor=white" />
  <img src="https://img.shields.io/badge/uv-Environment-4C1" />
</p>

---

## 🔧 Data Processing  

### 1. Data Cleaning
- Converted timestamp fields to `datetime`  
- Removed invalid or canceled orders  
- Resolved duplicates  
- Standardized data types  

### 2. Feature Engineering
Computed fields:
- `delivery_time_days`  
- `product_volume = length × width × height`  
- `shipping_cost_ratio = shipping_cost / price`  
- `revenue_per_order`  

### 3. Merging the Five Datasets
Merged using relational keys:
- `customer_id`  
- `order_id`  
- `product_id`  

Result: A fully consolidated dataset for analytics.

---

## 🧪 Hypotheses  

### H1: Heavier products incur higher shipping costs.  

### H2: Larger (high-volume) products take longer to deliver.  

### H3: Delivery speed differs across customer states.  

### H4: Some product categories have higher logistics cost ratios.  

### H5: Product category strongly influences total revenue.  

### H6: Higher shipping cost is associated with longer delivery time.  

---

## 📈 Analysis Summary (To Be Completed)  
> Final conclusions and visualizations will be added after completing the analytical steps.