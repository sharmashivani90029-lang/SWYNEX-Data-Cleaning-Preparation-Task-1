# SWYNEX-Data-Cleaning-Preparation-Task-1
Cleaning and preparation of the Netflix Movies and TV Shows dataset using Python (pandas) - SWYNEX Technologies Data Analyst Internship,# Netflix Data Cleaning & Preparation

## Overview
This project is Task 1 of the SWYNEX Technologies Data Analyst Internship. 
The goal was to clean and prepare a raw dataset for analysis using Python (pandas).

## Dataset
- **Source:** Netflix Movies and TV Shows dataset (`Netflix_Raw_Data.csv`)
- **Original size:** 271 rows, 12 columns
- **Cleaned size:** 250 rows, 13 columns

## Steps Performed

### 1. Handling Missing Values
- Dropped rows that were completely empty
- Filled missing values in `director`, `cast` with "Unknown"
- Filled missing `listed_in` with "Unknown" and `description` with "No description available"
- Filled missing `country` and `rating` with the most frequent value (mode)
- Filled missing `release_year` with the median year

### 2. Fixing Incorrect Data Types
- Converted `release_year` to numeric type
- Converted `date_added` to proper datetime format
- Standardized the `type` column (fixed inconsistent casing like "movie", "MOVIE", "tv show")
- Split the `duration` column into two separate numeric columns: `duration_minutes` (for Movies) and `duration_seasons` (for TV Shows)

### 3. Removing Duplicate Records
- Identified and removed exact duplicate rows from the dataset

### 4. Fixing Inconsistent Values
- Corrected invalid future `release_year` values
- Fixed Movies with 0 or negative duration by replacing with the median movie duration

## Tools Used
- Python
- pandas, numpy
- Jupyter Notebook (VS Code)

## Output
The final cleaned dataset is saved as `Netflix_Cleaned_Data.csv` in the `data/` folder.

## Author
Shivani Sharma
