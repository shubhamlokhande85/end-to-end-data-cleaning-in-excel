Customer Sales Dataset — Data Cleaning and Preprocessing
Project Overview

This project focuses on cleaning and preprocessing a messy customer sales dataset using Microsoft Excel. The dataset, messy_customer_sales_dataset.csv, contained inconsistent text values, missing information, duplicate records, and formatting issues.

The goal was to improve data quality, standardize values, handle missing entries, and prepare a cleaner dataset for further analysis and visualization.

Project Details
Item	Description
Project Name	Customer Sales Data Cleaning
Organization	Swynex
Project Type	Internship Project
Tool Used	Microsoft Excel
Input Format	CSV
Output Format	Excel Workbook
Main Tasks	Data cleaning, standardization, missing value handling, duplicate removal
Objectives
Inspect the dataset and identify data quality issues.
Detect and remove duplicate records.
Handle missing values using defined rules.
Standardize inconsistent text and categorical values.
Check phone number lengths for consistency.
Apply appropriate date and currency formatting.
Create a cleaned dataset suitable for further analysis.
Dataset Description

The dataset contains customer-related and sales-related information, including:

Customer ID
Gender
Age
City
Signup Date
Last Purchase Date
Purchase Amount
Feedback Score
Email
Phone Number
Country

The input file was provided as a CSV dataset for the cleaning exercise. Add the original dataset's public source and license here if available.

Data Quality Issues Identified

The initial inspection identified several data quality problems:

Missing customer IDs and other blank values.
Duplicate customer IDs or records.
Inconsistent gender entries, such as F, f, Female, m, and Male.
Age values containing decimal portions, such as 51.0.
Inconsistent spacing and capitalization in City and Country values.
Missing purchase dates and purchase amounts.
Missing feedback scores.
Phone numbers with different character lengths.
Inconsistent or general number formatting in date and currency columns.
Data Cleaning Process
1. Initial Inspection and Preparation
Imported the CSV file into Microsoft Excel.
Created a separate working copy to preserve the original dataset.
Adjusted column widths for readability.
Reviewed rows, columns, and field names.
Applied filters to inspect individual columns.
2. Duplicate Detection and Removal
Used Conditional Formatting to highlight duplicate customer ID values.
Filtered the highlighted values to inspect the corresponding records.
Used Data → Remove Duplicates to remove the identified duplicate records.

Validation consideration: Duplicate customer IDs do not always mean that entire records are duplicates. Customer IDs and complete duplicate records should be validated separately where appropriate.

3. Customer ID Cleaning
Identified blank customer ID values.
Used an IF() formula to replace missing IDs with Unknown_ID.
Copied the formula results and pasted them as values to create a static output column.
4. Gender Standardization
Identified inconsistent gender labels and missing entries using filters.
Used TRIM() to remove extra spaces.
Used PROPER() to standardize capitalization.
Used Find & Replace to map inconsistent labels to standard categories.
Replaced missing gender values with Unknown.
Converted formula results to static values.
5. Age Cleaning
Identified age values containing decimal portions, such as 51.0.
Used Text to Columns with the period (.) as a delimiter to separate the decimal portion.
Handled missing age values using an Unknown placeholder.
Copied the cleaned results as values.

Validation consideration: Text to Columns can split a value into separate fields. The resulting age values should be checked to ensure that the integer age was retained correctly and that valid age ranges are respected.

6. City Standardization
Inspected blank and inconsistent City values.
Used TRIM() and PROPER() to normalize spacing and capitalization.
Replaced missing City values with Unknown.
Converted the results into static values.
7. Date Cleaning

Signup Date

Checked for blank values and reviewed the column's formatting.
Applied a consistent date display format.

Last Purchase Date

Identified missing values using filters.
Replaced missing values with an Unknown placeholder.
Standardized the date display format.
Converted formula results to static values.

Validation consideration: A column containing both dates and text placeholders such as Unknown should be treated as mixed-type data. For analysis, consider retaining true date values and representing missing dates as blank or null in the analytical dataset.

8. Purchase Amount Cleaning
Identified missing purchase amounts.
Used an IF() formula to apply the selected missing-value rule.
Converted the formula output to static values.
Applied currency formatting to the cleaned numeric values.

Validation consideration: Missing purchase amounts should not automatically be interpreted as zero unless that meaning is justified by the dataset. The chosen treatment should be documented before calculating sales totals or averages.

9. Feedback Score Cleaning
Identified blank feedback scores.
Used an IF() formula to replace missing scores with 0.
Copied the resulting values into a static column.

Validation consideration: A zero can represent a genuine score or a missing value. Confirm the dataset's scoring rules before using zero as a replacement.

10. Email Review
Inspected the Email column using filters.
No blank email values were identified during the review.

This check addressed missingness only; email format validity and uniqueness were not established by that check.

11. Phone Number Cleaning
Used LEN() to measure the character length of each phone number.
Identified phone numbers with inconsistent lengths, including values containing 7, 8, 10, and 11 characters.
Applied a conditional rule based on the expected 10-character phone number format.
Converted the formula results to static values.

Validation consideration: A length of 10 characters does not prove that a phone number is valid. Values with other lengths should be flagged and investigated rather than automatically modified without a documented rule. Country codes, leading zeros, and non-numeric characters should also be considered.

12. Country Standardization
Identified missing Country values and inconsistent labels.
Used TRIM() and PROPER() to normalize text formatting.
Standardized variations such as IND, Ind, India, and INDIA to India.
Replaced missing Country values with Unknown.
Converted the cleaned output to static values.
13. Final Dataset Preparation
Created a separate final working sheet.
Removed unnecessary columns from the final output.
Saved the workbook containing the processed dataset.
Excel Functions and Features
Function or Feature	Purpose
IF()	Apply conditional rules and handle missing values
TRIM()	Remove extra spaces
PROPER()	Standardize text capitalization
LEN()	Check phone number character lengths
Find & Replace	Standardize inconsistent categories
Conditional Formatting	Highlight duplicate values
Filters	Inspect blanks and inconsistent entries
Remove Duplicates	Remove duplicate records
Text to Columns	Separate decimal portions from age values
Paste Special → Values	Convert formulas into static values
Number Formatting	Standardize date and currency display
Final Output

The final working sheet was prepared with selected columns and standardized values for subsequent analysis.

The cleaning process focused on:

More consistent text categories.
Explicit handling of missing values.
Removal of identified duplicate records.
Improved date and currency presentation.
Identification of inconsistent phone number lengths.
A separate final dataset for further processing.

The results should undergo final validation before being used for business decisions or reporting.

Limitations and Future Improvements
Verify whether duplicate records were removed using the correct business key.
Confirm that Unknown_ID placeholders do not create misleading customer-level counts.
Preserve missing-value indicators where zero or text placeholders could change analytical results.
Validate phone numbers against an appropriate country-specific rule.
Ensure dates and purchase amounts use consistent data types.
Compare the original and final row counts and record the number of duplicates removed.
Add before-and-after quality checks and summary statistics.
Use Python or Power BI in a future iteration if automated or repeatable processing is required.
Repository Structure

A suggested repository structure is:

customer-sales-data-cleaning/
├── README.md
├── data/
│   └── messy_customer_sales_dataset.csv
├── output/
│   └── cleaned_customer_sales_dataset.xlsx
└── documentation/
    └── cleaning_summary.xlsx


Adjust the filenames and folders to match the files actually uploaded to the repository. If the public dataset has redistribution restrictions, provide its source link rather than uploading another copy.

Conclusion

This project demonstrates a practical Excel-based data cleaning workflow, including data inspection, duplicate detection, missing-value handling, text standardization, formatting, and preparation of a final working dataset.

It provided hands-on experience in improving dataset consistency and preparing customer sales data for future analysis and visualization.

Tools: Microsoft Excel
Project Category: Data Cleaning and Preprocessing
Organization: Swynex Internship

<img width="860" height="326" alt="Cleanned Dataset" src="https://github.com/user-attachments/assets/fec7068b-83ba-48cf-a63f-489af1dfb95e" />
