# Python-API-Challenge
In this example, I created a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, I utilized a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and a little common sense to create a representative model of weather across world cities.

First objective is to create a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude


Second objective is to run linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

These are how relationships look like on a graph:

![graph1](Images_of_Graphs/Cloudiness_vs_Latitude.png)

* This graph shows that there is no direct relatipnship between cloudiness and latitude.

![graph2](Images_of_Graphs/Humidity_vs_Latitude.png)

* From this graph, one can tell that humidity increases when latitude ranges from 60.

![graph3](Images_of_Graphs/Temperature_vs_Latitude.png)

* We have quadratic linearship between temperature and latitude. Maximum temperature can be observable when latitude is around 20. 

![graph4](Images_of_Graphs/WindSpeed_vs_Latitude.png)

* One can see that there is no direct correlation between windspeed and latitude.

After each pair of plots explain what the linear regression is modeling such as any relationships you notice and any other analysis you may have.

Final notebook includes:

* Randomly select **at least** 500 unique (non-repeat) cities based on latitude and longitude.
* Perform a weather check on each of the cities using a series of successive API calls.
* Include a print log of each city as it's being processed with the city number and city name.
* Save a CSV of all retrieved data and a PNG image for each scatter plot.

### Part II - VacationPy

Using part 1, weather analysis, now I wanted to plan vacation spots with ideal weather. Used jupyter-gmaps and the Google Places API for this part of the assignment.

To accomplish this objective, I did the following steps:

* Create a heat map that displays the humidity for every city from the part I of the homework.

* Narrow down the DataFrame to find your ideal weather condition. For example:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Drop any rows that don't contain all three conditions. I wanted to be sure the weather is ideal.

Heres' how map with cities that have ideal weather :
![graph5](Images_of_Graphs/Map_of_Final_Hotel_List.png)

* One can tell from the map that the top 5 cities with ideal weather are located close to equator.