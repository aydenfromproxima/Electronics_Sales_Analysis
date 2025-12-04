# Electronics Sales Analysis – April 2019

A complete exploratory data analysis (EDA) on more than 18,000 retail transactions to understand product performance, customer purchasing behavior, and city-wise sales patterns.

---

## 1. Dataset Overview

The dataset includes the following fields:

- Order ID  
- Product  
- Quantity Ordered  
- Price Each  
- Order Date  
- Purchase Address  

### Key Notes

- 59 completely empty rows removed  
- 56 duplicate entries removed  
- Final dataset size: **18,267 rows × 12 columns** after data cleaning and feature engineering

---

## 2. Data Preparation

### Cleaning Steps
- Removed rows containing all null values  
- Removed duplicate rows  

### Feature Engineering
- Extracted:
  - `Date`
  - `Month`
  - `Hour`
  from the `Order_Date` column  
- Split `Purchase Address` into:
  - House Number  
  - City  
  - Pin Code  
- Converted data types:
  - `Quantity_Ordered` → integer  
  - `Price_Each` → float  
  - Date fields → datetime  
- Created a calculated column:
  - `Sales = Quantity_Ordered × Price_Each`

---

## 3. Analysis and Visualizations

### 3.1 Monthly Sales Summary
Total revenue:

| Month | Revenue ($) |
|-------|-------------|
| April | 3,384,047.56 |
| May   | 10,559.29    |

(Almost all data belongs to April.)

---

### 3.2 City-wise Sales Distribution

Highest order volumes:

| City           | Orders |
|----------------|--------|
| San Francisco  | 4434   |
| Los Angeles    | 3021   |
| New York City  | 2429   |
| Boston         | 1915   |
| Atlanta        | 1470   |

San Francisco leads in both sales volume and revenue.

---

### 3.3 Peak Purchase Hours

Key observations:

- Highest activity:
  - **10 AM to 1 PM**
  - **6 PM to 8 PM**
- Very low activity:
  - **2 AM to 5 AM**
- Orders begin rising around **7 AM** and decline after **9 PM**

---

### 3.4 Product-Level Performance

#### By Number of Orders
Top frequently purchased items:
- USB-C Charging Cable  
- AAA Batteries  
- AA Batteries  
- Wired Headphones  

Low-cost, high-frequency items dominate volume.

#### By Revenue Generated
Top revenue-generating products:
- MacBook Pro Laptop  
- iPhone  
- Google Phone  
- Bose SoundSport Headphones  

High-value electronics drive the majority of total revenue.

---

## 4. Key Insights

- Customer activity peaks around late morning and early evening  
- San Francisco, LA, and NYC dominate overall sales  
- Accessories account for most orders, but high-end electronics produce most revenue  
- Address parsing enables detailed geographic insights  
- The dataset primarily represents April sales, limiting cross-month comparison

---

## 5. Technologies Used

- Python  
- Pandas  
- NumPy  
- Seaborn  
- Matplotlib  

---

## 6. How to Run This Project

### Clone the Repository
``bash
git clone https://github.com/yourusername/ElectronicsSalesAnalysis.git 
### Install Dependencies
pip install pandas numpy matplotlib seaborn

### Launch the Notebook
jupyter notebook Electronics_Sales_Analysis.ipynb

## 7. Future Enhancements

Add geospatial heatmaps for city/state-level analysis

Build forecasting models for sales prediction

Implement market-basket analysis for product bundling insights

Create an interactive Streamlit or Power BI dashboard

## 8. Contributing

Contributions are welcome.
Feel free to add new analyses, visualizations, or improvements.

## 9. Support

If this repository helped you, consider giving it a star.
