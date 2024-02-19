# Crowdfunding_ETL
## Project desription
For the ETL mini project, we worked in a group to practise building an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions to extract and transform the data. After we transformed the data, we have created four CSV files and useed the CSV file data to create an ERD and a table schema. Finally, we have uploaded the CSV file data into a Postgres database.

This was completed in a group of three: Drishti Patel, Rahul Gade and Puja Tiwari. We ensured collaboration and communication while working on different parts of the project and final completion.

## The instructions for this mini project were divided into the following subsections:
- Create the Category and Subcategory DataFrames
- Create the Campaign DataFrame
- Create the Contacts DataFrame
- Create the Crowdfunding Database

# Create the Category and Subcategory DataFrames
Follwing steps were taken to create the DataFrames
1. Load data from 'crowdfunding.xlsx' into a pandas DataFrame.
2. Create the 'category' DataFrame with columns 'category_id' (sequentially from 'cat1' to 'catn') and 'category' (containing unique category titles).
3. Export the 'category' DataFrame to 'category.csv' and save it to the GitHub repository.
4. Create the 'subcategory' DataFrame with columns 'subcategory_id' (sequentially from 'subcat1' to 'subcatn') and 'subcategory' (containing unique subcategory titles).
5. Export the 'subcategory' DataFrame to 'subcategory.csv' and save it to the GitHub repository.
6. Utilize the pandas library in Python for data manipulation, assuming the Excel file contains columns named 'Category' and 'Subcategory'.
   
# Create the Campaign DataFrame
1. Load data from 'crowdfunding.xlsx' into a pandas DataFrame.
2. Create a 'campaign' DataFrame with the following columns:
- "cf_id"
- "contact_id"
- "company_name"
- "description" (renamed from "blurb")
- "goal" (converted to float)
- "pledged" (converted to float)
- "outcome"
- "backers_count"
- "country"
- "currency"
- "launch_date" (renamed from "launched_at" and converted to datetime with UTC times)
- "end_date" (renamed from "deadline" and converted to datetime with UTC times)
- "category_id" (matching unique identification numbers from the "category_id" column in the 'category' DataFrame)
- "subcategory_id" (matching unique identification numbers from the "subcategory_id" column in the 'subcategory' DataFrame)
- Export the campaign DataFrame as campaign.csv and save it to your GitHub repository.
  
# Create the Contacts DataFrame
We have used the 1st option to create the Contacts DataFrame

## Option 1: Using Python dictionary methods
1. Import the contacts.xlsx file into a DataFrame.
2. Iterate through the DataFrame, converting each row to a dictionary.
3. Iterate through each dictionary, extract values from keys using a Python list comprehension, and add them to a new list.
4. Create a new DataFrame containing the extracted data.
5. Split each "name" column value into first and last names, placing each in a new column.
6. Clean and export the DataFrame as contacts.csv and save it to the GitHub repository.
   
# Create the Crowdfunding Database:
1. Inspect the four CSV files: 'category.csv', 'subcategory.csv', 'contacts.csv', and 'campaign.csv'.
2. Sketch an Entity-Relationship Diagram (ERD) using QuickDBD to represent the relationships between tables.
3. Save the database schema as a Postgres file named **crowdfunding_db_schema.sql** and upload it to GitHub repository.
## Database Creation in Postgres SQL:
1. Create a new Postgres database named 'crowdfunding_db'.
2. Using the database schema from step 4, create the tables in the correct order to handle foreign keys.
3. Import each CSV file into its corresponding SQL table.
4. Verify table creation by running a SELECT statement for each table.








