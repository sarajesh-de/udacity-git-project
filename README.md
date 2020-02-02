# Sparkify Analytical Reporting 

Sparkify wants to analyse the data they've been collecting on songs and user activity on their new music streaming app, and this datamart will enable to analytical team to analyse what songs the users are listing.
User activities of the Spartify app are stored in a directory in JSON format,Sparkify Analytical Reporting sources this data and load it into the datamart to enable for more optimised queries.


## Platform

**ETL : **Python ,Pandas
**Database : **Postgres
**Data Model :**Star Schema

## Design Consideration

Records not filtered out even when song_id,artist_id is having the value 'None', and this was done so that we don't filter out the data. Duplicate records are ignored

## Schema Design

| Table Name  |  Description |
| ------------ | ------------ |
|  Users |   |
|  Songs |   |
|   |   |
|   |   |


# # Running the tests

- Need to run the create_table.py and this has to be run first so that the required tables are created for the run.
			python create_tables.py
- Once the tables are created we can run the etl.py which loads the data from the json files to Sparkify Analytical datamart
			python etl.py



Files| Description
------------ | -------------
Create_tables.py | creates the sparkify database and tables 
etl.py | reads the json file and load the data into sparkify database
sql_queries.py | contains the DDL and DML scripts
test.ipynb | notebook to validate the data
etl.ipynb | notebook to test and validate the script
