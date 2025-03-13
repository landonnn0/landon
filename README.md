# MIST4610-Project1-Group7

61608 Group 7


## Database information:

- Allmond, Chandler [@Chandler Allmond](https://github.com/chandlerallmond)
- Barton, Nick [@Nick Barton](https://github.com/nicholasbarton1)
- Kamdar, Manav [@Manav Kamdar](https://github.com/manavk2004)
- Sengaphone, Vincent [@Vincent Sengaphone](https://github.com/sengaphone)
- Wilson, Landon [@Landon Wilson](https://github.com/landonnn0)

## Problem Description:
Retail technology businesses, such as Best Buy, face challenges in efficiently managing inventory, sales transactions, and product categorization, and without an organized database system, they may encounter difficulties such as overstocking or understocking due to poor inventory tracking, inefficient sales tracking leading to unclear insights on employee performance and product demand, difficulty in categorizing products which slows down retrieval and impacts customer service, and a lack of visibility into sales trends making it harder for management to optimize stock levels and pricing strategies. To address these challenges, the Electronic Product Database is designed as a comprehensive inventory and sales tracking system that will store detailed product information—including descriptions, pricing, warranty periods, and brand associations—track real-time inventory status, restock dates, and reorder quantities, facilitate sales transactions by recording employee sales contributions, transaction amounts, and payment methods, and enable sales analysis, allowing management to identify top-selling products, evaluate employee performance, and forecast future demand, thereby improving inventory accuracy, sales efficiency, and data-driven decision-making to enhance overall operations.

## Data Model:
The Electronic Product Database is designed to manage the inventory and sales of an electronics retail business. This data model provides a structured way to store and retrieve information about electronic products, their availability, and their categorization. The electronic_product table serves as the core of the model, linking products to their respective brands and categories through the brand_name and type_of_device tables. Additionally, the inventory table ensures that stock levels and restocking requirements are efficiently tracked, preventing shortages and optimizing supply chain operations.
The sales transaction process is handled through the sales_transaction and sales_transaction_product tables, which record transaction details, payment methods, and the number of products sold. Each sale is associated with an employee, stored in the employee table, allowing management to track individual employee contributions to sales. This structure ensures that every transaction is linked to both the products being sold and the employees processing the sales, making it easier to evaluate performance and analyze revenue trends.
By integrating inventory, sales, and employee management, this database provides businesses with real-time insights into product performance, stock availability, and financial transactions. The structured relationships between tables allow for streamlined data retrieval, enabling managers to make data-driven decisions regarding restocking, sales strategies, and employee performance evaluations. This system ultimately helps improve operational efficiency, profitability, and customer satisfaction by ensuring that products are always available and transactions are accurately recorded.


<img width="900" alt="Screenshot 2025-03-13 at 12 08 05 PM" src="https://github.com/user-attachments/assets/1231dd62-08f9-4764-97e3-30b2fd0f4ef6" />

## Data Dictionary:
<img width="900" alt="Screenshot 2025-03-13 at 12 11 11 PM" src="https://github.com/user-attachments/assets/93eacbe0-79e0-4312-933a-92df6080525a" />

<img width="900" alt="Screenshot 2025-03-13 at 12 14 34 PM" src="https://github.com/user-attachments/assets/c09c1e67-be4b-4cc5-ba0f-052602fa86fe" />

<img width="900" alt="Screenshot 2025-03-13 at 12 15 33 PM" src="https://github.com/user-attachments/assets/24b9ca42-e8a0-4f46-841d-4e1825b0c5d0" />

<img width="900" alt="Screenshot 2025-03-13 at 12 16 09 PM" src="https://github.com/user-attachments/assets/88c7377b-cbe3-4324-aee3-aac7ad058732" />

<img width="900" alt="Screenshot 2025-03-13 at 12 16 45 PM" src="https://github.com/user-attachments/assets/4818339b-f78d-49b9-9e78-e9113182d978" />

<img width="900" alt="Screenshot 2025-03-13 at 12 17 46 PM" src="https://github.com/user-attachments/assets/382bc281-a158-4883-b6ff-36c95721a58a" />

<img width="900" alt="Screenshot 2025-03-13 at 12 18 20 PM" src="https://github.com/user-attachments/assets/69bc0239-f3e4-499a-ad27-a51843946b58" />

## Queries:
1. Low Sotck Alert / High Stock Alert

This query identifies products with low stock levels and high stock levels to help businesses manage inventory efficiently. The low stock alert retrieves products with a stock quantity of 30 or less, ensuring that managers restock them before they run out. The high stock alert retrieves products with a stock quantity greater than 50, helping managers avoid excessive inventory that could lead to high storage costs or markdowns. Both queries order the results in ascending order of stock quantity for better visibility.
<img width="900" alt="Screenshot 2025-03-13 at 12 26 48 PM" src="https://github.com/user-attachments/assets/45f8cff2-0705-4f20-b3da-ca0c848f88b8" />
Managers can use this query to maintain balanced stock levels by ensuring that fast-selling products are restocked in time while preventing overstocking of slow-moving items. This helps businesses reduce waste, improve cash flow, and optimize inventory space, leading to better profitability and operational efficiency.

2. Best Selling Products

This query retrieves the top 5 best-selling products based on the total quantity sold. The results are sorted in descending order by sales volume.
<img width="900" alt="Screenshot 2025-03-13 at 12 35 56 PM" src="https://github.com/user-attachments/assets/fae7f2f3-5545-46c4-9e0c-51ddfb1275ad" />
Managers can identify high-demand products, allowing them to prioritize restocking and promotional efforts.

3. Total Revenue by Product Category

This query calculates the total sales revenue for each product category while filtering out categories that generate less than the average revenue of all categories. It first groups transactions by product category to compute total revenue and then applies a HAVING clause to retain only those categories that exceed the average revenue. A subquery is used to determine the overall average category revenue, ensuring that the analysis focuses on high-performing product categories.
<img width="900" alt="Screenshot 2025-03-13 at 12 58 20 PM" src="https://github.com/user-attachments/assets/311596f0-dbef-4ea1-8c4d-13025ef701c7" />
Managers can use this query to identify high-performing product categories that generate above-average revenue. By filtering out lower-performing categories, businesses can allocate more resources to profitable categories, optimize inventory planning, and adjust marketing strategies for better financial outcomes.

4. Top 3 Most Profitable Brands

This query joins the sales transaction, sales transaction for products, electronic product, and brand name tables then groups it by brand name then order by total revenue. Then we set the limit to 3 in order to show only the top 3 brands by revenue.
<img width="900" alt="Screenshot 2025-03-13 at 12 38 39 PM" src="https://github.com/user-attachments/assets/3188fd0a-7e24-4836-80f0-043717acf890" />
If a store wanted to maximize revenue by stocking the brands from which consumers were purchasing most from, this code would be beneficial to visualize which brands sat at the top of the revenue chart.

5. Employees Sales Performance

This query shows show each of the employee’s sales performance and gives basic information including their name and employee id
<img width="900" alt="Screenshot 2025-03-13 at 12 40 22 PM" src="https://github.com/user-attachments/assets/917fd3e4-7b9a-4131-aa78-8df12ae869c6" />
Managers can use this to gauge whether employees are meeting the standards that the company has set for itself. Having a clear and concise table showing the level of performance each employee brings into the company can allow managers to pinpoint those who may need extra assistance, and give the proper guidance for success. Comparing the performance of each employee overtime can allow the managers to make logical decisions to keep employees, fire employees, give bonuses, etc.

6. Monthly Sales Trends

This query displays the year, month, and total sales revenue for each month. The results are grouped by month and sorted in descending order to show the most recent months first.
<img width="900" alt="Screenshot 2025-03-13 at 12 42 10 PM" src="https://github.com/user-attachments/assets/d278608e-3bd8-4a7d-bbb7-09278a5c9e5c" />
Managers can use this query to analyze sales trends over time, identifying seasonal patterns and peak sales months. This insight helps businesses make data-driven decisions about inventory management, pricing strategies, and marketing campaigns to maximize revenue.

7. Total Sales Transactions

This query retrieves the total number of transactions in the system.
<img width="900" alt="Screenshot 2025-03-13 at 12 43 29 PM" src="https://github.com/user-attachments/assets/c969d3e2-ab4e-45d4-afc9-db58a8f9db00" />
Gives managers a quick snapshot of overall sales activity.

8. List of All Employees

This query retrieves basic employee details, sorted alphabetically by last name.
<img width="900" alt="Screenshot 2025-03-13 at 12 45 29 PM" src="https://github.com/user-attachments/assets/667cdd86-26fb-4643-92eb-c1e13d862641" />
Provides a quick reference for employee records.

9. Most Used Payment Method

This query finds the most frequently used payment methods.
<img width="900" alt="Screenshot 2025-03-13 at 12 47 11 PM" src="https://github.com/user-attachments/assets/ccd753fd-c0be-4f41-9349-644ac4e2c208" />
Helps managers analyze customer payment preferences.

10. Average Transaction Value of Each Customer

This query shows the average transaction value of each customer, meaning the average amount that a customer will spend.
<img width="900" alt="Screenshot 2025-03-13 at 1 07 57 PM" src="https://github.com/user-attachments/assets/270ea593-780c-4a71-8a1f-8ce85c7217be" />
While this code is quite simple, managers can use this in a variety of ways. Taking a sample set of a few months and using it as a barometer for the following months can allow managers to see if there are fluctuations in the amount that customers usually spend. If significant fluctuations occur during certain parts of the year, managers can conclude that their product/service may have a seasonality component to it. If suddenly consumers start spending less, there may be new competition that has entered the market that the manager may be unaware of. If consumers are buying a lot of product, but there’s a disconnect with the transaction value, the product simply may not be priced high enough

## Database information:
<img width="900" alt="Screenshot 2025-03-13 at 1 11 14 PM" src="https://github.com/user-attachments/assets/ba82887b-d2b0-44b1-993b-8be4a2bf791c" />


Name of the database: ha_group7_crn61608


All queries are bookmarked through stored procedures and can be called using this format: CALL TP_Qx(); where 'x' is the query number.
