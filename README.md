# Capstone_part1

## COVID-19 Data Import 
### Introduction:
The Covid 19 pandemic has wreaked havoc and led to the dramatic loss of lives and livelihoods. Its impact continues to affect the way in we live and interact. In this project, I analyzed sample data related to COVID-19 cases as recorded from January 2019 to December 2020.

This repository contains:
- ### Part1.ipynb
     This script imports COVID-19 data from the provided URL into a PostgreSQL database. It utilizes the `psycopg2` library to establish a connection with the database and the `pandas` library to read the CSV file.
- ### SQL_Queries
    This is an SQL file containing all the queries used to analyze and generate insight from the data.
- ### Outputs folder
    This folder contains screenshots of the outputs from running the queries.

## Prerequisites

- Python 3.x
- PostgreSQL database server
- Required Python libraries: `psycopg2`, `pandas`

## Setup

1. Create a database and a table called covid_19_data to hold the data in Postgresql.
   
2. Install the required Python libraries:
   pip install psycopg2 pandas

3. Update the connection details in Part1.ipynb script:
  conn = get_db_connection('<host>', '<database>', '<user>', '<password>')
  Replace <host>, <database>, <user>, and <password> with your PostgreSQL server details.
  

## Notes 
The script assumes that the provided CSV file has columns with the following names: 'SNo', 'ObservationDate', 'Province', 'Country', 'LastUpdate', 'Confirmed', 'Deaths', 'Recovered'. If your CSV file has different column names, please adjust the script accordingly.
The 'ObservationDate' column in the CSV file is expected to be in the format '%m/%d/%Y'. If your date format is different, modify the datetime.strptime() function accordingly.
