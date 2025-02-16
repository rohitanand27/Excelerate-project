# Cleaned SLU Opportunity Wise Data

## Overview
This repository contains a cleaned and preprocessed dataset based on the SLU Opportunity Wise data. The dataset has undergone various data cleaning steps, including handling missing values, standardizing categorical data, and feature engineering.

## Data Cleaning Steps
1. **Loading the Dataset**: The raw dataset is loaded using `pandas.read_csv()`.
2. **Initial Inspection**:
   - Display dataset information (`df.info()`).
   - Show the first 10 rows (`df.head(10)`).
   - Provide summary statistics (`df.describe()`).
   - Identify duplicate rows (`df.duplicated().sum()`).
   - Count missing values (`df.isnull().sum()`).
3. **Date Formatting**:
   - Convert date-related columns to `datetime` format to ensure consistency.
4. **Handling Missing Values**:
   - Fill missing `Institution Name` values with "Unknown".
   - Fill missing `Opportunity Start Date` values with the mode of the column.
   - Remove rows where `Apply Date` is missing.
5. **Standardizing Categorical Data**:
   - Convert categorical text to title case and strip whitespace.
   - Normalize variations of "Saint Louis".
6. **Removing Unnecessary Columns**:
   - Drop the `Time to Apply` column if it exists.
7. **Removing Duplicates**:
   - Remove duplicate rows to ensure data integrity.
8. **Feature Engineering**:
   - Create a new `Age` column by calculating the difference between today’s date and `Date of Birth`.
   - Create an `Opportunity Duration` column based on the difference between `Opportunity End Date` and `Opportunity Start Date`.

## Output
The cleaned dataset is saved as `Cleaned_SLU_Opportunity_Data.csv`.

## How to Use
1. Clone this repository:
   ```sh
   git clone https://github.com/your-repo/slu-opportunity-data.git
   cd slu-opportunity-data
   ```
2. Run the data preprocessing script (if applicable):
   ```sh
   python clean_data.py
   ```
3. Use the `Cleaned_SLU_Opportunity_Data.csv` file for analysis or further processing.

## Dependencies
Ensure you have the following Python libraries installed:
```sh
pip install pandas numpy
```

## License
This project is licensed under the MIT License.

