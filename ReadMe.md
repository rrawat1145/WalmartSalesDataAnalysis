#Aim: 
This project aims to explore the Walmart Sales data using MYSQL to understand top performing branches and products, sales trend of different products, customer behavior. The aims are to study how sales strategies can be improved and optimized. 

##About Data: 
The dataset was obtained from the Kaggle Walmart Sales Forecasting Competition [Download Here] (https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting). This dataset contains sales transactions from three different branches of Walmart, respectively located in Mandalay, Yangon and Naypyitaw. The data contains 17 columns and 1000 rows

#Analysis List:
1. Product Analysis: Conduct analysis on the data to understand the different product lines, the products lines performing best and the product lines that need to be improved.
2. Sales Analysis: This analysis aims to answer the question of the sales trends of product. The result of this can help use measure the effectiveness of each sales strategy the business applies and what modifications are needed to gain more sales.
3. Customer Analysis: This analysis aims to uncover the different customers segments, purchase trends and the profitability of each customer segment.

#Approach Used:

##(Steps are also added to the code list as comments for reference.

##STEP I: Creating a database
1. Data Wrangling: This is the first step where inspection of data is done to make sure NULL values and missing values are detected and data replacement methods are used to replace, missing or NULL values.
2. Build a database and then creating a table and inserting the data.
3. There are no null values in our database as in creating the tables, we set NOT NULL for each field, hence null values are filtered out.

##STEP II: Adding new columns
1. Add a new column named time_of_day to give insight of sales in the Morning, Afternoon and Evening. This will help answer the question on which part of the day most sales are made.
2. Add a new column named day_name that contains the extracted days of the week on which the given transaction took place (Mon, Tue, Wed, Thur, Fri). This will help answer the question on which week of the day each branch is busiest.
3. Add a new column named month_name that contains the extracted months of the year on which the given transaction took place (Jan, Feb, Mar). Help determine which month of the year has the most sales and profit.

##STEP III: Business questions to answer are as under:

Q1.	How many unique cities does the data have?
Q2.	In which city is each branch?
Q3.	How many unique product lines does the data have?
Q4.	What is the most common payment method?
Q5.	What is the most selling product line?
Q6.	What is the total revenue by month?
Q7.	What month had the largest COGS?
Q8.	What product line had the largest revenue?
Q9.	What is the city with the largest revenue?
Q10.	What product line had the largest VAT?
Q11.	What are the total sales in each product line?  
Q12.	Which branch sold more products than average product sold?
Q13.	What is the most common product line by gender?
Q14.	What is the average rating of each product line?
Q15.	Number of sales made in each time of the day per weekday
Q16.	Which of the customer types brings the most revenue?
Q17.	Which city has the largest tax percent/ VAT (Value Added Tax)?
Q18.	Which customer type pays the most in VAT?
Q19.	How many unique customer types does the data have?
Q20.	How many unique payment methods does the data have?
Q21.	What is the most common customer type in terms of quantity?
Q22.	Which customer type buys the most?
Q23.	What is the gender of most of the customers?
Q24.	What is the gender distribution per branch?
Q25.	Which time of the day do customers give most ratings?
Q26.	Which time of the day do customers give most ratings per branch?
Q27.	Which day of the week has the best avg ratings?
Q28.	Which day of the week has the best average ratings per branch?

SQL create table code:

CREATE TABLE IF NOT EXISTS sales(
invoice_id VARCHAR(30) NOT NULL PRIMARY KEY,
branch VARCHAR(5) NOT NULL,
city VARCHAR(30) NOT NULL,
customer_type VARCHAR(30) NOT NULL,
gender VARCHAR(10) NOT NULL, 
product_line VARCHAR(100) NOT NULL,
unit_price DECIMAL(10, 2) NOT NULL,
quantity INT NOT NULL,
VAT	FLOAT NOT NULL,
total DECIMAL(12, 4) NOT NULL,
date DATE NOT NULL,
time TIME NOT NULL,
payment_method VARCHAR(15) NOT NULL,
cogs DECIMAL(10, 2) NOT NULL,
gross_margin_pct FLOAT,
gross_income DECIMAL(12, 4) NOT NULL,
rating FLOAT NOT NULL
);

For rest of the codes please refer to the Code file.