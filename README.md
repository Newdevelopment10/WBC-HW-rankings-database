# WBC-rankings-database
Created a database of the top 40 heavyweights in the WBC + the WBC HW champion (current as of April 2024). The following are the instructions for creating the database in PostgreSQL and the SQL for creating the tables and columns within the tables:
PostgreSQL was downloaded for free from their website. The files were placed in the appropriate directory. PGAdmin4 was downloaded as well. PG Admin4 is
the graphic interface to use on this RDMS (Relation Database Management System). Using the interface, a data was created by right-clicking on PostgreSQL 16, hovering on Create, click Database, name database, click on Save. Once database is created, click on Schema, right click on tables, click on Query Tool, then type in the following code to create each table:

boxer_rankings-
CREATE TABLE boxer_rankings (
boxer_id SMALLSERIAL PRIMARY KEY NOT NULL,
weight_division VARCHAR(50) NOT NULL,
person_id VARCHAR(50),
stat_id INT)

boxer_stats
CREATE TABLE boxer_stats (
stat_id INT PRIMARY KEY,
first_name VARCHAR(50),
last_name VARCHAR(50),
weight_class INT,
wins INT,
losses INT,
draws INT,
knockouts INT,
height INT,
reach INT)

boxer_info
CREATE TABLE boxer_stats (
person_id VARCHAR(50) PRIMARY KEY,
first_name VARCHAR(50),
last_name VARCHAR(50),
weight_class INT,
weight_classes_fought INT,
stat_id INT,
year_turned_pro INT,
stance VARCHAR(50),
nationality VARCHAR(50),
year_born INT)

The tables were filled using the following format:
INSERT INTO (column 1, column 2, column n...)
VALUES (input value according to syntax for data type)

A list of queries that I used to obtain information and aggregate results are in the Word document in this repository.
