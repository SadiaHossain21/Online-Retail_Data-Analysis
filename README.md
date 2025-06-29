# Online Retail Data Analysis

A full-cycle data wrangling and analytics project using the **UCI Online Retail dataset**, showcasing skills in **Python**, **Pandas**, **SQL (PostgreSQL)**, **RFM Segmentation** and **Power BI** for customer analysis.  
This project demonstrates how raw e-commerce data can be cleaned, enriched, loaded into a database, and analyzed to uncover business insights.

---

## Objectives

- Clean messy real-world retail data with nulls, cancellations, and duplicates
- Create engineered features like cancellation flags
- Export cleaned data for SQL-based exploration
- Perform SQL analytics to answer business questions
- Segment customers using **RFM analysis** 
- Showed the insights in **Power BI** with connecting to the PostgreSQL DB

---

## Project Structure

| File | Description |
|------|-------------|
| `Data_Preparation.ipynb` | Python notebook for cleaning and transforming the dataset |
| `SQL_Queries.ipynb` | Analytical SQL queries for sales, orders, and returns |
| `RFM_Segmentation.ipynb` | RFM scoring and customer segmentation using SQL |

 **Dataset (on Kaggle)**:  
 [Online Retail Data – Raw & Cleaned](https://www.kaggle.com/datasets/sadia21121/online-retail-data-raw-cleaned)

---

## Data Cleaning (Python + Pandas)

- Parsed `InvoiceDate` as datetime
- Filled missing product descriptions with `"Unknown"`
- Cast `CustomerID` to int for consistency and filled the missing values with `"0"`
- Created `IsCancelled` flag (based on invoices starting with `"C"`)
- Removed invalid prices, quantities, and empty rows
- Exported cleaned dataset as `.csv`

> Notebook: `Data_Preparation.ipynb`

---

## SQL Analysis (PostgreSQL + SQLAlchemy)

After loading the cleaned dataset into PostgreSQL, various SQL queries were used to explore and analyze:

###  Key Insights Extracted

- Top 10 products by revenue  
- Country-wise orders, returns, and sales totals  
- Repeat vs one-time customer distribution  
- Average order value  
- Most active purchase hours  
- Cancellation rate by country  
- Most returned products  
- Customer Lifetime Value  
- Top 3 customers by country (using window functions)

> Notebook: `SQL_Queries.ipynb`

---

## RFM Segmentation

**RFM (Recency, Frequency, Monetary)** scoring was implemented in SQL to classify customers into meaningful segments:

- Scores ranked into quartiles using `NTILE(4)`
- Total RFM score and category code (e.g. `444`, `111`) calculated
- Customers labeled as:
  - **Loyal**
  - **Churned**
  - **New**
  - **Active**
  - **Potential Churners**

> Notebook: `RFM_Segmentation.ipynb`

---

## Tools Used

- **Python** (Pandas, NumPy)
- **SQL** (PostgreSQL)
- **SQLAlchemy** for database interaction
- **Jupyter Notebook** for analysis workflow
- **Excel** (initial file format)

---

## Sample Business Questions Answered

- Which customers bring the most revenue?
- How many orders are canceled, and from which countries?
- Which hours of the day are most active for purchasing?
- What is the average value of an order?
- Are customers buying repeatedly or only once?
- What are the most frequently returned products?
- Which segments are loyal vs. slipping away?

---

## Dataset Source

UCI Machine Learning Repository  
🔗 [https://archive.ics.uci.edu/ml/datasets/online+retail](https://archive.ics.uci.edu/ml/datasets/online+retail)

---

## Author

**Sadia Hossain**  
MSc Data Science | SQL • Python • Power BI  
sadiahossain2101@gmail.com  
[LinkedIn](https://www.linkedin.com/in/sadia-hossain-297993251/)
