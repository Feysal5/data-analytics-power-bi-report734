# Power BI Business Intelligence Project

## Overview
This project aims to elevate business intelligence practices for a medium-sized international retailer by transforming accumulated sales data into actionable insights. The comprehensive Quarterly report will be designed using Microsoft Power BI, encompassing high-level business summaries and specific insights for better decision-making.

## Data Loading and Transformation

### Task 1: Orders Table
- Connect to the Azure SQL Database and import the `orders_powerbi` table.
  - **Credentials:**
    - Server Name: `my-server-maya.database.windows.net`
    - Database Name: `orders_db`
    - Username: `maya`
    - Password: `AiCore127!`
- In Power Query Editor:
  - Delete the [Card Number] column for data privacy.
  - Split [Order Date] and [Shipping Date] into separate date and time columns.
  - Filter out rows with missing [Order Date].
  - Rename columns to align with Power BI conventions.

### Task 2: Products Table
- Download the `Products.csv` file and import it into Power BI.
- In Power Query Editor:
  - Remove duplicates based on the `product_code` column.
  - Clean and transform the `weight` column as specified.
  - Create a calculated column for weight in kilograms.
  - Rename columns for consistency.

### Task 3: Stores Table
- Connect to Azure Blob Storage and import the `Stores` table.
  - **Blob Storage Credentials:**
    - Account Name: `powerbistorage2`
    - Account Key: `ZPUQ+verSniHMG7EqR5/VAQc0aUYYG1utLQQuke0JQqR18TRRZI1/vTX65OqeXfUgWAugYLL73Gp+AStozRNKw==`
    - Container Name: `data-analytics`
- Rename columns for consistency.

### Task 4: Customers Table
- Download and unzip the `Customers.zip` file.
- Import the Customers folder using the Folder data connector.
- In Power BI:
  - Combine and transform data from the three CSV files.
  - Create a Full Name column by combining [First Name] and [Last Name].
  - Delete unused columns and rename for consistency.
