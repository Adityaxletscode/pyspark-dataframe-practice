# PySpark DataFrame Assignment --- Questions

This assignment contains practical PySpark DataFrame exercises covering
filtering, column operations, aggregation, joins, and window functions.

## 1. Employee Salary Filter

You are given an employee dataset containing:

`employee_id, employee_name, department, salary, city`

The HR team wants to identify employees who are earning more than
₹50,000 and working in the IT department.

**Task:** - Filter employees with salary greater than ₹50,000. - Keep
only employees from the IT department. - Display `employee_id`,
`employee_name`, `department`, and `salary`. - Sort the result by salary
from highest to lowest.

**Concepts:** `createDataFrame()`, `filter()`, `select()`, `orderBy()`

------------------------------------------------------------------------

## 2. Employee Salary Revision

A company has decided to provide a 10% salary increment to all
employees.

The dataset contains:

`employee_id, employee_name, department, salary`

**Task:** - Create a column called `increment_amount` containing 10% of
salary. - Create a column called `revised_salary` containing salary
after the increment. - Display all employee details with the newly
calculated columns.

**Concepts:** `withColumn()`, `col()`, arithmetic operations

------------------------------------------------------------------------

## 3. Categorize Customers Based on Age

A retail company wants to classify its customers into different age
groups.

The dataset contains:

`customer_id, customer_name, age, city`

Create an `age_category` column using:

-   Age \< 25 → Young
-   Age 25 to 40 → Adult
-   Age \> 40 → Senior

**Task:** Display customer name, age, city, and the calculated age
category.

**Concepts:** `withColumn()`, `when()`, `otherwise()`

------------------------------------------------------------------------

## 4. Clean Employee Data

The HR department received an employee dataset containing some
incomplete records:

`employee_id, employee_name, department, salary, email`

Some records have a missing salary, while others have a missing email.

**Task:** - Identify employees with missing salaries. - Replace missing
salary values with `0`. - Replace missing email addresses with
`"Not Available"`. - Remove records where the employee identifier is
missing.

**Concepts:** `isNull()`, `fillna()`, `dropna()`

------------------------------------------------------------------------

## 5. Department-wise Salary Report

Management wants a summary of salary expenses for every department.

The employee dataset contains:

`employee_id, employee_name, department, salary`

**Task:** For each department, calculate: - Number of employees - Total
salary - Average salary - Highest salary

Display only departments whose average salary is greater than ₹50,000
and arrange them by average salary in descending order.

**Expected columns:**

`department | employee_count | total_salary | average_salary | highest_salary`

**Concepts:** `groupBy()`, `agg()`, `count()`, `sum()`, `avg()`,
`max()`, `filter()`, `orderBy()`

------------------------------------------------------------------------

## 6. Completed Order Sales Analysis

An e-commerce company maintains order data containing:

`order_id, customer_id, product, category, quantity, unit_price, status`

The business team wants to analyze only successfully completed orders.

**Task:** - Filter records where `status = "Completed"`. - Create
`order_value = quantity × unit_price`. - Calculate total sales amount
for each category. - Display categories from highest to lowest sales.

**Concepts:** `filter()`, `withColumn()`, `groupBy()`, `sum()`,
`orderBy()`

------------------------------------------------------------------------

## 7. Customer and Order Details

You are provided with two DataFrames.

### Customers

`customer_id, customer_name, city`

### Orders

`order_id, customer_id, product, amount, status`

The sales team wants a consolidated report containing customer
information along with their completed orders.

**Task:** - Filter only completed orders. - Join Customers and Orders
using `customer_id`. - Display: - `customer_id` - `customer_name` -
`city` - `order_id` - `product` - `amount` - Sort the final result by
amount in descending order.

**Concepts:** `filter()`, `join()`, `select()`, `orderBy()`

------------------------------------------------------------------------

## 8. Find Customers Without Orders

A marketing team wants to identify registered customers who have never
placed an order.

### Customers

`customer_id, customer_name, city`

### Orders

`order_id, customer_id, amount`

**Task:** Use an appropriate DataFrame join to identify customers who do
not have any matching orders.

Display:

`customer_id, customer_name, city`

**Expected approach:**

Customers → Left Join → Orders → Customers without orders

**Concepts:** `left join`, `left_anti join`, `isNull()`, `select()`

------------------------------------------------------------------------

## 9. Highest-Paid Employee in Every Department

The HR department wants to identify the highest-paid employee in every
department.

The dataset contains:

`employee_id, employee_name, department, salary`

**Task:** - Create a window for each department. - Arrange employees by
salary in descending order. - Assign a row number. - Return only the
highest-paid employee from each department.

**Expected output:**

`department | employee_name | salary`

**Concepts:** `Window.partitionBy()`, `orderBy()`, `row_number()`,
`filter()`

------------------------------------------------------------------------

## 10. E-Commerce Customer Spending Analysis

An e-commerce company wants to identify its most valuable customers.

You are provided with three DataFrames.

### Customers

`customer_id, customer_name, city`

### Orders

`order_id, customer_id, order_date, status`

### Order Items

`order_id, product_name, category, quantity, unit_price`

**Task:** 1. Keep only orders where `status = "Completed"`. 2. Calculate
`item_value = quantity × unit_price`. 3. Calculate the total value of
each order. 4. Join the order totals with the completed orders. 5. Join
the result with the customer DataFrame. 6. Calculate total spending for
every customer. 7. Keep only customers whose total spending is greater
than ₹10,000. 8. Sort customers by total spending in descending order.
9. Display the top 5 customers.

**Final output:**

`customer_id | customer_name | city | total_spending`

**Concepts:** `filter()`, `withColumn()`, `groupBy()`, `agg()`,
`join()`, `select()`, `orderBy()`, `limit()`
