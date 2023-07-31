# Data cleaning and creation of a database: videoculb. 

# 1. Project Description: 

This project focuses on cleaning a dataset and creating a functional database using MySQL Workbench. The dataset comprises information from a videoclub business that ceased operations a long time ago.

The primary objective of this project is to generate an operational database by extracting relevant information from the original dataset. The original database contains outdated and irrelevant data that needs to be cleaned and updated.


# 2. Data Cleaning
```
To prepare the dataset for the creation of the database in MySQL Workbench, the following steps and decisions were made to clean and transform the data. The actions are described for each table of the old dataset:

2.1 actor

Contains information about actor names and surnames. Actions taken:
    Converted the content of each row to lowercase.
    Removed duplicated rows.
    Deleted information in the "last_update" column, as the old videoclub no longer exists.


2.2 category

Contains information about the category of each film (e.g., action, comedy, etc.). Actions taken:
    Deleted information in the "last_update" column, as the old videoclub no longer exists.


2.3 film

Contains information related to available films. Actions taken:
    Added two columns: "subtitles_id" and "original_language_id" to enhance the film repository.
    Removed the "last_update" and "rental_duration" columns, as they do not provide useful information for the new videoclub.
    Set default values for certain columns, as the information in the old database is outdated. For example, the "rental_price" column contained prices from almost 20 years ago.


2.4 inventory

Contains information about the number of copies of each film, but appears to be incomplete. Actions taken:
    Estimated the total number of films since the inventory seems to be incomplete. The maximum value in the "inventory_id" column is significantly lower than that in the "inventory_id" column of the "rental" table, suggesting that there should be around 1000 films.
    Deleted the information related to the store that contains each title, as there will be only one store.


2.5 language, original language, and subtitles

"Language" contains information about the language of each film. Actions taken:
    Incorporated information related to the original language and subtitles to provide better film information in the new database.


2.8 rental

Contains information about clients, telephone numbers, etc. Actions taken:
    Reset most of the columns to include new values, as preserving the old customers is unlikely.


2.9 actor_per_film

Relates information between films and actors appearing in each film.
    Changed the name of the old table from "Old_HDD" to "actor_per_film".
```



# 3. Creation of the database:

A new database has been created using MySQL Workbench, establishing the relationships between the tables. The code to implement the entire database, along with some example queries, has been included.

Please refer to the provided code files for the complete implementation and the specific queries.




# 4. Documents in this repository:

This repository consists of the following documents and folders:

## Data folder
It contains two subfolders:
Cleaned: Contains cleaned .csv documents representing the new database tables.
Raw: Contains raw .csv documents representing the old database tables.

## Jupyter notebook folder
Contains a Jupyter notebook that provides detailed information about the data cleaning process.

## Src folder
Contains a .sql document that includes the code to implement the new database. This document also includes the necessary data.

## SQL folder
Contains a .sql document that includes sample queries to demonstrate how the database is structured.

Please refer to the respective folders and files for accessing and understanding the data, code, and queries associated with this project.


