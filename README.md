# Sales-Inventory-Shrinkage-Analysis-and-Prediction

Inventory Shrinkage Analysis & Prediction

This project analyzes retail inventory shrinkage by combining datasets on stock, sales, and returns to identify product loss patterns. Using data cleaning, aggregation, and exploratory analysis, it builds predictive models (Linear Regression, Random Forest, Gradient Boosting) to forecast shrinkage. The project includes interactive visualizations and a dashboard to help businesses monitor inventory loss, improve operational efficiency, and reduce financial impact.
## Dataset Description

Three main datasets are used in this project:

The project uses synthetic datasets designed to mimic real-world retail inventory, sales, and return scenarios. Synthetic data was created to simulate realistic stock movements, sales patterns, and return behaviors, ensuring the analysis and models are applicable to practical retail environments while maintaining data privacy.

1. **Inventory Dataset**  
   Contains daily records of stock movements for products.
   - `date`: Date of record  
   - `product_id`: Unique product identifier  
   - `stock_in`: Number of units added to inventory  
   - `stock_out`: Number of units removed or sold from inventory  
   - `stock_remaining`: Units remaining at day end  

2. **Sales Dataset**  
   Tracks daily sales for each product.  
   - `date`: Date of sale  
   - `product_id`: Unique product identifier  
   - `quantity_sold`: Units sold  
   - `unit_price`: Price per unit  

3. **Returns Dataset**  
   Records returned products and reasons.  
   - `date`: Date of return  
   - `product_id`: Unique product identifier  
   - `quantity_returned`: Units returned  
   - `return_reason`: Reason for return (e.g., damaged, wrong item)  

---

Why Synthetic Data?
Synthetic data was used to simulate a controlled retail environment, allowing robust model development without access to proprietary data. The datasets were crafted to include realistic patterns (e.g., seasonal sales spikes, variable return rates) and challenges (e.g., missing values, inconsistent formats) to mirror real-world complexities, ensuring the models and insights are transferable to actual retail scenarios.

## Methodology & Pipeline

1. **Data Cleaning & Preparation**  
   - Loaded datasets, ensured consistent date formats.  
   - Aggregated total stock added (`stock_in`), sales (`quantity_sold`), and returns (`quantity_returned`) by `product_id`.  
   - Merged datasets to calculate **shrinkage** as:  
     `shrinkage = stock_in - (quantity_sold - quantity_returned)`

2. **Exploratory Data Analysis (EDA)**  
   - Visualized top products by shrinkage using bar charts.  
   - Calculated KPIs: total sales revenue, total returns, shrinkage per product.

3. **Model Building**  
   - Used Linear Regression to predict shrinkage based on:  
     - Stock added  
     - Quantity sold  
     - Quantity returned  
   - Split data into training and testing sets.  
   - Evaluated model performance using R² score (~0.99).

4. **Prediction on New Data**  
   - Loaded new monthly inventory and sales data.  
   - Predicted shrinkage values using the trained model.  
   - Saved predictions for business use.

---

## Technologies Used

- Python 3  
- Pandas for data manipulation  
- Matplotlib & Plotly for visualization  
- Scikit-learn for regression modeling  
- Jupyter Notebook for interactive development and reporting  

---
## How to Use

1. Clone the repository.  
2. Load your datasets into the `data/` folder.  
3. Run the notebook `sales_shrinkage_prediction.ipynb` to perform analysis and generate predictions.  
4. Visualize insights and export reports in HTML format for sharing.  
5. Optionally, use the trained model to predict shrinkage on new datasets.

---
#### TOP 10 Products by Inventory shrinkage
* <img width="1776" height="448" alt="image" src="https://github.com/user-attachments/assets/daf8ef73-21b8-46e4-8b5c-f85bd1f717fa" />
---
#### Model
* Model R² score: 0.9895746689563556
* Random Forest R²: 0.7687706838820284
* Gradient Boosting R²: 0.8382298875721109

 *Linear regression is better in compare dto both Random Forest and Gradient Boosting

 #### Residual Distribution
 <img width="1767" height="443" alt="image" src="https://github.com/user-attachments/assets/1c3db224-d8e9-4894-9204-da1c78a51c0b" />
 
 #### Residual vs Shrinkage
 <img width="1772" height="441" alt="image" src="https://github.com/user-attachments/assets/0d6c8e11-023d-41ff-b284-4a8b3490fcbe" />

 ---
#### Predicted shrinkage per Product
<img width="1771" height="449" alt="image" src="https://github.com/user-attachments/assets/e016e90c-84a9-44a0-b105-9981e687ec44" />


----

### Dashboard

<img width="291" height="71" alt="image" src="https://github.com/user-attachments/assets/07ed8de7-6a6d-4b00-87d3-16762600d7a7" />

<img width="1493" height="890" alt="image" src="https://github.com/user-attachments/assets/666a04d2-016e-48f9-8d9e-355f986044f5" />

----
Inventory Overview
<img width="1825" height="411" alt="image" src="https://github.com/user-attachments/assets/7038d1be-341b-4af6-ab87-8f824fa04ed4" />



## Insights & Business Impact

- **Top shrinkage products identified:** Helps prioritize inventory audits.  
- **Accurate shrinkage prediction:** Enables proactive stock management and loss reduction strategies.  
- **Returns analysis:** Provides insight into product quality or customer satisfaction issues.  
- **Interactive dashboards:** Facilitate easy monitoring of KPIs by business teams.

---

## Conclusion

This project demonstrates how combining sales, inventory, and return data can reveal hidden losses through shrinkage analysis. Predictive modeling empowers retailers to anticipate losses and optimize stock management, ultimately improving profitability.

---
