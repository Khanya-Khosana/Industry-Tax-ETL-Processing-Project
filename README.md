# Industry-Tax-ETL-Processing-Project

Overview

This project implements a simple ETL (Extract, Transform, Load) pipeline using Python and Pandas. The objective is to process the industry_tax.csv dataset in batches of five rows, perform tax-related calculations, and generate a summarized dataset containing batch-level statistics.

Objectives
Import data from a CSV file.
Process the dataset in batches of 5 rows.
Calculate average taxable income, average tax paid, and average cash tax paid.
Aggregate batch statistics.
Store the results in a new DataFrame.
Export the transformed data to a CSV file.
Technologies Used
Python
Pandas
Jupyter Notebook
ETL Process
1. Extract

The dataset industry_tax.csv is imported into Python using Pandas. The data is then processed in batches of five rows at a time.

2. Transform

For each batch of five rows, the following calculations are performed:

Average Taxable Income

For each row:

average_taxable_income =
total_taxable_income / number_of_firms

The batch average taxable income is calculated as the mean of all average_taxable_income values within the batch.

Average Tax Paid

For each row:

average_tax_paid =
total_taxes_paid / number_of_firms

The batch average tax paid is calculated as the sum of all average_tax_paid values within the batch.

Average Cash Tax Paid

For each row:

average_cash_tax_paid =
total_cash_taxes_paid / number_of_firms

The batch average cash tax paid is calculated as the sum of all average_cash_tax_paid values within the batch.

3. Batch Summary DataFrame

For each processed batch, the following information is stored:

batch_number
batch_average_taxable_income
batch_average_tax_paid
batch_average_cash_tax_paid

The final transformed DataFrame contains only these four columns.

4. Load

The final DataFrame is:

Printed to the console/output cell.
Exported to a CSV file named:
studentID-batched_average_taxes.csv
Output

The project produces:

A summarized DataFrame containing batch-level tax statistics.
A CSV file containing the transformed results.
A Jupyter Notebook file documenting the complete ETL process.
Files Included
StudentID-LastName.ipynb
industry_tax.csv
studentID-batched_average_taxes.csv
