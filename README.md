# Bank-data-analysis
Analyze different types of transactions and customers
Banking Transaction & Customer Insights Dashboard
 Project Overview
This project involves a comprehensive analysis of a banking dataset containing 20,000 financial transactions. The goal is to transform raw transactional data into an interactive Power BI dashboard that provides actionable insights into financial performance, customer behavior, and risk management.
The dashboard helps stakeholders monitor high-level KPIs, track cash flow dynamics, and identify high-risk customer segments using advanced analytical visuals
.
 Dataset Description
The analysis is based on the Banking_Transactional_Dataset, which includes detailed information across 19 columns
:
Transaction Metadata: TransactionID, CustomerID, TransactionDate, and Channel (ATM, Branch, Mobile, Online)
.
Financial Details: Amount, Currency (EUR/USD), and TransactionType (Deposit, Withdrawal, Transfer, Card Payment, Fee, Loan Payment)
.
Product Info: ProductCategory (Checking, Savings, Credit Card, Mortgage, Loan) and ProductSubcategory
.
Fee Structure: CreditCardFees, InsuranceFees, and LatePaymentAmount
.
Customer Profile: CustomerScore (credit rating), MonthlyIncome, and CustomerSegment
.
Geography: BranchCity, BranchLat, and BranchLong
.
 Tools & Technologies
Microsoft Power BI Desktop: The primary environment for report building
.
Power Query (M Language): Used for the ETL (Extract, Transform, Load) process and data cleaning
.
DAX (Data Analysis Expressions): Used to create complex measures and calculated columns
.
Data Dictionary: Utilized for standardizing field definitions
.
 Project Workflow
Data Ingestion: Importing the CSV dataset into Power BI
.
ETL & Transformation:
Normalizing currencies by converting USD transactions to EUR (1 USD = 0.92 EUR) to ensure accurate aggregation.
Standardizing date formats and creating a dedicated Calendar Table for time-intelligence analysis
.
Pivoting and flattening tables using the Power Query Editor where necessary for advanced visuals
.
Data Modeling: Establishing relationships between the transaction data and the calendar hierarchy
.
DAX Development: Building measures for Total Transactions, Unique Customers, Total Fee Revenue, and Actual Cash Flow.
Dashboard Design: Organizing visuals into a 4-level information hierarchy for professional storytelling
.
 Power BI Development Details
Data Cleaning & ETL
Currency Normalization: Implemented a SUMX measure to calculate totals across multiple currencies.
Type Casting: Ensured all fee-related columns were recognized as decimal numbers for precise calculation
.
Key DAX Measures
Total Transactions: COUNT('Banking Data'[TransactionID]) — returns the total volume of 20,000 records.
Total Actual Cash Flow: A comprehensive measure summing Amount plus all additional fees (CreditCardFees, InsuranceFees, LatePaymentAmount).
Unique Customers: DISTINCTCOUNT('Banking Data'[CustomerID]) to identify the unique client base .
Interactive Dashboard Design
The dashboard follows a structured layout
:
Level 1 (KPI Cards): Displays high-level totals like Total Amount, Total Fees, and Average Credit Score
.
Level 2 (Trends & Structure): A Line Chart for monthly transaction dynamics and a Donut Chart for customer segment distribution
.
Level 2.5 (Geography & Engagement): A Map visual showing branch performance by city and a Bar Chart comparing transaction channels
.
Level 3 (Advanced Analytics): A Decomposition Tree used for root-cause analysis of late payments across categories
.
 Key Insights
Revenue Streams: Identified that total revenue is significantly impacted by "hidden" fees (Credit Card, Insurance) and late payment penalties, rather than just transaction amounts.
Channel Preference: Discovered which channels (e.g., Mobile vs. ATM) handle the highest volume of transactions .
Risk Profiles: Mapped late payment amounts to specific income segments to assist the bank's risk department .
 How to Run the Project
Open the .pbix file in Power BI Desktop.
If the data source is disconnected, go to Transform Data > Data Source Settings and point to your local copy of Banking_Transactional_Dataset.csv.
Click Refresh to reload the visuals.
 Future Improvements
Predictive Modeling: Using Power BI's built-in AI to forecast future transaction volumes.
Dynamic Exchange Rates: Connecting to a live API for real-time currency conversion instead of a static rate.
What-if Analysis: Adding parameters to simulate the impact of fee changes on total bank revenue.
