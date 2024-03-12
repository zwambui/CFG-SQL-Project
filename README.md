## CFG-SQL-Project

### Introduction
#### A simple process of creating and populating tables within a database of a bakery business.

### Project Overview
#### The database facilitates efficient order management, product catalog management, customer relationship management, and analysis/reporting capabilities for the bakery business. It helps streamline operations, improve customer service, and make data-driven decisions to optimize business performance.

### Tools used
#### - MySQL
#### - Excel

### Procedure
#### 1. Data Creation
   * The script begins by creating a database named "Baked_by_Zep" using the CREATE DATABASE statement.
   * It then switches to use this newly created database with the USE statement.
   * Several tables are then created within the database:
        * OrderFact: Contains order-related information such as order ID, product ID, customer ID, etc.
        * MyBaked_goodies: Stores information about baked products along with their prices.
        * MyOrders: Stores order details including order ID, product ID, order date, customer details, etc.
        * Customers: Contains customer information like customer ID, name, phone number, address, etc.
        * Ingredients: Stores information about ingredients used in baked goods.
        * Delivery: Contains delivery information such as delivery ID, order ID, delivery date, and status.

#### 2. Data Insertion
  * Data is inserted into the tables using the INSERT INTO statements to populate them with initial values.
  * Foreign key constraints are added to ensure referential integrity between related tables using the ALTER TABLE statements.

#### 3. Analysis Queries
  * A join query to retrieve information from multiple tables (MyOrders and MyBaked_goodies) based on a common column (ProductID).
  * A query using GROUP BY and HAVING clauses to calculate the average unit price of orders for each customer and filter results based on a condition.
  * A subquery to count the number of orders with fewer than 5 units for each customer.
  * Creation of a view (AView) combining columns from OrderFact and Delivery tables.
  * Definition of a stored procedure (GetOrderTotal) to calculate the total price of an order based on its ID.
  * Creation of a stored function (GetOrderCountByProduct) to count the number of orders for a specified product.

### Results/Findings
#### - Analysis of the OrderFact table can reveal the best-selling products by aggregating the total number of units sold for each product. This information helps identify the most popular items among customers.
#### - Calculation of total revenue from orders can be done by multiplying the unit price with the order units for each transaction in the OrderFact table. This analysis provides insights into the bakery's overall sales performance.
#### - Comparison of prices for similar products in the MyBaked_goodies table allows for assessing pricing strategies and identifying opportunities for pricing optimization to maximize profitability.

### Challenges
#### - Data Inaccuracy
  *  I mistakenly entered an incorrect OrderID when recording an order in the "OrderFact" table. As a result, the data in the "OrderFact" table did not match the corresponding entry in the "MyOrders" table. I had to implement data cleaning and standardization processes to address inconsistencies caused by the data entry error to ensure uniformity and accuracy.
