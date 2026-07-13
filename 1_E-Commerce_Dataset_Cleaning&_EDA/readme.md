
### 🛒 E-commerce Sales Analysis Summary Report

#### 🎯 Project Purpose

The purpose of this analysis is to explore sales performance, customer purchasing patterns, and product trends within the online retail dataset. The analysis aims to identify key revenue drivers, understand customer behavior, and uncover insights that can support data-driven business decisions.

---
#### 🛠️ Tools Used

- 💻 **Visual Studio Code (VS Code)**  
  Used as the development environment for writing, organizing, and executing Python scripts and Jupyter notebooks.

- 📓 **Jupyter Notebook**  
  Used for data cleaning, exploratory data analysis (EDA), statistical analysis, and creating data visualizations.

- 🐍 **Python**  
  Used as the main programming language for data processing, analysis, and visualization.

#### 📚 Python Libraries Used

- 🐼 **Pandas**  
  Used for data cleaning, data manipulation, filtering, and exploratory analysis.

- 🔢 **NumPy**  
  Used for numerical computations and handling mathematical operations.

- 📊 **Matplotlib**  
  Used for creating charts and visualizing patterns in the data.

#### 🧹 Data Cleaning Summary

The dataset was examined for data quality issues, including incorrect data types, missing values, invalid values, and outliers. The following cleaning steps were performed:

| 🔍 Issue Identified | ✅ Action Taken |
|--------------------|----------------|
| **Data type issues in two columns:** `CustomerID` was stored as `float64` instead of a string, and `InvoiceDate` was stored as an object/string instead of datetime format. | Converted `InvoiceDate` to datetime format using `pd.to_datetime()` and changed `CustomerID` to string format using `astype(str)`. |
| **Missing values in `Description` and `CustomerID` columns:** `Description` had **0.27%** missing values, while `CustomerID` had approximately **33.2%** missing values. | Removed records with missing `Description` values due to their small proportion. For `CustomerID`, missing values were replaced with **"Missing"** to avoid losing a significant portion of the dataset. |
| **Negative values identified in the `UnitPrice` column (2 records).** | Investigated the records and corrected the values by converting them to their appropriate positive prices. |
| **Negative values identified in the `Quantity` column (1.8% of records).** | The values were retained because they represent valid business transactions, such as returned or cancelled orders. |
| **Zero values identified in the `UnitPrice` column (1,000 records).** | The values were retained because they represent a small portion of the dataset and may correspond to free items, promotional items, or transaction adjustments. These values do not affect revenue calculations since their price is zero. |
| **Outliers identified in the `Quantity` column using box plot analysis.** | Outliers were investigated and retained because they represented valid transactions, including bulk purchases and returned/cancelled items, rather than data entry errors. |

#### Summary

After cleaning, the dataset was standardized by correcting data types, handling missing values, investigating invalid entries, and reviewing outliers. The cleaning process improved data consistency while preserving important transaction information needed for further exploratory data analysis.

### 📊 Key Insights

#### 🌍 1. The United Kingdom generated the highest revenue for the online retail store.

* The **United Kingdom** was the largest revenue-generating market, contributing approximately **$8.2 million** in sales.
* This was significantly higher than the **Netherlands**, the second-highest revenue-generating country, which generated approximately **$0.3 million**.
* This indicates that the business is highly dependent on the UK market for revenue generation.

---
![alt text](<Top Revenue Generating Country.png>)

#### 📈 2. Monthly sales increased throughout the year.

* Sales were relatively lower at the beginning of the year but gradually increased over time.
* The highest sales were recorded in **November**, indicating increased customer demand toward the end of the year.
* This trend may suggest the influence of seasonal shopping patterns and holiday-related purchases.

---
1_E-Commerce_Dataset_Cleaning&_EDA/Monthly sales trend.png

#### 🏆 3. Dotcom Postage was the highest revenue-generating product.

* **Dotcom Postage** generated the highest revenue, followed closely by the **Regency Cakestand 3 Tier**.
* These products contributed significantly to overall sales performance and represent important revenue drivers for the business.
* However, postage-related items should be interpreted separately from physical products when evaluating product performance.

---
![alt text](<Top selling Products.png>)
#### 👥 4. Missing CustomerID values limit customer-level analysis.

* Approximately **33.33%** of transactions have missing `CustomerID` values, making it challenging to identify the store's most valuable customers.
* Transactions without customer identification contributed approximately **$1.4 million** in revenue.
* Due to these missing values, customer purchasing behavior, customer lifetime value, and customer segmentation cannot be accurately analyzed.

---
![alt text](<Top Customers.png>)

#### 🛍️ 5. World War 2 Gliders Asstd Designs was the most purchased product.

* **World War 2 Gliders Asstd Designs** recorded the highest number of units purchased.
* The top five most purchased products have relatively similar purchase volumes, showing that demand is distributed across multiple products.
* This suggests that customers purchase a wide variety of products rather than relying on a single popular item.

---
![alt text](<most purchased product.png>)

### ✅ Conclusion

The analysis shows that the online retail store's revenue is primarily driven by the **United Kingdom market**, with sales showing strong growth toward the end of the year due to possible seasonal demand. While a few products contribute significantly to revenue, customer purchasing patterns indicate demand across a wide range of products.

However, missing customer identification data limits deeper customer behavior analysis, such as identifying high-value customers and creating customer segments. Improving customer data collection would allow the business to better understand customer preferences, improve marketing strategies, and increase customer retention.
