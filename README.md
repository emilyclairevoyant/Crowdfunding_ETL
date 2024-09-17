# Mini Project Crowd Funding Analysis
![(https://www.impactguru.com/info/wp-content/uploads/2023/03/crowdfunding-featured-image.jpg)](https://www.impactguru.com/info/wp-content/uploads/2023/03/crowdfunding-featured-image.jpg)

**ETL Mini Project**

Collaboratively developed an ETL pipeline utilizing Python, Pandas, dictionary methods, and regular expressions for data extraction and transformation. After processing the data, generated four CSV files, which were then used to design an ERD and define a table schema. Ultimately, the CSV data was uploaded into a PostgreSQL database.

**Mini Project Instructions**
The steps for this mini project are divided into the following sections:

1. Create the Category and Subcategory DataFrames
Category DataFrame: Extract and transform data from the crowdfunding.xlsx file to create a category DataFrame with:

* A `category_id` column with sequential entries from "cat1" to "catn", where n is the number of unique categories.
* A `category` column containing only the category titles.
Export the DataFrame as `category.csv` and upload it to your GitHub repository.

Subcategory DataFrame: Extract and transform data from the crowdfunding.xlsx file to create a subcategory DataFrame with:
* A `subcategory_id` column with sequential entries from "subcat1" to "subcatn", where n is the number of unique subcategories.
* A `subcategory` column containing only the subcategory titles.
Export the DataFrame as `subcategory.csv` and upload it to your GitHub repository.

2. Create the Campaign DataFrame
Extract and transform the `crowdfunding.xlsx` data to build a campaign DataFrame with the following columns:
`cf_id`, `contact_id`, `company_name`, `description (formerly blurb)`, `goal (converted to float)`, `pledged (converted to float)`, `outcome`, `backers_count`, `country`, `currency`.
`launch_date` (converted from launched_at to datetime format) and `end_date` (converted from deadline to datetime format).
`category_id` and `subcategory_id` linked to the respective IDs in the category and subcategory DataFrames.
Export the DataFrame as `campaign.csv` and upload it to your GitHub repository.

3. Create the Contacts DataFrame
Option 1: Import `contacts.xlsx` into a DataFrame, iterate over it, and:
Convert each row to a dictionary.
Use a Python list comprehension to extract values for each row and create a new DataFrame.
Split the name column into separate first and last name columns.
Clean and export the DataFrame as `contacts.csv` and upload it to your GitHub repository.

4. Create the Crowdfunding Database
Inspect the four CSV files and sketch an ERD , we have used Postgres.
Use the ERD to create a table schema for each CSV file, including data types, primary keys, foreign keys, and constraints.
Save the schema as a Postgres file `(crowdfunding_db_schema.sql)` and upload it to your GitHub repository.
Create a new Postgres database `(crowdfunding_db)` and create the tables in the correct order to manage foreign keys.
Verify table creation with `SELECT` statements and import each CSV file into its corresponding SQL table.
Confirm that each table contains the correct data by running `SELECT` queries.

**Insights gathered from the data**

Note: All graphs from our data analysis are stored in the Resources folder.

Theater leads in campaigns, with plays being the dominant subcategory; Journalism ranks lowest in campaigns, with worldmusic as the smallest subcategory.

Theater had the most successful outcomes among categories, with plays leading in subcategories.

The US tops the list for successful campaigns.
