# Ecommerce Sales Dashboard

This project performs an **exploratory data analysis (EDA)** and **visual analysis** on an online retail dataset to uncover sales trends, customer behavior, and geographic revenue distribution.

The analysis is implemented in a **Jupyter Notebook (`.ipynb`)** using Python libraries such as Pandas, NumPy, and Plotly.

---

## Dataset

This project uses the **Online Retail Dataset**, which is publicly available.

Source:  
https://www.kaggle.com/datasets/vijayuv/onlineretail


- **File used:** `online_retail.csv`
- **Rows:** 541,909  
- **Columns:** 8
  
Download the dataset and save it as `online_retail.csv` in the project directory before running the notebook.

### Key Features
- InvoiceNo  
- StockCode  
- Description  
- Quantity  
- InvoiceDate  
- UnitPrice  
- CustomerID  
- Country  

---

## Tools & Libraries Used

- **Python**
- **Pandas** – data manipulation and cleaning  
- **NumPy** – numerical computations  
- **Plotly Express & Graph Objects** – interactive visualizations  

---

## Project Workflow

### 1. Data Loading & Inspection
- Loaded dataset with proper encoding
- Checked shape, data types, and summary statistics
- Identified missing values

### 2. Data Cleaning
- Removed records with missing `CustomerID`
- Created a new feature:  
  **`TotalSales = Quantity × UnitPrice`**

### 3. Outlier Detection
- Used **Interquartile Range (IQR)** method to detect anomalies
- Separated:
  - Standard transactions
  - Anomalous transactions

### 4. Sales Trend Analysis
- Converted invoice dates to datetime format
- Performed **Month-over-Month (MoM) growth analysis**
- Calculated monthly total sales and growth percentage

### 5. Data Visualization
- **Interactive world choropleth map** showing revenue by country
- **Scatter plot** showing relationship between unit price and quantity purchased
- Visuals created using Plotly for interactivity

---

## 📈 Key Insights

- Majority of revenue originates from a small number of countries
- Sales show seasonal fluctuations with sharp month-over-month changes
- High-value outliers significantly impact total revenue
- Customer purchase behavior varies strongly with unit price

---

## Notes

- A Plotly–Kaleido version warning may appear for static image export  
  (interactive plots still work correctly inside the notebook)

---

## How to Run

1. Clone the repository  
2. Install required libraries:
   ```bash
   pip install pandas numpy plotly
