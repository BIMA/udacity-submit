# Sparkify Databases Project

## Objective

Sparkify is a music streaming startup. As a startup, Sparkify would handle huge data as they grow up to. If Sparkify still using conventional method like store the data in JSON format, it would be a problem one day. In spite of to handle big data, Sparkify should analyze their data to make decision to speed up their business. With two goals, Sparkify should store their data into tabular format using PostgreSQL. In this project, there are two programs could be used to create tables and run an ETL process automatically.

There are three tables i.e. song table, user table, artist table, time table, and songplay table

## Database Schema

#### Song table

Table that store song information

Columns schema:
- song_id varchar
- title varchar
- artist_id varchar
- year int
- duration float

#### User table

Table that store user information

Columns schema:
- user_id int
- first_name varchar
- last_name varchar
- gender varchar
- level varchar

#### Artist table

Table that store artist of particular song information

Columns schema
- artist_id varchar
- name varchar
- location text
- latitude float
- longitude float

#### Time table

Table that store timestamp of the streamed song from user

Columns schema:
- start_time bigint
- hour int
- day int
- week int
- month int
- year int
- weekday int

#### Songplay table

Table result of join another table. This table is for analytical purposes

Columns schema:
- songplay_id int
- start_time bigint
- user_id int
- level varchar
- song_id varchar
- artist_id varchar
- session_id int
- location text
- user_agent text

## ETL Pipeline

The pipelines of this project are:
1. Transform song, artist, and user data from JSON format into tabular format
2. Load song, artist, and user table to Postgre database
3. Transform log data into time table and load to Postgre database
4. Transform log data into songplay table and joining with song, artist, and user table
5. Load songplay table to Postgre

## How to install database

`python create_tables.py`

## How to run ETL process

`python etl.py`