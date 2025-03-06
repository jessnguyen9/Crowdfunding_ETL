# Crowdfunding Data Analysis & ETL Project

## Overview
Conducted a thorough analysis of crowdfunding data, focusing on campaign performance, backer engagement, and funding success rates. The dataset, containing over 1,000 crowdfunding campaigns, was acquired from multiple sources, including Excel files. The project aimed to clean and transform the raw data, load it into a PostgreSQL database, and then analyze it to generate actionable insights for business stakeholders.

## Techniques & Tools
### Techniques
1. **Data Acquisition**
* Data was acquired from multiple sources, including Excel files containing crowdfunding campaign information and external APIs for contact information. Python libraries like pandas were utilized for reading and processing the data.
2. **Data Preparation**
* **Data Cleaning:** The data underwent various cleaning processes, including removing missing values, handling duplicates, and ensuring consistency in formatting.
* **Data Manipulation:** Using pandas, the data was transformed by converting columns to appropriate data types (e.g., converting dates from Unix timestamps to human-readable formats) and creating new features (e.g., splitting the "category & sub-category" column into separate category and subcategory columns).
* **Regex:** For extracting specific data points like the "contact_id" from the contact information, regex (regular expressions) was applied. This allowed for efficient extraction of the required details from nested JSON strings within the dataset.
3. **Data Analytics**

### Tools
* **QuickDBD:** Used for designing the database schema visually and exporting the SQL code to create the database structure.
* **Python (pandas, numpy):** pandas for data manipulation and cleaning; numpy for generating arrays and performing numeric operations.
* **PostgreSQL:** Relational database for storing and querying the transformed data.
* **Regex:** Extracted specific data (e.g., contact IDs) from unstructured text for further processing.
* **Jupyter Notebooks:** Enabled interactive execution and debugging of Python code during data transformations.


- Extracted and transformed data from the provided Excel files to create dataframes using Python and pandas.

- Cleaned and formatted the data, handling missing values and inconsistencies.
  
<img width="902" alt="Screenshot 2023-07-10 at 12 34 55 PM" src="https://github.com/m-janssens-boop/Crowdfunding_ETL/assets/127706155/87743cc5-e8a1-49b2-89a4-770226cadaaa">

- Exported the dataframes as CSV files: category.csv, subcategory.csv, campaign.csv, and contacts.csv.

- Designed the database schema based on the Entity Relationship Diagram (ERD) provided.

<img width="1284" alt="Screenshot 2023-07-10 at 12 35 42 PM" src="https://github.com/m-janssens-boop/Crowdfunding_ETL/assets/127706155/aa8a16aa-728e-4492-8bd6-c2c69140e092">

- Created tables in PostgreSQL with appropriate data types, primary keys, foreign keys, and constraints.

- Imported the CSV files into the respective database tables.

- Ran SQL queries on the database to analyze the crowdfunding data.

### References ###

[line 5 reference](https://sparkbyexamples.com/pandas/pandas-split-column/#:~:text=In%20Pandas%2C%20the%20apply(),to%20split%20into%20two%20columns)

[line 10 reference](https://stackoverflow.com/questions/2050637/appending-the-same-string-to-a-list-of-strings-in-python)
