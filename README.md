# Weather and Vacation Analysis: Python-API-Challenge

## Overview
This project utilizes Python scripting to analyze weather data for over 500 cities at varying distances from the equator, leveraging the OpenWeatherMap API and the `citipy` library. The analysis aims to explore the relationship between weather variables and latitude. Additionally, the project uses the Geoapify API and the `geoviews` Python library to plan hypothetical vacations based on ideal weather conditions.

## Part 1: WeatherPy

### Objective
To visualize and analyze how weather changes as we approach the equator.

### Methodology
1. **Data Collection**: Generate random geographic coordinates and use `citipy` to find the nearest city for each coordinate set. Retrieve weather data for these cities using the OpenWeatherMap API.

2. **Data Visualization**: Create scatter plots to showcase relationships between latitude and key weather variables:
   - Latitude vs. Temperature
   - Latitude vs. Humidity
   - Latitude vs. Cloudiness
   - Latitude vs. Wind Speed

3. **Linear Regression Analysis**: 
   - Perform linear regression on each relationship.
   - Separate the data into Northern Hemisphere (latitude >= 0) and Southern Hemisphere (latitude < 0).
   - Create scatter plots with regression lines for each hemisphere and weather variable.

## Part 2: VacationPy

### Objective
To use weather data to identify potential vacation destinations and nearby hotels.

### Methodology
1. **Ideal Weather Condition**: Narrow down the cities to those with ideal weather conditions:
   - Max temperature between 21°C and 27°C.
   - Wind speed less than 4.5 m/s.
   - Zero cloudiness.

2. **Hotel Search**: Use the Geoapify API to find the first hotel within 10,000 meters of each city's coordinates.

3. **Mapping**: 
   - Create a map visualization with a point for every city. Point size represents humidity.
   - Filter down based on ideal conditions and add hotel names and country information in hover tooltips for each city on a second map.

## Repository Guide
This repository contains the following key files and folders:

1. **WeatherPy.ipynb**
   - A Jupyter Notebook containing the analysis for Part 1 of the project. 
   - It includes the generation of city list, retrieval of weather data using OpenWeatherMap API, and creation of scatter plots with linear regression.

2. **VacationPy.ipynb** 
   - A Jupyter Notebook for Part 2 of the project. 
   - It focuses on using the weather data to identify potential vacation destinations, finding hotels using Geoapify API, and mapping the results with `geoviews`.

3. **output_data** (folder) 
   - Contains output data and visualizations generated from the WeatherPy analysis.
   - Includes:
     - Exported scatter plots with linear regression analysis.
     - A CSV file of the generated city data used in both Part 1 and Part 2 of the project.



