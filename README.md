# Telecom Customer Churn Analysis Dashboard

This project presents an end-to-end churn analysis solution using **SQL Server for EDA**, **Power BI for data visualization**, and **machine learning (Random Forest)** for churn prediction.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

##  Tools & Technologies Used

- **SQL Server Management Studio (SSMS)** – For data cleaning and transformation
- **Power BI Desktop** – For interactive visual dashboards
- **Python (Jupyter Notebook)** – For machine learning using Random Forest
- **Excel/CSV** – For data storage and exports

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
#  Customer Churn Analysis Dashboard

This project presents an end-to-end churn analysis solution using **SQL Server for EDA**, **Power BI for data visualization**, and **machine learning (Random Forest)** for churn prediction.

---

## Tools & Technologies Used

- **SQL Server Management Studio (SSMS)** – For data cleaning and transformation
- **Power BI Desktop** – For interactive visual dashboards
- **Python (Jupyter Notebook)** – For machine learning using Random Forest
- **Excel/CSV** – For data storage and exports

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

##  Dataset Schema

The project uses a **single flat table**: `prod_Churn`, which contains customer-level telecom data.

📄 View full schema image:  
![Database Schema](assets/Database%20Schema.png)

| Column Name             | Description                              |
|-------------------------|------------------------------------------|
| Customer_ID             | Unique ID of customer                    |
| Gender, Age, Married    | Demographic info                         |
| State, Number_of_Referrals | Geographic & referral info          |
| Internet_Service, Phone_Service, Streaming_* | Services subscribed |
| Tenure_in_Months        | Customer tenure                          |
| Monthly_Charge, Total_Revenue, Refunds | Financial metrics        |
| Churn_Reason, Churn_Category, Customer_Status | Churn labels       |

There are **no relationships** – a single-table model was used.

--------------------------------------------------------------------------------------------------------------------------

##  SQL Data Exploration & Cleaning

All EDA and preparation were done in SQL Server:

- Checked for **null values**, **data distribution**
- Created **views** for Power BI based on customer status:
  - `vw_ChurnData` → for churn/stay analysis
  - `vw_JoinData` → for newly joined customers
- Cleaned nulls using `ISNULL()` and inserted into `prod_Churn`

[View SQL Scripts](sql/SQL%20Queries.docx)

---

##  Power BI Dashboard Overview

The Power BI report contains **3 pages**:

### Summary View  
![Summary](assets/Summary.png)
- Churn rate by **gender, age, tenure, internet type, payment method**
- Regional churn insights and service usage breakdowns

###  Churn Prediction View  
![Churn Prediction](assets/Churn%20Prediction.png)
- Churner count by demographics and tenure
- "Customers at Risk" table with revenue and referrals

----------------------------------------------------------------------------------------------------------------------------------------

## Machine Learning: Random Forest

Machine learning was performed in a separate **Jupyter Notebook** using:
- **Random Forest Classifier**
- Feature selection and label encoding
- Trained model to predict churners

[See Model Code](Churn%20Prediction%20Model.ipynb)  
[View Prediction Output](Predictions.xlsx)

-----------------------------------------------------------------------------------------------------------------------------------------

## Project Files

| File | Description |
|------|-------------|
| `Customer_Data.csv` | Raw input dataset |
| `SQL Queries.docx`  | SQL scripts for EDA, cleaning, views |
| `Churn Prediction Model.ipynb` | Python notebook for model building |
| `Prediction_Data.xlsx` | Prepared data with prediction results |
| `Summary.png`, `Churn Prediction.png` | Power BI dashboard screenshots |
| `Database Schema.png` | Table schema diagram from SSMS |

--------------------------------------------------------------------------------------------------------------------------------------

## How to Use This Project

1. Open `.pbix` file in Power BI Desktop (if shared separately)
2. Use `SQL Queries.docx` to reproduce database structure and cleaning
3. Run `Churn Prediction Model.ipynb` to explore the ML workflow
4. Analyze insights from screenshots or build your own visuals

--------------------------------------------------------------------------------------------------------------------------------------------

## Note

This project is for educational purposes only.  
Data used is anonymized or synthetic and does not represent real customers.

---------------------------------------------------------------------------------------------------------------------------------------------

## 🔗 Author

**Priyanka R**  
Feel free to connect via [LinkedIn](#) or reach out with questions!



