## Task: Data Loading and Transformation with Apache Spark

## Scenario
You are tasked with loading customer, order, and payment data, performing transformations to create meaningful insights, and saving the transformed data back for reporting purposes. The focus is on efficient coding and applying best practices in Spark for handling large datasets.

## Dataset Overview
# raw_customers.csv:
Contains customer details.

Columns: id, first_name, last_name, email
# raw_orders.csv:
Contains order information.

Columns: id (order_id), user_id (refers to raw_customers.id), order_date, status
# raw_payments.csv:
Contains payment information.

Columns: id, order_id (refers to raw_orders.id), payment_method, amount

## Steps

## 1. Data Loading
Load the three CSV files into Spark DataFrames.
Ensure correct schema inference and proper handling of data types for order_date and amount.
Handle missing or invalid data (e.g., drop rows or fill with default values).
Log or print a summary of the dataset (e.g., number of records, distinct users, etc.).

## 2. Data Transformation
# Join the Datasets
Join raw_orders.csv with raw_customers.csv on the user_id field.
Join the resulting DataFrame with raw_payments.csv on order_id.

# Perform the Following Transformations
Calculate the total spent by each customer (sum of amount from raw_payments.csv).
Add a new column to indicate whether a customer has placed more than one order.
Filter the orders to include only completed orders (from raw_orders.csv).

# Extra Transformation
Create a new column full_name by combining first_name and last_name.
Filter customers who spent more than a specified amount (e.g., > 500).

## 3. Data Saving
Save the final transformed DataFrame to Parquet format, partitioned by order_date.
Ensure efficient querying by optimizing partitioning and using the appropriate file format for analytics (e.g., Parquet).


## Bonus Task
Write a PySpark SQL query to find the top 5 customers by total spending and save the result as a Parquet file.

