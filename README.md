# World Weather Analysis

Analysis of over 500 worldwide city locations and corresponding weather data to match visitors travel criteria

## Overview of Project

The scenario for this project is to collect and present data for customer's travel preferences for a travel technology company specializing in internet-related services in the hotel and lodging industry. Over 500 random latitude and longitudes, collected from the citypy module, and their corresponding JSON weather data from the OpenWeather map API, are combined to show the relationship between cities and various weather parameters around the world.

### Purpose

The overall aim of the study is to help customers find their ideal hotel anywhere in the world based on their specific travel criteria. 

### Software

* Random latitude and longitude values were generated using the Random function
* The citypy module was used to locate the nearest city for the random lat longs

Import our dependencies and initialize counters and an empty list that will hold the weather data.
Loop through the cities list.
Group the cities in sets of 50 to log the process as we find the weather data for each city.
Two counters will be needed here: one to log the city count from 1 to 50, and another for the sets.
Build the city_url or endpoint for each city.
Log the URL and the record and set numbers.
Make an API request for each city.
Parse the JSON weather data for the following:
City, country, and date
Latitude and longitude
Maximum temperature
Humidity
Cloudiness
Wind speed
Add the data to a list in a dictionary format and then convert the list to a DataFrame.

##
