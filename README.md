# python-api-challenge
Week 06 - Homework


## Python API Homework - What's the Weather Like?


### Background

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

Use Python requests, APIs, and JSON to per form the following:

### Data Sources

https://pypi.org/project/citipy/
https://openweathermap.org/api
https://developers.google.com/maps

### API Keys

Sign up for a key at the following sites and add your API keys to the "api_keys.py" file

* https://home.openweathermap.org/users/sign_up
* https://developers.google.com/maps

Note: if you having trouble displaying the maps try running jupyter nbextension enable --py gmaps in your environment and retry.


## Part I - WeatherPy

Create a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, you'll be utilizing a simple Python library, the OpenWeatherMap API, and a little common sense to create a representative model of weather across world cities.

Create a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

Run linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude


## Part II - VacationPy

Use jupyter-gmaps and the Google Places API for this part of the assignment. Note: if you having trouble displaying the maps try running jupyter nbextension enable --py gmaps in your environment and retry.

* Create a heat map that displays the humidity for every city from the part I of the homework.
* Narrow down the DataFrame to find your ideal weather condition. For example:
** A max temperature lower than 80 degrees but higher than 70.
** Wind speed less than 10 mph.
** Zero cloudiness.
** Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.
* Using Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.
* Plot the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.


###  Observation Summary

1. Temperatures decrease as the latitude increases towards the northern hemisphere, compared to the temperatures as we move down towards southern hemisphere.

2. Humidity is higher in cities with higher temperatures than in cities with lower temperatures.

3. Looking at all of the trends, we can see that latitude has a direct impact on temperatures, but not so much on humidity, cloudiness, or windspeed. These three variables (humidity, cloudiness, and windspeed) are more specifically related to temperatures, therefore plotting these three variables against temperatures rather than Latitude would yield more conclusive results.