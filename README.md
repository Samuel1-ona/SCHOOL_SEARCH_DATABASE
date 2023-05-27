# SCHOOL_SEARCH_DATABASE

# INTRODUCTION

When using the website connected to the database, students can search through all the necessary fields in the school search database. The database is a central repository or a datapipeline that will hold data about the institution, as well as information about the country, city, state, field of study, department, and website that links to the institution.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# FIELDS DEFINITIONS

* ``` School_name```: Contains all the school names.
* ``` Country```:     Contains the target countries (Canada and the USA).
* ``` Country_id```:  Contains all the contry postal code
* ``` State```:       Contains all the state base on the country.
* ``` City```:        Contains all the cites base on the country.
* ``` Fields```:      Contains all the selected fields for each student.
*  ```Department```:  Contains all the selected department base on the fields for each student.
* ``` website_link```: Contains all the links to each school portals.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# CREATING OF DATABASE 

```CREATE DATABASE school_search_database;  -- Creating the database for the school search data```

# CREATING OF TABLE

```
CREATE TABLE school_search -- The table that contains all the school search data 

(
 school_name CHAR(100) NOT NULL,
 country CHAR(50) NOT NULL,
 country_id INT NOT NULL,
 state CHAR(50) NOT NULL,
 city CHAR(50) NOT NULL,
 field CHAR(50) NOT NULL,
 department CHAR(50) NOT NULL,
 website_link VARCHAR(512) NOT NULL,   -- NOT NULL prevent any NULL values  from being inserted
 
 PRIMARY KEY (field, department)   -- The PRIMARY KEY automatically prevent the insertion of duplicate values in the id column
 
 );
 
 ```
