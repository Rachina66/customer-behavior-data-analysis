1.	Customer Behavior Analysis
End-to-end data analytics project analyzing retail customer shopping behavior using Python, SQL Server, and Power BI.

1.1 Overview
A retail company wants to better understand customer shopping behavior to improve sales, customer satisfaction, and long-term loyalty.
This project answers:
How can customer data be used to identify trends, improve customer engagement, and optimize marketing and product strategies?

1.2 Dataset
•	Source: Customer Shopping Behavior Dataset (Kaggle)
•	Rows: 3,900
•	Columns: 18
•	Includes customer demographics, purchase data, shipping details, discounts, and review ratings

1.3 Tools and Technologies
•	Python (Pandas, Matplotlib, Seaborn)
•	MS SQL Server LocalDB
•	SQLAlchemy and pyodbc
•	Power BI Desktop
•	Jupyter Notebook

1.4 Project Workflow
1. Data Loading
•	Loaded dataset using pandas
•	Explored structure with df.info() and df.describe()
•	Checked data types and column names

2. Data Cleaning
•	Found 37 missing values in review_rating column
•	Filled missing values using median per category to avoid bias
•	Renamed all columns to snake_case
•	Dropped promo_code_used column (duplicate of discount_applied)

3. Feature Engineering
•	Created age_group column (Young Adult, Adult, Middle-aged, Senior)
•	Created purchase_interval_days by converting frequency values into number of days

4. Connecting Python to MS SQL Server LocalDB
•	Used SQLAlchemy and pyodbc with Windows Authentication
•	No username or password required
•	Loaded cleaned DataFrame into customer table in customer_shopping_behavior database

5. SQL Business Analysis
Answered 10 business questions:
Q1. Revenue by gender
•	Compared male vs female total revenue
Q2. Discount users above average spend
•	Identified customers using discounts but spending above average
Q3. Top 5 products by review rating
•	Found highest-rated products
Q4. Standard vs Express shipping
•	Express shipping customers spend more than standard
Q5. Subscription vs non-subscription spending
•	Similar average spend between both groups
Q6. Top 5 products by discount rate
•	Products that rely most on discounts
Q7. Customer segmentation
•	Loyal: 3,116 customers
•	Returning: 701 customers
•	New: 83 customers
Q8. Top 3 products per category
•	Best-selling products within each category
Q9. Repeat buyers vs subscription
•	2,518 repeat buyers are not subscribed
•	958 repeat buyers are subscribed
Q10. Revenue by age group
•	Young Adult: $62,143
•	Middle-aged: $59,197
•	Adult: $55,978
•	Senior: $55,763

6. Power BI Dashboard
•	Connected MS SQL Server LocalDB directly to Power BI
•	Created DAX measures for KPIs
•	Built interactive dashboard with Teal and Navy theme
KPI Cards
•	Total Customers: 3.9K
•	Total Revenue: $233K
•	Average Purchase Amount: $59.76
•	Average Review Rating: 3.75
Charts
•	Revenue by Category
•	Sales by Category
•	Revenue by Age Group
•	Sales by Age Group
•	Subscription Status Distribution
Slicers
•	Gender
•	Category
•	Subscription Status
•	Shipping Type

1.5 Key Insights
•	Young Adults generate the highest revenue ($62,143)
•	Express shipping customers spend more than standard shipping
•	Majority of customers are loyal (3,116 out of 3,900)
•	2,518 repeat buyers are not subscribed → subscription strategy needs improvement
•	Subscribed and non-subscribed customers show similar spending behavior

1.6 How to Run
1. Clone the repository
git clone https://github.com/Rachina66/customer-behavior-analysis.git
2. Install required libraries
pip install pandas sqlalchemy pyodbc matplotlib seaborn
3. Run the project
•	Open and run the Jupyter Notebook
•	Connect to SQL Server LocalDB
•	Open .pbix file in Power BI Desktop

1.7 Author
Rachina Gosai
rachina.gosai@gmail.com
