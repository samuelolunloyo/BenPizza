Designing and Building a SQL Database for Ben's Pizzeria
Project Brief: Ben's Pizzeria Data Solution
Overview
Ben's Pizzeria is a new business focused on takeout and delivery services. The goal of this project is to design, build, and implement a scalable SQL database solution that will streamline operations, improve customer experience, and facilitate performance tracking for Ben's Pizzeria. The database will manage customer orders, inventory, and employee information, and support the generation of actionable insights through dynamic dashboards.

Objectives
Capture and organize essential business data for customer orders, inventory, and staff.
Support real-time tracking of customer orders, stock levels, and staff performance.
Enable the creation of insightful dashboards to provide Ben with business health insights.
Scope of Work
Database Design and Development
Relational Schema Design
Design a normalized relational database schema to store and manage Ben's Pizzeria’s data.

Key Tables and Relationships:
Customer Orders: Stores order details, including time, delivery address, items ordered, payment status, and special instructions.
Inventory Management: Tracks ingredient stock levels, restocking needs, and low-stock alerts.
Employee Records: Manages staff information such as roles, shifts, performance metrics, and payroll data.
Normalization
Normalize data to reduce redundancy and improve efficiency:

Separate data for customer details, delivery information, and item details into distinct tables.
Use primary keys for unique identification, and represent related tables with foreign keys.
Data Integration and Collection
ETL Processes
Build Extract, Transform, Load (ETL) workflows to import data from various business sources, including POS systems and web orders.
Data Validation
Implement validation checks to ensure data accuracy and integrity at each processing stage.
Dashboard Design for Business Insights
SQL Queries and Procedures
Develop SQL queries to support key performance metrics:
Sales Performance: Trends in sales over time, popular items, and revenue growth.
Order Trends: Frequency, peak times, and customer preferences for targeted marketing.
Inventory Levels: Real-time stock data to help plan for efficient restocking.
Staff Performance: Productivity, attendance, and shift performance for staffing decisions.
Deliverables
SQL Database
A fully functional SQL database optimized for Ben's Pizzeria operations.
Predefined SQL Queries
SQL queries for essential metrics across sales, inventory, and staffing.
Interactive Dashboards
Dashboards leveraging SQL outputs for Ben's business performance insights.
Expected Outcomes
Upon completion, Ben's Pizzeria will have:

A powerful database to store and manage essential data.
Actionable insights into business performance, enabling data-driven decision-making.
A scalable system to support future growth, including new locations or expanded services.
Data Preparation and Column Structure
Initial Data Provided
Ben provided basic data fields for each order:

Item Name, Item Price, Quantity, Customer Name, Delivery Address
Enhanced Data Structure
Based on requirements, we developed a more detailed table structure with the following columns:

RowID, OrderID, Item Name, Item Category, Item Size, Item Price, Quantity
Customer First Name, Customer Last Name, Delivery Address 1, Delivery Address 2, City, Zipcode
Data Visualization Tool
QuickDBD was used to visualize the database structure and define each column's data type.

Database Model Design
Customer and Delivery Information
To avoid data redundancy, separate tables were created for Customer Information and Delivery Details:

Customer Table: Contains customer-specific information.
Delivery Table: Tracks delivery addresses, split into multiple address components.
Stock Control
A stock control feature allows Ben to monitor ingredient levels and know when to restock.

Inventory: Tracks stock levels for ingredients.
Recipe: Maps ingredients and quantities needed for each pizza size.
Relationships: Connects recipes to items through foreign keys to manage inventory accurately.
Staffing
Separate tables manage employee information and shift schedules:

Staff Table
Contains staff details including staff_id (primary key), first_name, last_name, position, and hourly_rate.
Rota Table
Tracks staff schedules, including rota_id, date, shift_id, and staff_id.
Shift Table
Contains shift details, such as shift_day, start_time, and end_time, linked by primary keys to the rota table.
Database Implementation Steps
Database Modeling and Exporting SQL Script
QuickDBD generates an SQL script for creating tables. This project uses MySQL as the relational database management system (RDBMS).
Schema Creation in MySQL
The script is loaded into MySQL Workbench, where the schema, PizzaDB, is created to store Ben's data.
Error Resolution
During execution, any errors are resolved by referring to MySQL documentation or external sources.
Data Population
Data from an Excel file, part of the project dataset, populates the tables.
Future Steps and Improvements
Automate regular ETL processes for seamless data integration.
Enhance dashboard interactivity to support real-time updates.
Expand the database to accommodate multiple store locations as Ben’s Pizzeria grows.
