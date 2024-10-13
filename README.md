# etlPocess
# Incubyte Assessment

# Customer ETL Workflow

This repository contains the code and resources for a customer data ETL (Extract, Transform, Load) workflow, implemented using PySpark and Databricks. The workflow processes customer data files, applies transformations, and writes the results into partitioned tables based on country.

## Project Overview

### Problem Statement:
The goal of this ETL workflow is to process customer data for a global multi-specialty hospital chain. The hospital issues user cards to its customers, and the data needs to be partitioned and stored based on customer locations (country).

The data includes details like:
- Customer name
- Customer ID
- Date of Birth (DOB)
- Last consulted date
- Vaccination details

The workflow derives new columns such as:
- Age of the customer
- Days since the last consultation

### ETL Process:
1. **Data Ingestion**: Reads customer data from a CSV file.
2. **Data Transformation**:
   - Converts integer dates (DOB, last consulted) to proper date formats.
   - Calculates derived columns (Age, Days Since Last Consultation).
3. **Data Partitioning**: The data is partitioned by country and saved in a parquet format for efficient querying.
4. **Data Validation**: Ensures data consistency and correctness throughout the process.

## How to Use

### Prerequisites:
- [Databricks Community Edition](https://databricks.com/try-databricks)
- Basic knowledge of PySpark and DataFrames
- Git for version control (optional)

### Running the ETL Workflow:

1. **Upload the CSV File**: 
   - Upload the sample customer data CSV (available in this repo) to your Databricks environment.

2. **Run the PySpark Script**:
   - Open the notebook `deAssess.ipynb` in your Databricks environment.
   - Execute the code to read, transform, and write the data to the output location.

3. **Outputs**:
   - The transformed data is written into a partitioned format based on countries in the `/FileStore/output/partCust` directory.


###Sreenshots
- Screenshots of the Databricks UI input path, output path, and code are available
