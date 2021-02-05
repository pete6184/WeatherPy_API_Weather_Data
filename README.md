## Work left to do
- Humidity Kernel
- For Part I, you must include a written description of three observable trends based on the data.
- For Part II, you must include a screenshot of the heatmap you create and include it in your submission.
- Finish README file


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

* Humidity (%) vs. Latitude
![graph2](output_data/Fig2.png)

* Cloudiness (%) vs. Latitude
![graph3](output_data/Fig3.png)

* Wind Speed (mph) vs. Latitude
![graph4](output_data/Fig4.png)



After each plot I added an explaination as to what the code is doing as I analyzed the results.




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

After each pair of plots, I added an explain as to what the linear regression is modeling.


### Part II - VacationPy

Now I used my skills in working with weather data to plan future vacations.

To complete this part of the assignment, I did the following:

* Created a heat map that displays the humidity for every city from Part I.
![heatmap](Images/heatmap.png)

* Chose criteria to narrow down the DataFrame to find my ideal weather condition.

  * A max temperature lower than 85 degrees but higher than 70.

  * Humidity between 30-50%

  * Less than 20% chance of cloudiness.
  
 * Plotted the hotels over the previously created humidity heatmap
 ![hotelmap](Images/hotel_map.png)
