Customer Sales Dataset — Data Cleaning and Preprocessing
📌 Project Overview

This project focuses on cleaning and preprocessing a messy customer sales dataset using Microsoft Excel as part of an internship project at Swynex.

The original dataset, messy_customer_sales_dataset.csv, contained missing values, duplicate records, inconsistent text entries, and formatting issues.

The objective was to improve data quality, standardize inconsistent values, handle missing data, and prepare a cleaned dataset for further analysis and visualization.

📋 Project Information


Category	Details


Project Name	Customer Sales Data Cleaning


Organization	Swynex


Project Type	Internship Project


Tool Used	Microsoft Excel


Input Format	CSV


Output Format	Excel Workbook


Project Focus	Data Cleaning and Preprocessing


🎯 Project Objectives


Identify data quality issues in the original dataset.


Detect and remove duplicate records.


Handle missing values using conditional formulas.


Standardize inconsistent text and categorical values.


Inspect phone number lengths for consistency.


Apply appropriate date and currency formatting.


Prepare a cleaned dataset for further analysis and reporting.


📂 Dataset Description

The dataset contains customer and sales-related information across the following columns:

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

Data Quality Issues Identified

During the initial inspection, the following issues were identified:

Missing customer IDs and other blank values.

Duplicate customer IDs or records.

Inconsistent gender entries, such as F, f, Female, m, and Male.

Age values containing decimal portions, such as 51.0.

Inconsistent spacing and capitalization in City and Country values.

Missing purchase dates, purchase amounts, and feedback scores.

Phone numbers with inconsistent character lengths.

Inconsistent date and currency formatting.


🧹 Data Cleaning Process

Initial Inspection and Preparation
   
Imported the CSV dataset into Microsoft Excel.

Created a separate working copy to preserve the original data.

Adjusted column widths for better readability.

Reviewed the dataset structure, rows, and columns.

Applied filters to inspect individual columns and identify data quality issues.

Duplicate Detection and Removal

Used Conditional Formatting to highlight duplicate customer ID values.

Applied filters to inspect the identified duplicates.

Used Data → Remove Duplicates to remove the selected duplicate records.

Note: Duplicate customer IDs do not necessarily indicate duplicate records. The appropriate business key should be verified before removing records.

1. Customer ID Cleaning

Identified blank customer ID values using filters.

Used the IF() function to replace missing IDs with Unknown_ID.

Copied the formula results and used Paste Special → Values to create static values.

2. Gender Standardization

Identified inconsistent gender values and missing entries.

Used TRIM() to remove extra spaces.

Used PROPER() to standardize text capitalization.

Used Find & Replace to map inconsistent labels to standard categories.

Replaced missing gender values with Unknown.

Converted formula results into static values.


3. Age Cleaning

Identified age values containing decimal portions, such as 51.0.

Used Text to Columns with a period (.) as the delimiter to separate decimal portions.

Handled missing age values using an Unknown placeholder.

Copied the cleaned results as static values.

Note: The resulting age values should be checked to ensure that valid ages were retained correctly and no information was lost during the conversion.



4. City Standardization

Inspected the City column for missing values and inconsistent text.

Used TRIM() and PROPER() to standardize spacing and capitalization.

Replaced missing City values with Unknown.

Converted formula results into static values.



Date Cleaning

5. Signup Date

Checked for blank values using filters.

Reviewed the existing date formatting.

Applied a consistent date display format.



6. Last Purchase Date

Identified missing date values.

Replaced missing values with an Unknown placeholder.

Standardized the date display format.

Converted formula results into static values.

Note: For further analysis, actual dates should ideally remain date values, while missing dates should be represented as blank or null rather than text placeholders.


7. Purchase Amount Cleaning

Identified missing Purchase Amount values.

Used an IF() formula to apply the selected missing-value treatment.

Converted formula results into static values.

Applied currency formatting to the numeric values.

Note: Missing purchase amounts should not automatically be interpreted as zero unless this treatment is appropriate for the dataset.

8. Feedback Score Cleaning

Identified blank Feedback Score values.

Used an IF() formula to replace missing values with 0.

Converted the resulting values into static values.

Note: A score of 0 may represent either a genuine score or missing information. This distinction should be considered during analysis.


9. Email Review

Inspected the Email column using filters.

No blank email values were identified during the review.

The check focused on missing values; email format validity and uniqueness were not verified.


10. Phone Number Cleaning

Used the LEN() function to measure phone number character lengths.

Identified inconsistent lengths, including values containing 7, 8, 10, and 11 characters.

Applied a conditional rule based on the expected 10-character phone number format.

Copied formula results as static values.

Note: Phone number length alone does not confirm validity. Values with unexpected lengths should be reviewed, considering country codes, leading zeros, and the applicable phone numbering rules.


11. Country Standardization

Identified missing values and inconsistent country labels.

Used TRIM() and PROPER() to standardize text formatting.

Used Find & Replace to standardize variations such as IND, Ind, India, and INDIA to India.

Replaced missing Country values with Unknown.

Converted the cleaned results into static values.


12. Final Dataset Preparation

Created a separate final working sheet.

Removed unnecessary columns from the final output.

Saved the processed dataset in the Excel workbook.



🛠️ Excel Functions and Features Used

Function / Feature	Purpose

IF()	Apply conditional rules and handle missing values

TRIM()	Remove unnecessary spaces

PROPER()	Standardize text capitalization

LEN()	Check phone number character lengths

Find & Replace	Standardize inconsistent text values

Conditional Formatting	Highlight duplicate values

Filters	Inspect blanks and inconsistent entries

Remove Duplicates	Remove identified duplicate records

Text to Columns	Separate decimal portions from age values

Paste Special → Values	Convert formula results into static values

Number Formatting	Standardize date and currency display


📊 Missing Value Treatment

The following treatments were applied during the cleaning process:


Column	Cleaning Treatment

Customer ID	Replaced missing values with Unknown_ID

Gender	Replaced missing values with Unknown

Age	Replaced missing values with Unknown

City	Replaced missing values with Unknown

Last Purchase Date	Replaced missing values with Unknown

Purchase Amount	Applied a conditional formula to handle missing values

Feedback Score	Replaced missing values with 0

Country	Replaced missing values with Unknown


Signup Date and Email were inspected, and no blank values were identified during the review.

✅ Final Output

The final working sheet was prepared with selected columns and standardized values for further analysis.

The cleaning process focused on:

Improving consistency across text and categorical fields.

Handling missing values using defined rules.

Removing identified duplicate records.

Standardizing date and currency presentation.

Inspecting inconsistent phone number lengths.

Preparing a separate cleaned dataset for further processing.

Final validation is recommended before using the dataset for business reporting or decision-making.

🚀 Limitations and Future Improvements

Potential improvements for future iterations include:

Verifying duplicate removal using the correct business key.

Ensuring placeholder customer IDs do not affect customer counts.

Preserving missing-value indicators where zero could be misleading.

Validating phone numbers against appropriate numbering rules.

Ensuring dates and purchase amounts have consistent data types.

Recording original and final row counts and the number of duplicates removed.

Adding before-and-after data quality checks and summary statistics.

Exploring Python or Power BI for more repeatable cleaning and analysis workflows.


📁 Suggested Repository Structure

customer-sales-data-cleaning/
│
├── README.md
│
├── data/
│   └── messy_customer_sales_dataset.csv
│
├── output/
│   └── cleaned_customer_sales_dataset.xlsx
│
└── documentation/
    └── cleaning_summary.xlsx


Update the filenames and folder structure to match the files actually uploaded to the repository. If the dataset has redistribution restrictions, link to the original source instead of uploading another copy.

📝 Conclusion

This project demonstrates a practical data cleaning and preprocessing workflow using Microsoft Excel.

Through data inspection, duplicate detection, missing-value handling, text standardization, and formatting, the project aimed to improve dataset consistency and prepare customer sales data for future analysis and visualization.

Tools Used: Microsoft Excel
Project Category: Data Cleaning and Preprocessing
Organization: Swynex
Project Type: Internship Project 

<img width="860" height="326" alt="Cleanned Dataset" src="https://github.com/user-attachments/assets/fec7068b-83ba-48cf-a63f-489af1dfb95e" />

