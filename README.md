# World Weather Analysis

Analysis of over 700 worldwide city locations and corresponding weather data to match visitors travel criteria

## Overview of Project

The scenario for this project is to collect and present data for customer's travel preferences for a travel technology company specializing in internet-related services in the hotel and lodging industry. Over 500 random latitude and longitudes, collected from the citypy module, and their corresponding JSON weather data from the OpenWeather map API, are combined to show the relationship between cities and various weather parameters around the world.

### Purpose

The overall aim of the study is to help customers find their ideal hotel anywhere in the world based on their specific travel criteria. Customers should be able to search for hotels tied to specific cities that are based on current weather and their chosen temperature range, identify travel destinations and form a travel itinerary using the analysis. 

### Software and Resources

* Tools and data sources used in this project: citipy, OpenWeatherMap API, Google Maps API (Maps, Places, Directions)
* Software used: Python 3.7.9, Jupyter Notebook 6.1.4, Anaconda 1.10.0

## Retrieving City Destination and Weather Data to Build Database

The analysis used to build the weather database can be found [here](https://github.com/jkenning/World_Weather_Analysis/blob/main/Weather_Database/Weather_Database.ipynb). 

- First, a set of 2000 random latitude and longitudes were created using numpy and added to a list. 
- Then using citypy, the nearest cities to those co-ordinates were identified, resulting in 774 locations (positioned on land). 
- Using an API call on OpenWeatherMap, a request for weather data was run for each city, parsing the JSON and retrieving data.
- The scraped data was converted into a dataframe and exported as [WeatherPy_Database.csv](https://github.com/jkenning/World_Weather_Analysis/blob/main/Weather_Database/WeatherPy_Database.csv).

![](https://github.com/jkenning/World_Weather_Analysis/blob/main/Weather_Database/Weather_database_dataframe.png)

Figure 1. Example of retrieved weather data

## Customer Travel Destinations

Using an input range for user's temperature preferences on the WeatherPy data, requests to Google's Maps and Places API was able to search for hotels within 5000 m of the city co-ordinates. A marker layer was then created for each city location on the map, with hotel and current weather information (see [Vacation_Search.ipynb](https://github.com/jkenning/World_Weather_Analysis/blob/main/Vacation_Search/Vacation_Search.ipynb)).

![](https://github.com/jkenning/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png)

Figure 2. Map showing worldwide destinations with travel information

## Travel Itinerary Map

Google Map's Directions API was used to generate a possible travel itinerary. As an example, the app was able to generate a travel route between four cities in the south-eastern United States that could represent a customer's travel itinerary for the region (see [Vacation_Itinerary.ipynb](https://github.com/jkenning/World_Weather_Analysis/blob/main/Vacation_Itinerary/Vacation_Itinerary.ipynb)).

![](https://github.com/jkenning/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map.png)

Figure 3. Map showing the travel route from the example itinerary

![](https://github.com/jkenning/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map_markers.png)

Figure 4. Map showing the travel itinerary locations with markers

