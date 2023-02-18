# Climate Analysis in Honolulu, Hawaii

Welcome to the Climate Analysis project in Honolulu, Hawaii.

![Screenshot_20230218_112847](https://user-images.githubusercontent.com/113273722/219877543-81d68bf9-4759-436b-b25c-23f872173375.png)![Screenshot_20230218_112918](https://user-images.githubusercontent.com/113273722/219877553-8514d861-35ca-46cd-80eb-7b9df8300404.png)




## Project Overview

The purpose of this project is to conduct a basic climate analysis and data exploration of a climate database for Honolulu, Hawaii.

The analysis is conducted using ***Python***, ***SQLAlchemy ORM queries***, ***Pandas***, and*** Matplotlib***.

The climate database contains two tables, ***station*** and ***measurement***, which are used to perform precipitation and station analyses.

After completing the analysis, a Flask API is designed based on the queries developed in the analysis.

The API provides routes for retrieving precipitation data, station data, and temperature observations for a specified time range

## Prerequisites

The following tools and technologies are required to run the project:

* Python
* Jupyter Notebook
* Flask
* Pandas
* SQLAlchemy
* Matplotlib

## Climate Analysis
In this section, I'll use Python and SQLAlchemy to perform a precipitation and station analysis of the climate data.

## ***Precipitation Analysis***
The precipitation analysis is performed using the following steps:

1- Find the most recent date in the dataset.

2- Using that date, get the previous 12 months of precipitation data.

3- Select only the "date" and "prcp" values.

4- Load the query results into a Pandas DataFrame, and set the index to the "date" column.

5- Sort the DataFrame values by "date".

6- Plot the results using the DataFrame plot method.

7- Print the summary statistics for the precipitation data.

## ***Station Analysis***
The station analysis is performed using the following steps:

1- Calculate the total number of stations in the dataset.

2- Find the most-active stations (that is, the stations that have the most rows) and answer the following question:

which station id has the greatest number of observations?

3- Calculate the lowest, highest, and average temperatures that filters on the most-active station id found in the previous query.

4- Get the previous 12 months of temperature observation (TOBS) data for the most-active station and plot the results as a histogram with bins=12

## Flask API

The Flask API is designed based on the queries developed in the previous section. The available routes are:

* ***Home page*** - Lists all the available routes.

* ***/api/v1.0/precipitation*** - Retrieves the last 12 months of precipitation data and returns the JSON representation of the data.

* ***/api/v1.0/stations*** - Returns a JSON list of stations from the dataset.

* ***/api/v1.0/tobs*** - Retrieves the dates and temperature observations of the most-active station for the previous year of data and returns a JSON list of temperature observations for the previous year.

* ***/api/v1.0/<start> and /api/v1.0/<start>/<end>***- Returns a JSON list of the minimum temperature, the average temperature, and the maximum temperature for a specified start or start-end range

For a specified start, the API calculates TMIN, TAVG, and TMAX for all the dates greater than or equal to the start date

## Conclusion
In this project, we used Python and SQLAlchemy to conduct a basic climate analysis and data exploration of a climate database for Honolulu, Hawaii.

We performed precipitation and station analyses and visualized the results using Matplotlib.

We also designed a Flask API that provides routes for retrieving precipitation data, station data, and temperature observations for a specified time range.

Overall, this project provides a useful example of how to use Python and SQLAlchemy to analyze and explore a database and how to design a Flask API based on the analysis.

The project can be adapted to other databases and locations to conduct similar analyses and provide useful information for trip planning or other purposes
