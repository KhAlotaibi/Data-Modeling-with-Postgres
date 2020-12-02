# Data Modeling with Postgres

## Introduction 

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

They'd like a data engineer to create a Postgres database with tables designed to optimize queries on song play analysis, and bring you on the project. Your role is to create a database schema and ETL pipeline for this analysis. You'll be able to test your database and ETL pipeline by running queries given to you by the analytics team from Sparkify and compare your results with their expected results.

## Project Description

In this project, you'll apply what you've learned on data modeling with Postgres and build an ETL pipeline using Python. To complete the project, you will need to define fact and dimension tables for a star schema for a particular analytic focus, and write an ETL pipeline that transfers data from files in two local directories into these tables in Postgres using Python and SQL.


## How to run the code

`python sql_queries.py`
`python create_tables.py`
`python etl.py`

Then check the outcome in test.ipynb

## File Description 
The dataset is consists of tow log files, the first one is song data where we can extract the songs data table and artists data table, the other one is log data where we can extract the user data table and the time data table as well as the fact table songplays table.

## Table Schema
The fact table is songplays table consists of a primary key which is songplay_id, and other four dimensional tables (users table, time table, songs table, artists table)
the fact table is linked with the other table with keys(user_id, start_time, song_id, artist_id)

## Project Description 
* `Sql_queries.py`
Contains the insert statements, drop and create tables, and one query for finding the songs where the power of joins the table has been shown.
* `Create_table.py`
Here we created the database and the tables which statements been written in sql_queries.py
* `etl.py`
Reading and inserting the data in the log data to the database.
* `test.ipynb`
testing if the steps above is done correctly and the data has been successfully in the database.
