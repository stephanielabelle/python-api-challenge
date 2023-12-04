# Module 6 Challenge - Python API

The goal of this project is to determine changes in weather characteristics based on proximity to the equator.  This anaysis is in the [WeatherPy](WeatherPy\WeaterPy.ipynb) file located in this repository's WeatherPy folder.  

Weather knowledge was then used to help determine key vacation cities based on weather parameters.  Geoapify Places was used to determine hotel options in these prime weather locations.  This analysis is in the [VacationPy](WeatherPy\VacationPy.ipynb) file located in this repository's WeatherPy folder.

## WeatherPy
A collection of over 500 random cities were obtained by utilizing Numpy random number generator to generate Latitude and Longitude coordinates.  CitiPy was then utilized to determine the nearest city to those generated coordinates.  

OpenWeather API was used to determine the following:
  1. Latitude and Longitude of the City
  2. Maximum Temperature (C)
  3. Cloudiness
  4. Wind Speed
  5. Country
  6. Date of Data Aquisition

The resulting DataFrame was exported as [cities.csv](WeatherPy\output_data\cities.csv) in the output_data folder.

Scatter plots were constructed and saved in the output_data folder:
  1. [Fig1](
