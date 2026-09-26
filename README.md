# PySpark DataFrame Practice

A practical **PySpark DataFrame assignment** covering core DataFrame
operations used in data engineering and analytics workflows.

The notebook contains hands-on exercises involving filtering, column
transformations, conditional logic, missing-value handling,
aggregations, joins, and window functions.

## 🧰 Technologies & Platform Used

-   Python
-   PySpark
-   Apache Spark
-   **Databricks Workspace**
-   **Databricks Catalog**
-   Jupyter Notebook

## ☁️ Databricks Environment

This project was developed and executed using a **Databricks
Workspace**.

The datasets and Spark DataFrame exercises were organized and accessed
within the Databricks environment using the **Databricks Catalog**. This
provided a structured environment for working with data and running
PySpark transformations.

The project demonstrates practical usage of:

-   Databricks Workspace for notebook development and execution
-   Databricks Catalog for organizing and accessing data
-   PySpark DataFrames for data processing
-   Spark SQL functions for transformations and aggregations
-   Joins and Window Functions for analytical processing

## 📂 Project Structure

``` text
pyspark-dataframe-assignment/
│
├── PySparkDF_Assignment.ipynb
├── QUESTIONS.md
└── README.md
```

## 📚 Topics Covered

  -----------------------------------------------------------------------
  \#                      Topic                   Main PySpark Concepts
  ----------------------- ----------------------- -----------------------
  1                       Employee Salary Filter  `filter()`, `select()`,
                                                  `orderBy()`

  2                       Employee Salary         `withColumn()`,
                          Revision                `col()`, arithmetic
                                                  operations

  3                       Customer Age            `when()`,
                          Categorization          `otherwise()`,
                                                  `withColumn()`

  4                       Clean Employee Data     `isNull()`, `fillna()`,
                                                  `dropna()`

  5                       Department-wise Salary  `groupBy()`, `agg()`,
                          Report                  `count()`, `sum()`,
                                                  `avg()`, `max()`

  6                       Completed Order Sales   `filter()`,
                          Analysis                `withColumn()`,
                                                  `groupBy()`, `sum()`

  7                       Customer and Order      `join()`, `filter()`,
                          Details                 `select()`, `orderBy()`

  8                       Find Customers Without  `left join`,
                          Orders                  `left_anti`, `isNull()`

  9                       Highest-Paid Employee   `Window`,
                          by Department           `partitionBy()`,
                                                  `row_number()`

  10                      E-Commerce Customer     `filter()`,
                          Spending                `withColumn()`,
                                                  `groupBy()`, `join()`,
                                                  `orderBy()`, `limit()`
  -----------------------------------------------------------------------

## 📝 Assignment Overview

### 1. Employee Salary Filter

Filter employees earning more than ₹50,000 who belong to the IT
department. Display selected employee details and sort by salary in
descending order.

### 2. Employee Salary Revision

Calculate a 10% salary increment and create a revised salary column.

### 3. Categorize Customers Based on Age

Create age categories:

-   `< 25` → Young
-   `25–40` → Adult
-   `> 40` → Senior

### 4. Clean Employee Data

Work with incomplete employee records by identifying null values,
replacing missing salary and email values, and removing records with a
missing employee identifier.

### 5. Department-wise Salary Report

Generate department-level salary statistics including employee count,
total salary, average salary, and maximum salary.

### 6. Completed Order Sales Analysis

Analyze completed e-commerce orders by calculating order value and total
sales by category.

### 7. Customer and Order Details

Join customer and order data to create a consolidated report of
completed orders.

### 8. Find Customers Without Orders

Use a left join or left anti join to identify customers who have not
placed an order.

### 9. Highest-Paid Employee in Every Department

Use a window function partitioned by department to find the highest-paid
employee in each department.

### 10. E-Commerce Customer Spending Analysis

Combine customers, orders, and order items to calculate customer-level
spending, filter customers above ₹10,000, sort by spending, and display
the top 5.

## 🎯 Learning Objectives

By completing this assignment, you will practice:

-   Creating and loading Spark DataFrames
-   Working with PySpark in Databricks
-   Using Databricks Workspace and Catalog
-   Filtering DataFrames
-   Selecting and renaming columns
-   Creating calculated columns
-   Applying conditional logic
-   Handling missing values
-   Performing aggregations
-   Joining multiple DataFrames
-   Using left and left anti joins
-   Creating window specifications
-   Ranking records within groups
-   Sorting and limiting results
-   Building multi-step PySpark data transformations

## 🚀 Getting Started

### 1. Databricks

Open the project notebook in your **Databricks Workspace** and make sure
the required datasets are available through the appropriate **Catalog**.

### 2. Start Spark

Databricks provides the Spark environment required to execute the
notebook. The exercises can be run directly from a Databricks notebook.

Example:

``` python
from pyspark.sql import SparkSession

spark = SparkSession.builder \
    .appName("Spark DataFrame Assignment") \
    .getOrCreate()
```

### 3. Open the Notebook

Open:

``` text
PySparkDF_Assignment.ipynb
```

If you are running the notebook outside Databricks, update the input
data paths and Spark configuration accordingly.

## 📊 Skills Demonstrated

This project demonstrates practical PySpark skills relevant to:

-   Data Engineering
-   Big Data Processing
-   Data Analytics
-   ETL Pipelines
-   Apache Spark
-   Databricks
-   Spark SQL

## 👤 Author

**Aditya Kumar Singh**

This repository is intended as a learning and practice project for
PySpark DataFrame operations using Databricks.
