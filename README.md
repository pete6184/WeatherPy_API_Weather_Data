# Python API Homework - What's the Weather Like?

## Background

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what we've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

Now, we know what you may be thinking: _"Duh. It gets hotter..."_

But, if pressed, how would you **prove** it?

![Equator](Images/equatorsign.png)


## Part I - WeatherPy

In this example, I creating a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator.

The first requirement was to create a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
![graph](output_data/Fig1.png)
Analysis of Latitude vs. Max Temp Plot
- This graph shows the relationship between a city's latitude and their max temperature.
- The result shows what we all know and expect in that cities in the southern hemisphere and cities (both hemispheres) that are close to the equator have higher max temperatures than cities farther north of the equator.


* Humidity (%) vs. Latitude
![graph2](output_data/Fig2.png)
Analysis of Latitude vs. Humidity Plot
- This graph shows the relationship between a city's latitude and their humidity levels.
- The analysis of this graph does not give us a great definitive correlation between a city's latitude and their humidity levels.
- When I ran this last data set, there was a small cluster of cities between 40-70 degrees latitude that had lower humidity rates, however this was not the case in some of my previous data sets.


* Cloudiness (%) vs. Latitude
![graph3](output_data/Fig3.png)
Analysis of Latitude vs. Cloudiness
- This graph shows the relationship between a city's latitude and their percentage of cloudy days.
- The results of this graph do not show any correlation between a city's latitude and how many cloudy days they have.


* Wind Speed (mph) vs. Latitude
![graph4](output_data/Fig4.png)
Analysis of Latitude vs. Wind Speed Plot
- This graph shows the relationship between a city's latitude and wind speeds.
- Looking at the graph, there does not seem to be a relationship between the city's latitude and wind speed.



The second requirement was to run linear regression on each relationship. This time, I separated the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
![graph5](output_data/LinRegress1.png)

* Southern Hemisphere - Temperature (F) vs. Latitude
![graph6](output_data/LinRegress2.png)

* Northern Hemisphere - Humidity (%) vs. Latitude
![graph7](output_data/LinRegress3.png)

* Southern Hemisphere - Humidity (%) vs. Latitude
![graph8](output_data/LinRegress4.png)

* Northern Hemisphere - Cloudiness (%) vs. Latitude
![graph9](output_data/LinRegress5.png)

* Southern Hemisphere - Cloudiness (%) vs. Latitude
![graph10](output_data/LinRegress6.png)

* Northern Hemisphere - Wind Speed (mph) vs. Latitude
![graph11](output_data/LinRegress7.png)

* Southern Hemisphere - Wind Speed (mph) vs. Latitude
![graph12](output_data/LinRegress8.png)



### Part II - VacationPy

Now I used my skills in working with weather data to plan future vacations.

To complete this part of the assignment, I did the following:

* Created a heat map that displays the humidity for every city from Part I.
![heatmap](Images/heatmap.png)

* Chose criteria to narrow down the DataFrame to find my ideal weather condition. My conditions included:

  * A max temperature lower than 85 degrees but higher than 70.
  * Humidity between 30-50%
  * Less than 20% chance of cloudiness.
  
 * Lastly I plotted the hotels over the previously created humidity heatmap
 ![hotelmap](Images/hotel_map.png)
