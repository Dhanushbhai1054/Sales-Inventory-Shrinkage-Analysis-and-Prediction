# Sales-Inventory-Shrinkage-Analysis-and-Prediction

Inventory Shrinkage Analysis & Prediction

This project analyzes retail inventory shrinkage by combining datasets on stock, sales, and returns to identify product loss patterns. Using data cleaning, aggregation, and exploratory analysis, it builds predictive models (Linear Regression, Random Forest, Gradient Boosting) to forecast shrinkage. The project includes interactive visualizations and a dashboard to help businesses monitor inventory loss, improve operational efficiency, and reduce financial impact.
## Dataset Description

Three main datasets are used in this project:

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
