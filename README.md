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
