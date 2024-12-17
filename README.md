# Rolling average SQL

## Overview
This repository contains SQL code files for managing transaction data and calculating rolling averages.

## Files

### 1. Table Definition Code (table_definition.sql)
- **Purpose**: Defines the structure of the database table for storing transaction data.
- **Description**: This SQL file contains code to create a table named `transactions`. The table has two columns: `transaction_time` of type TIMESTAMP and `transaction_amount` of type FLOAT. This table is intended to store transaction records with their timestamps and corresponding amounts.

### 2. Rolling Average SQL Code (rolling_avg_sql.sql)
- **Purpose**: Implements a SQL query to calculate rolling averages of transaction amounts.
- **Description**: This SQL file contains code to calculate the rolling average of transaction amounts per transaction date. It utilizes window functions and subqueries to calculate the average considering the current row and the two preceding rows. The query provides a useful analytical tool for understanding trends and patterns in transaction data over time.

## Usage
1. **Table Definition Code**:
   - Execute `table_definition.sql` to create the `transactions` table in your database.
   - Ensure that the database connection details are properly configured before executing the script.

2. **Rolling Average SQL Code**:
   - Execute `rolling_avg_sql.sql` to run the rolling average calculation query.
   - Adjust the window size in the query as per your analysis requirements.
   - Ensure that the `transaction_time` column in the `transactions` table is of TIMESTAMP data type for accurate date extraction.

## Note
- Both SQL files are intended for use with a PostgreSQL database due to the use of specific syntax like `::date` for type casting and window functions.
- Make sure to review and customize the SQL code according to your specific database environment and data requirements.
