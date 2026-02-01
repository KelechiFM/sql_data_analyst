# Retail Sales SQL Analysis Project

[cite_start]**Author:** Okoli Kosisochukwu Anastesia [cite: 2]  
[cite_start]**Tools:** SQL Server Management Studio (SSMS) [cite: 19, 44]

## 1. Introduction
[cite_start]This project demonstrates a complete retail sales analytics workflow using SQL Server[cite: 20]. [cite_start]In the competitive retail sector, precise data analysis is required to assess performance, predict trends, and understand customer behavior[cite: 16]. 

[cite_start]The project evolves a raw CSV dataset into a cleaned, structured, and analyzed sales database[cite: 39].

## 2. Objectives
* [cite_start]**Database Setup:** Create a retail sales database and import raw transactional data[cite: 23].
* [cite_start]**Data Cleaning:** Identify and remove null or invalid values to ensure data integrity[cite: 24].
* [cite_start]**Exploratory Data Analysis (EDA):** Uncover initial trends, distributions, and customer demographics[cite: 25].
* [cite_start]**Business Analysis:** Solve specific business questions regarding sales performance and customer habits[cite: 26].

## 3. Project Scope & Workflow

### Step 1: Database Setup
* [cite_start]**Database Creation:** A database named `retail_sales` was created[cite: 46].
* [cite_start]**Data Import:** The `retail_sales TB.csv` file was imported using the "Import Flat File" wizard in SSMS[cite: 67, 71].
* [cite_start]**Schema:** The table includes columns for `transaction_id`, `sale_date`, `sale_time`, `customer_id`, `gender`, `age`, `category`, `quantity`, `price_per_unit`, `cogs`, and `total_sale` [cite: 102-127].

### Step 2: Data Cleaning
* [cite_start]**Null Check:** The dataset was checked for null values in critical columns (age, quantity, price, cogs, etc.)[cite: 269].
* [cite_start]**Data Cleaning:** Records containing null values were deleted to avoid distorting analysis[cite: 327].
    ```sql
    DELETE FROM [retail_sales TB.csv]
    WHERE age IS NULL OR quantity IS NULL OR total_sale IS NULL; [cite_start]-- (Excerpt) [cite: 328]
    ```

### Step 3: Exploratory Data Analysis (EDA)
Initial queries were run to understand the dataset structure:
* [cite_start]**Total Records:** Validated the count of valid transactions[cite: 382].
* [cite_start]**Date Range:** Identified the start and end dates of sales data[cite: 445].
* [cite_start]**Categories:** Listed distinct product categories (e.g., Clothing, Electronics, Beauty)[cite: 506].
* [cite_start]**Demographics:** Analyzed gender distribution and customer age (min, max, average)[cite: 566, 626].

## 4. Business Analysis (Key Questions)
The following business questions were answered using SQL queries:

1.  [cite_start]**Sales on Specific Date:** Retrieve all columns for sales made on `2022-11-05`[cite: 696].
2.  [cite_start]**High Quantity Orders:** Retrieve transactions for 'Clothing' in Nov 2022 with quantity > 4[cite: 836].
3.  [cite_start]**Category Performance:** Calculate total sales (revenue) for each category[cite: 905].
4.  [cite_start]**Customer Demographics:** Find the average age of customers who purchased from the 'Beauty' category[cite: 968].
5.  [cite_start]**High-Value Transactions:** Find all transactions where `total_sale` is greater than 1000[cite: 1029].
6.  [cite_start]**Gender & Category analysis:** Count the total number of transactions made by each gender in each category[cite: 1163].
7.  [cite_start]**Monthly Trends:** Calculate average monthly sales and identify the best-selling month in each year[cite: 1239].
8.  [cite_start]**Top Customers:** Identify the top 5 customers based on highest total spending[cite: 1356].
9.  [cite_start]**Customer Reach:** Find the number of unique customers who purchased items from each category[cite: 1427].
10. [cite_start]**Shift Analysis:** Categorize sales into shifts (Morning, Afternoon, Evening) and count orders per shift[cite: 1494].

## 5. Key Insights & Recommendations
Based on the analysis, the following actions are recommended:
* [cite_start]**Marketing:** Prioritize funding for categories with the highest overall sales[cite: 1579].
* [cite_start]**Demographics:** Target younger demographics for Beauty products on relevant platforms[cite: 1581].
* [cite_start]**High-Value Strategy:** Consider premium packages or protection plans for transactions over 1000[cite: 1582].
* [cite_start]**Seasonality:** Increase stock and staffing during peak months (November-December)[cite: 1584].
* [cite_start]**Operations:** Adjust staffing for afternoon shifts, which show peak traffic[cite: 1586].

## 6. Project Script
[cite_start]For the full SQL script and dataset, refer to the [Project Drive Link](https://drive.google.com/file/d/1BG0bSlaOiXNTV4fhXBEuFXRPExaRDaMV/view?usp=drive_link)[cite: 1588].