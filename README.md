Project Overview

This project demonstrates how to integrate data from multiple sources and formats—CSV, JSON, and SQL—into a single unified dataset for analytics.
The final dataset acts as the single source of truth for answering business and hackathon-style analytical questions related to a food delivery application.

Objective

Load and process datasets from CSV, JSON, and SQL

Perform relational joins using business keys

Create an analytics-ready final dataset

Enable insights into user behavior, revenue, cuisine performance, and trends

Data Sources
| Dataset Name | File Name         | Format | Description                                                                                               |
| ------------ | ----------------- | ------ | --------------------------------------------------------------------------------------------------------- |
| Orders       | `orders.csv`      | CSV    | Contains order-level details such as order ID, user ID, restaurant ID, order date, and total order amount |
| Users        | `users.json`      | JSON   | Contains user information including user ID, city, and membership type (Gold / Regular)                   |
| Restaurants  | `restaurants.sql` | SQL    | SQL script that creates and populates the restaurants table with restaurant ID, cuisine type, and ratings |

Join Logic

The datasets are combined using LEFT JOINS to ensure no order data is lost:

orders.user_id → users.user_id

orders.restaurant_id → restaurants.restaurant_id

Tech Stack

Python

Pandas

SQLite (in-memory)

Jupyter Notebook

Implementation Steps

Load orders data from CSV

Load user data from JSON

Execute SQL script and extract restaurant table

Merge datasets using LEFT JOINs

Export final dataset as CSV

Output
final_food_delivery_dataset.csv

The final dataset includes:

Order information

User details (city, membership type)

Restaurant details (cuisine, ratings)

This file is the only source of truth used for all analytical questions in the hackathon.

Analysis Enabled

Using the final dataset, students can analyze:

Order trends over time

City-wise and cuisine-wise revenue

Gold vs Regular membership impact

Average order value patterns

Revenue distribution and seasonality
