# **World_Weather_Analysis**

## Overview of Project

### Summary ### 
The objective of this project is to utilize newly learned statistical skills and retrieve specific information from websites using the application programming interface (API) from 2000 locations around the world.  The goals are to:
* Retrieve Weather Data
* Create a Customer Travel Destination Map
* Create a Travel Itinerary Map

### Data Sources
The data sources to complete this project are outlined below:
* Open Weather: https://openweathermap.org/api
* Google Maps Platform: https://cloud.google.com/maps-platform/
The statistical analysis was performed using the following Python Library:
* Citipy

### Software Used
Python 3.9.12, Pandas Library, Matplotlib, Jupyter Notebook, APIs


## Results 

### Retrieve Weather Data 

Using the randomization numpy tool to generate a set of latitudes and longitudes yielded 2,000 locations around the world.  Those locations were analyzed with the “citipy” Library to obtain a list of cities based on the proximity to those locations.
After analyzing and cleaning up the data, a total of 713 unique cities were identified and added to a Pandas DataFrame for further analysis.  Using the Open Weather API, specific weather elements for each of those cities were obtained. This information would then be used by the customer to help narrow down vacation plans based on user-specified temperature parameters.
The ensuing data was placed in a new DataFrame which was exported into a CSV file for further processing and analysis with the Google Map API.
![image](https://user-images.githubusercontent.com/86136535/128609492-06a86969-d119-4901-839f-f341d2d8fb6a.png)


| **Table 1.** Unique Cities |
| :---: |
| ![Table](https://github.com/mrmarken/World_Weather_Analysis/blob/main/Weather_Database/cities_df.png) |

 
### Customer Travel Map 
Using the input function, a customer was asked to input their preferred temperature range which was then used to provide a list of cities meeting those criteria.  These potential travel destinations were further analyzed to provide customers with hotel options.
When a user submitted the range of 70 - 85 deg F, a list of 313 possible travel destinations were identified.  Using the Google Map API, a list of hotels within a 5km radius of each city was produced.  Only those cities that had a hotel within that radius yielded a new DataFrame with 303 possible destinations.
Next, we used a marker layer map with pop-up markers to provide further city details for the end-user.

|  |
| :---: |
| ![Figure1](https://github.com/mrmarken/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png) |
| **Figure 1.** Map with Custom Pop-up Markers |


### Travel Itinerary Map

Using the Google Directions API, a travel route was created to display the optimal driving route for a set of four cities selected in part of western Europe: Narbonne and Fontaine in France, and Lerici and Codigoro in Italy.  A map was provided to the customer:

|  |
| :---: |
| ![Figure2](https://github.com/mrmarken/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map.png) |
| **Figure 2.** Travel Map |

Lastly, a marker layer map with pop-up was provided to highlight the customized information for the user.  The pop-up describes the name of the city, country, suggested hotel and current weather description.

|  |
| :---: |
| ![Figure3](https://github.com/mrmarken/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map_markers.png) |
| **Figure 3.** Map with Custom Pop-up Markers |



  


