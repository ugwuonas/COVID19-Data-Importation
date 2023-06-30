# Capstone_part1

## COVID-19 Data Import 
### Introduction:
The Covid 19 pandemic has wreaked havoc and led to the dramatic loss of lives and livelihoods. Its impact continues to affect the way we live and interact. In this project, I analyzed sample data related to COVID-19 cases as recorded from January 2019 to December 2020. This code is used to download a CSV file containing COVID-19 data and import it into a PostgreSQL database. It utilizes the requests, psycopg2, os, csv, and pandas libraries

This repository contains:
- ### Part1.ipynb
     This script imports COVID-19 data from the provided URL into a PostgreSQL database. It utilizes the `psycopg2` library to establish a connection with the database, the requests, os, csv, and pandas libraries.
- ### SQL_Queries
    This is an SQL file containing all the queries used to analyze and generate insight from the data.
- ### Outputs folder
    This folder contains screenshots of the outputs from running the queries.

## Prerequisites
Before running the code, ensure that the following prerequisites are met:

Python 3.x is installed on your system.
Required packages are installed. You can install them using pip:
- Python 3.x is installed on your system.
- PostgreSQL database server
- Required packages(Python libraries: `psycopg2`, `pandas`) are installed. You can install them using pip: 
  

## Instructions
Follow these steps to run the code successfully:

1. Download the code file and save it with a .py extension (e.g., covid_data_import.py).

2. Set up the PostgreSQL database:
   - Ensure that you have a PostgreSQL server running.
   - Create a new database (e.g., 'Capstone').
     
3. Set the environment variables:

Set the user environment variable to your PostgreSQL username. For example:
export user=your_username
Set the password environment variable to your PostgreSQL password. For example:

export password=your_password
   - Set the user environment variable to your PostgreSQL username. For example: export user=your_username
   - Set the password environment variable to your PostgreSQL password. For example: export password=your_password
     
5. Download the COVID-19 data file:
   - Specify the URL of the file to download in the URL variable.
   - Set the filename variable to the desired name of the downloaded file.
   - Run the code to download the file using the download_file function.
     
6. Connect to the PostgreSQL database:
   - Modify the get_db_connection function parameters if necessary (host, database, user, password).
   - Call the get_db_connection function to establish a connection to the database.
     
7. Load the data into the PostgreSQL database:
   - The CSV file is read into a Pandas DataFrame.
   - Each row of the DataFrame is inserted into the PostgreSQL database using a cursor.
   - Adjust the SQL query and table structure to match your database schema if needed.
     
8. Close the cursor and connection:
   - After the data import is complete, close the cursor and connection to the database.
### Notes 
The script assumes that the provided CSV file has columns with the following names: 'SNo', 'ObservationDate', 'Province', 'Country', 'LastUpdate', 'Confirmed', 'Deaths', 'Recovered'. If your CSV file has different column names, please adjust the script accordingly.
The 'ObservationDate' column in the CSV file is expected to be in the format '%m/%d/%Y'. If your date format is different, modify the datetime.strptime() function accordingly.

## Troubleshooting
If you encounter any issues or errors while running the code, consider the following:
- Ensure that the PostgreSQL server is running and accessible.
- Verify that the PostgreSQL credentials and database details are correct.
- Check your internet connection and ensure that you can access the file URL.
- Make sure you have the necessary permissions to read and write files and access the database.

## Disclaimer
This code is provided as-is without any warranties. Use it at your own risk. The author is not responsible for any damages or data loss caused by running this code.

