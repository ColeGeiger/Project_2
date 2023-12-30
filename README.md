# Project 2 - Crowdfunding_ETL

**Team Members**
-Cole Geiger,
-Matthew Yackee,
-Grace Long,
-Paul Ji
# **Introduction**
In this project, we practiced building an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform the data. After, we transformed the data, created four CSV files and use the CSV file data to create an ERD and a table schema. Finally, we uploaded the CSV file data into a Postgres database.
# **Instructions**
-Create the Category and Subcategory DataFrames
-Create the Campaign DataFrame
-Create the Contacts DataFrame
-Create the Crowdfunding Database
# **Sources of Data**
-crowdfunding.xlsx
-contacts.xlsx
# **Create the Category and Subcategory DataFrames**
Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:
-A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
-A "category" column that contains only the category titles
<img width="190" alt="category_DataFrame" src="https://github.com/ColeGeiger/Crowdfunding_ETL/assets/141586099/8f6a1c6e-e422-42a9-af48-8fd37fb7f587">

Export the category DataFrame as category.csv and save it to your GitHub repository.
Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:

-A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
-A "subcategory" column that contains only the subcategory titles
<img width="250" alt="subcategory_DataFrame" src="https://github.com/ColeGeiger/Crowdfunding_ETL/assets/141586099/b004f19e-98c3-4c38-8308-fe120db175b8">
Export the subcategory DataFrame as subcategory.csv and save it to your GitHub repository.

# **Create the Campaign DataFrame**
Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:
-The "cf_id" column
-The "contact_id" column
-The "company_name" column
-The "blurb" column, renamed to "description"
-The "goal" column, converted to the float data type
-The "pledged" column, converted to the float data type
-The "outcome" column
-The "backers_count" column
-The "country" column
-The "currency" column
-The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
-The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
-The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
-The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame
<img width="1074" alt="campaign_DataFrame" src="https://github.com/ColeGeiger/Crowdfunding_ETL/assets/141586099/4cfb34bc-6eed-4903-8b33-c1e57867ab1e">
Export the campaign DataFrame as campaign.csv and save it to your GitHub repository.

# **Create the Contacts DataFrame**
Choose one of the following two options for extracting and transforming the data from the contacts.xlsx Excel data:
-Option 1: Use Python dictionary methods.
-Option 2: Use regular expressions.

If you chose Option 1, complete the following steps:

-Import the contacts.xlsx file into a DataFrame.
-Iterate through the DataFrame, converting each row to a dictionary.
-Iterate through each dictionary, doing the following:
-Extract the dictionary values from the keys by using a Python list comprehension.
-Add the values for each row to a new list.
-Create a new DataFrame that contains the extracted data.
-Split each "name" column value into a first and last name, and place each in a new column.
-Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.

If you chose Option 2, complete the following steps:

-Import the contacts.xlsx file into a DataFrame.
-Extract the "contact_id", "name", and "email" columns by using regular expressions.
-Create a new DataFrame with the extracted data.
-Convert the "contact_id" column to the integer type.
-Split each "name" column value into a first and a last name, and place each in a new column.
-Clean and then export the DataFrame as contacts.csv and save it to your GitHub repository.
<img width="415" alt="contact_DataFrame_final" src="https://github.com/ColeGeiger/Crowdfunding_ETL/assets/141586099/293e3811-3de9-430a-a422-4aa4356d4a05">

# **Create the Crowdfunding Database**
-Inspect the four CSV files, and then sketch an ERD of the tables by using QuickDBDLinks to an external site.
![screenshot_2023-12-28_at_9 13 14___am_720](https://github.com/ColeGeiger/Crowdfunding_ETL/assets/141586099/a353b7de-ca04-4de5-9d76-45e3c83fa32b)


-Use the information from the ERD to create a table schema for each CSV file.

-Save the database schema as a Postgres file named crowdfunding_db_schema.sql, and save it to your GitHub repository.

-Create a new Postgres database, named crowdfunding_db.

-Using the database schema, create the tables in the correct order to handle the foreign keys.

-Verify the table creation by running a SELECT statement for each table.

-Import each CSV file into its corresponding SQL table.

-Verify that each table has the correct data by running a SELECT statement for each
