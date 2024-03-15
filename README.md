# Mini Project: Crowdfunding Data Analysis

## Overview
This project focuses on creating and analyzing DataFrames from crowdfunding data, utilizing Excel and CSV files. The process includes extracting, transforming, and structuring data for analysis.

## Functionality

### Create Category and Subcategory DataFrames
- **What it does:** Generates `category` and `subcategory` DataFrames from `crowdfunding.xlsx`.
- **How it works:** 
  - Categories: Extracts unique categories, assigns sequential IDs, and stores them in the `category` DataFrame.
  - Subcategories: Similar process, with unique sequential IDs.
  - Each DataFrame is exported as a CSV file.

### Create Campaign DataFrame
- **What it does:** Constructs a DataFrame for crowdfunding campaigns.
- **How it works:** 
  - Extracts campaign details and financial data from `crowdfunding.xlsx`.
  - Involves renaming, formatting, and type conversion of columns.
  - Integrates `category_id` and `subcategory_id` from respective DataFrames.
  - Exports the DataFrame as a CSV file.

### Create Contacts DataFrame
- **What it does:** Creates a DataFrame for contact information.
- **How it works:** 
  - Utilizes Python dictionaries or regular expressions to process data from `contacts.xlsx`.
  - Splits names, extracts essential information, and converts data types.
  - Cleans and exports the DataFrame as `contacts.csv`.

### Crowdfunding Database
- **Primary Keys and Foreign Keys:**
  - **Category DataFrame:** Utilizes `category_id` as a primary key, uniquely identifying each category.
  - **Subcategory DataFrame:** Features `subcategory_id` as a primary key, uniquely identifying each subcategory.
  - **Campaign DataFrame:** Contains a primary key (likely `campaign_id` or similar), and two foreign keys: `category_id` and `subcategory_id`, linking to the Category and Subcategory DataFrames respectively.
  - **Contacts DataFrame:** Employs a primary key (such as `contact_id`), which is likely used as a foreign key in the Campaign DataFrame to establish a link between campaigns and their contacts.
