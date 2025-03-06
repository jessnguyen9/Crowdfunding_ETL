# Crowdfunding Data Analysis & ETL Project

## Overview
Conducted a thorough analysis of crowdfunding data, focusing on campaign performance, backer engagement, and funding success rates. The dataset, containing over 1,000 crowdfunding campaigns, was acquired from multiple sources, including Excel files. The project aimed to clean and transform the raw data, load it into a PostgreSQL database, and then analyze it to generate actionable insights for business stakeholders.

## Techniques & Tools
### Techniques
1. **Data Acquisition**

Data was acquired from multiple sources, including Excel files containing crowdfunding campaign information and external APIs for contact information. Python libraries like pandas were utilized for reading and processing the data.

2. **Data Preparation**
**Data Cleaning:**
* Identified and removed incomplete or missing values from the datasets. For instance, any campaigns with missing campaign outcomes or backer counts were handled to ensure data integrity.
* Converted date columns (e.g., launch date and end date) from UNIX timestamp format to human-readable datetime formats.

<img width="902" alt="Screenshot 2023-07-10 at 12 34 55 PM" src="https://github.com/m-janssens-boop/Crowdfunding_ETL/assets/127706155/87743cc5-e8a1-49b2-89a4-770226cadaaa">

**Data Manipulation:** 
* Transformed various columns to the appropriate data types to facilitate analysis (e.g., converting goal and pledged amounts to float).
* Created new features such as category_id and subcategory_id, which linked each campaign to a specific category and subcategory using a reference table.

**Regex:** 

For extracting specific data points like the "contact_id" from the contact information, regex (regular expressions) was applied. This allowed for efficient extraction of the required details from nested JSON strings within the dataset.

3. **Data Analytics**
* The cleaned and prepared data was imported into a PostgreSQL database, where SQL queries were used to perform deeper analysis, such as identifying trends, calculating success rates, and examining backer behavior.
* The database was structured using foreign key relationships to ensure data integrity and optimize query performance. Analysis was conducted on multiple dimensions, including goals, pledged amounts, and campaign outcomes.
## ETL Process & Database Design
After performing the data analysis, we designed and implemented an ETL (Extract, Transform, Load) pipeline to efficiently structure and store the cleaned data in a PostgreSQL database. The schema is structured to allow for easy querying and analysis across different dimensions such as campaigns, categories, subcategories, and contacts.

<img width="1284" alt="Screenshot 2023-07-10 at 12 35 42 PM" src="https://github.com/m-janssens-boop/Crowdfunding_ETL/assets/127706155/aa8a16aa-728e-4492-8bd6-c2c69140e092">

### Tools
* **QuickDBD:** Used for designing the database schema visually and exporting the SQL code to create the database structure.
* **Python (pandas, numpy):** pandas for data manipulation and cleaning; numpy for generating arrays and performing numeric operations.
* **PostgreSQL:** Relational database for storing and querying the transformed data.
* **Regex:** Extracted specific data (e.g., contact IDs) from unstructured text for further processing.
* **Jupyter Notebooks:** Enabled interactive execution and debugging of Python code during data transformations.

## Challenges
- **Handling Semi-Structured Data:** The contact information was stored as JSON-like strings within a single column. This format made it difficult to directly manipulate or analyze the data, as each entry was essentially a raw string rather than a fully parsed structure.
- **Inconsistent Data:** Initially, the dataset had some inconsistencies, such as extra rows or non-standardized column headers. This required cleaning before the extraction of structured data.
- **Missing or Invalid Data:** Some rows may have missing contact information or improperly formatted JSON.

## References ###

[line 5 reference](https://sparkbyexamples.com/pandas/pandas-split-column/#:~:text=In%20Pandas%2C%20the%20apply(),to%20split%20into%20two%20columns)

[line 10 reference](https://stackoverflow.com/questions/2050637/appending-the-same-string-to-a-list-of-strings-in-python)
