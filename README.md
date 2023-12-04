# Module 6 Challenge - Python API

The goal of this project is to determine changes in weather characteristics based on proximity to the equator.  This anaysis is in the [WeatherPy](WeatherPy/WeatherPy.ipynb) file located in this repository's WeatherPy folder.  

Weather knowledge was then used to help determine key vacation cities based on weather parameters.  Geoapify Places was used to determine hotel options in these prime weather locations.  This analysis is in the [VacationPy](WeatherPy/VacationPy.ipynb) file located in this repository's WeatherPy folder.

## WeatherPy
A collection of over 500 random cities were obtained by utilizing Numpy random number generator to generate Latitude and Longitude coordinates.  CitiPy was then utilized to determine the nearest city to those generated coordinates.  

OpenWeather API was used to determine the following:
  1. Latitude and Longitude of the City
  2. Maximum Temperature (C)
  3. Cloudiness
  4. Wind Speed
  5. Country
  6. Date of Data Aquisition

The resulting DataFrame was exported as [cities.csv](WeatherPy/output_data/cities.csv) in the output_data folder.

Scatter plots were constructed and saved in the output_data folder:
  1. [Fig1](WeatherPy/output_data/Fig1.png) = Maximum Temperature vs. Latitude
  2. [Fig2](WeatherPy/output_data/Fig2.png) = Humidity vs. Latitude
  3. [Fig3](WeatherPy/output_data/Fig3.png) = Cloudiness vs Latitude
  4. [Fig4](WeatherPy/output_data/Fig4.png) = Wind Speed vs Latitude

Linear Regression was calculated and modelled for Northern and Southern Hemisphere cities separately, for the following parameters:
  1. Maximum Temperature vs. Latitude
  2. Humidity vs. Latitude
  3. Cloudiness vs Latitude
  4. Wind Speed vs Latitude

## VacationPy
The previously created cities.csv file was imported for this analysis.

First, a map plot of all cities in the DataFrame was constructed with markers size based on humidity values.

Ideal weather conditions were defined, and the city_data_df DataFrame was reduced to only include cities that met those parameters.  Using this newly filtered DataFrame, Geoapify Places was utilized to find the closest hotel within 10km.  A map plot was created to visualize the Ideal Weather Cities and their closest hotel option.

