# 📦 Supply Chain & Operational Insights Optimization

## 📚 Table of Contents  
- [📦 Project Description](#-project-description)  
- [📊 Objectives](#-objectives)  
- [🧩 Dataset Overview](#-dataset-overview)  
- [🔗 Source](#-source)  
- [🛠️ Tech Stack & Tools](#️-tech-stack--tools)  
- [🔧 Data Processing](#-data-processing)  
- [🧪 Hypotheses](#-hypotheses)  
- [🔑 Analysis & Key Findings)](#-analysis-key-findings)
- [📈 Business Insights)](#-business-insights)
- [👥 Project Management & Collaboration)](#-project-management-collaboration)

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

H1: Heavier products incur higher shipping costs.  

H2: Larger (high-volume) products take longer to deliver.  

H3: Delivery speed differs across customer states.  

H4: Some product categories have higher logistics cost ratios.  

H5: Product category strongly influences total revenue.  

H6: Higher shipping cost is associated with longer delivery time.  

---

## 🔑 Analysis & Key Findings 

### H1 – Product Weight vs Shipping Cost
Shipping charges increase with product weight, but the overall change is relatively small (approximately €40 → €46 on average).  
Significant variability exists within each weight category, indicating that weight alone is not a strong predictor of shipping cost.

**Conclusion**: Supported, but with limited predictive power.



### H2 – Product Volume vs Delivery Time
Delivery time rises gradually as product volume increases (around 11 → 13 days).  
However, large variability within volume groups suggests that volume does not reliably predict delivery speed.

**Conclusion**: Supported, but effect size is small.



### H3 – Delivery Speed by Customer State
Delivery performance differs substantially across customer states.  
For example, São Paulo shows faster and more stable delivery times, while remote states such as Roraima experience longer and more variable delivery durations.

**Conclusion**: Supported. Geographic location is a key driver of delivery speed.



### H4 – Logistics Cost Ratio by Product Category
Certain product categories consistently exhibit higher logistics cost ratios (approximately 1.7–1.8), while others remain closer to 0.8.  
Outliers indicate extremely costly shipments in specific categories.

**Conclusion**: Supported. Logistics efficiency varies significantly by product category.



### H5 – Product Category vs Revenue
Revenue distribution across product categories is highly uneven.  
A small number of categories dominate total revenue (e.g., Toys generating over €20 million), while many categories contribute marginally.

**Conclusion**: Supported. Product category strongly influences revenue.



### H6 – Shipping Cost vs Delivery Time
No meaningful relationship is observed between shipping cost and delivery time.  
The correlation coefficient is r = 0.019, indicating no significant linear association.  
Higher shipping fees do not lead to faster delivery.

**Conclusion**: Not supported. Shipping cost is not a predictor of delivery speed.

---

## 📈 Business Insights

Based on the combined results across all hypotheses, the following insights emerge:

1. Pricing strategies should not assume faster delivery in exchange for higher shipping fees.  
2. Delivery performance is primarily driven by operational factors such as carrier selection, SLA management, warehouse location, and fulfillment routing.  
3. Product categories with high logistics cost ratios should be operationally optimized or strategically repriced.  
4. Since revenue is highly concentrated in a few categories, businesses should prioritize investment in top-performing segments.  
5. Underperforming categories may require reassessment, optimization, or portfolio rationalization.

---

## 👥 Project Management & Collaboration

- Followed a structured workflow from data cleaning to hypothesis validation, with additional cleaning applied only when necessary.  
- Maintained strong team coordination through clear task division and continuous communication.  
- Used consistent GitHub version control practices to manage risks related to data inconsistencies, missing values, and outliers.