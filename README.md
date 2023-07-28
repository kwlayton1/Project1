# Project1


Weather API information 
Using https://www.latlong.net/ I was able to retrieve the proper Lat/Long info to match up our weather data points. 
Using https://api.weather.gov/points/40.593,-111.624 we know that the proper grid for the API data pull is 
        "gridX": 109,
        "gridY": 167,

We should be able to use this info with:
https://api.weather.gov/gridpoints/{office}/{grid X},{grid Y}/forecast
For example: https://api.weather.gov/gridpoints/TOP/31,80/forecast

To pull weather API data using 
https://api.weather.gov/openapi.json.

Time of data API info
https://sunrise-sunset.org/api

Plots to create:
1. Bar chart by each animal species and the count for the total data set
2. When is the best time of day to see a particular animal? (plot animal count by time of day)
3. XY scatter plot of animal count vs human count
4. Create a map with animal count by each station (geo api map)
5. XY scatter plot of animal count vs all of our continuous weather metrics
6. Day time vs night time
