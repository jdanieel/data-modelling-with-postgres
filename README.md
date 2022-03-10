# Data Modelling with Postgres

## Introduction
This repo contains files required to run an ETL process in order to create a database in Postgres. They are part of one of the projects required in Udacity's Data Engineering Nanodegree, called Data Modelling with Postgres.

## Context
In this project, as the Data Engineer of a fictional music startup called Sparkify, I had to create a database in Postgres using .json files containing song and songplays data in order to provide tables in which the analytics team can perform some queries to understand better users' behaviour. In this process, I created the tables' schemas and wrote the scripts in Python used for the ETL pipeline, using best practices in terms of documentation, data quality checks and code writing.

## Files

The repo contains the following folders and files:

* `data` folder: contains all the data files used as the source of the ETL pipeline, which are split among two folders: `song_data` folder, which contains `.json` files containing metadata about song and the artist of the song, and `log_data` folder, which contains `.json` files that represent activity logs from events of the Sparkify app;
* `create_tables.py`: script that drops and creates the database tables;
* `etl.py`: script that reads and processes each `.json` data file from the `data` folder and then loads the processed data into the tables;
* `sql_queries.py`: file containing all the SQL queries that will be used in the scripts to drop, create and insert data into the tables;
* `README.md`: the file you are reading right now :)

## Running the Scripts

### Dependencies
You need to have the library `psycopg2` installed at your environment in order to make the connection with your Postgres database. The easiest way to do this is using pip install, executing this on your terminal:

```pip install psycopg2-binary```

More info about this process can be found at the [psycopg2 documentation](https://www.psycopg.org/docs/install.html).

### Steps
In order to properly run the scripts, do as follows:

* First, run `create_tables.py` in order to create the database and the tables that are necessary for the ETL processes;
* Second, run `etl.py` to read and process the data from the .json files. Make sure to have `sql_queries.py` and the folder `data` at the same directory as `etl.py`.
