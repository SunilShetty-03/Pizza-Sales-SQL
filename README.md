Pizza Sales Analysis: SQL Insights Project
A collection of SQL queries designed to extract business insights from pizza sales data, ranging from basic aggregations to advanced analytics.
Short Description / Purpose
This SQL project analyzes a Pizza Sales Dataset to uncover sales performance metrics, customer preferences, and revenue trends through 13 targeted queries. It is intended for data analysts, business managers, and SQL learners to derive actionable insights from transactional data and demonstrate SQL proficiency from basic to advanced levels.
Tech Stack
The project was built using the following tools and technologies:
•  SQL for executing queries and viewing results.
• Presentation – Canva for compliling queries into slides.
• File Format – .sql for query scripts, .pdf for the final project presentation.
Data Source

Source: Public Pizza Sales Dataset (commonly available on platforms like Kaggle).

The dataset comprises relational tables including:
orders: Order IDs, dates, and times.
order_details: Quantities and pizza IDs per order.
pizzas: Pizza IDs, types, sizes, and prices.
pizza_types: Pizza names, categories (e.g., Chicken, Classic), and ingredients.
It captures transactional data for analysis of sales volume, revenue, and trends.

Features / Highlights
Business Problem
Pizza businesses generate vast transactional data, but extracting insights like total revenue, popular products, peak ordering times, or category performance is challenging without structured queries. Key questions include: What are the top-selling pizzas? When are peak hours? How does revenue accumulate over time?
Goal of the Dashboard
To deliver a set of SQL queries that:

Analyze sales data to answer business questions efficiently.
Support decisions on inventory, marketing, and operations.
Uncover trends in customer behavior, revenue distribution, and product popularity.

Walkthrough of Key Visuals

Key Metrics from Queries 
Total Orders: 21,350 
Total Revenue: $817,860.05 
Highest-Priced Pizza: The Greek Pizza ($35.95) 
Most Common Size: Large (18,526 orders) 
Average Pizzas per Day: 138
Problem 1 (Total Orders) Simple COUNT query on orders table; result shows 21,350 orders.
Problem 2 (Total Revenue) JOIN order_details and pizzas, SUM quantity * price; rounded to $817,860.05.
Problem 3 (Highest-Priced Pizza) JOIN pizza_types and pizzas, ORDER BY price DESC LIMIT 1; identifies The Greek Pizza.
Problem 4 (Most Common Size) JOIN pizzas and order_details, GROUP BY size, ORDER BY count DESC LIMIT 1; Large size dominates.
Problem 5 (Top 5 Pizza Types by Quantity) Multi-JOIN, SUM quantity, GROUP BY name, ORDER DESC LIMIT 5; e.g., Classic Deluxe (2,453).
Problem 6 (Quantity by Category) Multi-JOIN, SUM quantity, GROUP BY category, ORDER DESC; Classic leads with 14,888.
Problem 7 (Orders by Hour) HOUR function on time, COUNT orders, GROUP BY hour; peaks at 12-13 (around 2,500 each).
Problem 8 (Pizzas per Category) COUNT names, GROUP BY category; balanced distribution (6-9 per category).
Problem 9 (Average Pizzas per Day) Subquery to SUM daily quantities, then AVG; 138 pizzas/day.
Problem 10 (Top 3 by Revenue) Multi-JOIN, SUM revenue, GROUP BY name, ORDER DESC LIMIT 3; Thai Chicken tops at $43,434.25.
Problem 11 (Percentage by Category) Subquery for total revenue, calculate category %; Classic ~27%.
Problem 12 (Cumulative Revenue) Window function SUM OVER ORDER BY date; shows growth over time.
Problem 13 (Top 3 per Category by Revenue) RANK() OVER PARTITION BY category; e.g., Thai Chicken for Chicken category.

Business Impact & Insights

Product Strategy: Focus promotions on top performers like Thai Chicken Pizza.
Operational Efficiency: Staff more during peak hours (noon-early afternoon).
Revenue Forecasting: Cumulative trends help predict future sales.
Category Optimization: Balance inventory across categories based on contributions.

