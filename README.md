# Pandemic Database Project

### This project is part of a data normalization and analysis task using MySQL. The dataset contains information about various infectious disease cases across multiple entities and years.

## Tasks Completed

### 1. Schema Setup and Data Import
- Created the `pandemic` schema using SQL.
- Imported the `infectious_cases` dataset via MySQL Workbench Import Wizard.
- Inspected the dataset for structure and repetition.

### 2. Data Normalization (to 3NF)
- Created two normalized tables: `entities` and `cases`.
- Migrated data from `infectious_cases` into these new tables.
- Removed redundancy by extracting repeating `Entity` and `Code` values into the `entities` table and referencing them by foreign key in `cases`.

### 3. Data Analysis
- Calculated aggregate statistics for the `number_rabies` field:
  - Total, average, minimum, and maximum values per entity.
- Filtered out NULL or empty values.
- Displayed top 10 entities by average number of rabies cases in descending order.

### 4. Date Calculation
- Created additional columns for:
  - Start of the year (`YYYY-01-01`).
  - Current date (`CURDATE()`).
  - Difference in years using `TIMESTAMPDIFF`.

### 5. Custom SQL Function
- Defined a SQL function `year_diff(y INT)` to compute the number of years between a given year and today.
- Used this function in queries to calculate year differences directly.

## Technologies Used
- MySQL 8.x
- MySQL Workbench

## Author
- Oleksii Andrieiev
