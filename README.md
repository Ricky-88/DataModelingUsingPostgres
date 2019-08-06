# DataModelingUsingPostgres
## Objective
To build an ETL pipeline using Python and design data modeling with Postgres 

## Introduction
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

They'd like a data engineer to create a Postgres database with tables designed to optimize queries on song play analysis. My role 
is to create a database schema and ETL pipeline for this analysis. 


## Project Description

Using the song and log datasets, I created a star schema optimized for queries on song play analysis. This includes the following tables.

### Fact Table
<b> songplays </b> - records in log data associated with song plays i.e. records with page NextSong <br />
songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent
### Dimension Tables
<b> users </b> - users in the app <br />
user_id, first_name, last_name, gender, level <br />

<b> songs </b>- songs in music database <br />
song_id, title, artist_id, year, duration <br />
<br />
<b> artists </b>  - artists in music database <br />
artist_id, name, location, latitude, longitude <br /> 
<br />
<b> time </b>  - timestamps of records in songplays broken down into specific units <br /> 
start_time, hour, day, week, month, year, weekday

## Project Steps

### Create Tables
1. Write CREATE statements in sql_queries.py to create each table.
2. Write DROP statements in sql_queries.py to drop each table if it exists.
3. Run create_tables.py to create your database and tables.
4. Run test.ipynb to confirm the creation of tables with the correct columns. 

### Build ETL Pipeline
Develop ETL processes for each table in the etl.ipynb notebook. Use it to complete etl.py, where the entire datasets will get processed.
