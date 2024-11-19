# Billing Data Warehouse Setup and Data Quality Checks

## Project Overview

This project performs essential data quality checks on the billingDW data warehouse. It ensures that the data is clean and reliable by validating key aspects such as null values, duplicates, range constraints, and valid values.

## Data Quality Checks
- Check for Nulls: Ensures that columns do not contain NULL values.
- Check for Min/Max Range: Validates that values fall within a specified range.
- Check for Valid Values: Verifies that column values are within a predefined set of valid values.
- Check for Duplicates: Detects duplicate entries in specified columns.

## Features

- **Database Setup**: Creates a PostgreSQL database with a star schema structure (`FactBilling`, `DimCustomer`, and `DimMonth` tables).
- **Data Loading**: Automates loading of billing data into the database.
- **Data Quality Checks**: Includes tests for null values, data ranges, valid entries, and duplicate records to maintain data accuracy.

## Project Structure

```plaintext
.
├── dataqualitychecks.py   # Python functions for data quality checks
├── mytests.py             # Definitions of the test cases
├── star-schema.sql        # SQL script to create the database schema
├── DimCustomer.sql        # SQL script to load data into DimCustomer table
├── DimMonth.sql           # SQL script to load data into DimMonth table
├── FactBilling.sql        # SQL script to load data into FactBilling table
├── verify.sql             # SQL script to verify data in the database
├── setup.sh               # Shell script for setting up the database and loading data
└── README.md              # Documentation file
