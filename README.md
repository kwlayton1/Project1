# Project1

Primary Animal Data Source:
Wildlife Insights Wasatch data 2018-2020

Does urbanization affect wildlife in the wasatch?

We created a bar chart of each animal observed in total/overall thoughout all 3 years. From there, it was split by wild versus urban data. Along with wild versus urban, we created a bar chart by year and urban/wild by year. Only 7 animals were observed during all 3 years to some degree in an urban and wild setting. With these 7 animals, t-tests were applied to each to determine if there was any significant difference between the frequency of observations in a wild versus an urban location. From these tests, Elk and Moose were the animals with a significant difference, tested at 90% confidence, being observed more frequently in a wild location than an urban one. From here, we located the 5 camera sites these animals were captured the most and recorded them, as they would be good locations to study further as possible wildlife protection areas. (Powerpoint pages 4-5) (Urban_Wild_BarCharts_Analysis.ipynb)

Wildlife Dataset (Full dataset) was merged with Weather dataset (left join method). A csv file was created from the merge. 
We narrowed down the station data to 3 stations (they had the most observations of animals/humans. The 3 maps show where the stations are located. 2 in Little Cottonwood and 1 in Emigration Canyon. 
Human vs Wildlife Correlation? The following stacked bar charts show the number of Humans (Bicycles) and the wild animals that were captured on each day (2019 data was used). Also a 2 sample t-test was used per station (using data sets with yes or no humans present). The p values on these 2 charts are > .05  (both .56). Per these results > humans do affect wildlife
This station had opposite result with p value 0.016, less than .05 shows humans do not affect wildlife.  (Powerpoint pages 6-8) (Wildlife_Data_Analysis_KL.ipynb)

One of the questions that we had with this wildlife data was how does weather impact the behavoir of animals and can we draw any conclusions based on that. In order to answer this question we first had to pull in historical weather data for each of our data points. We decided to look at the mean temperature and the total rain accumulation for each day and compared that to the sum of each animal type seen in that day. Since both of these data points are continous, we were able to genereate scatter plots for every unique animal and do a linear regression for each one. Outlined below are some of the main observations from these plots:
Mean Temperature:
    Overall, a linear regression probably isn't the best statistical analysis to perfrom on these data sets since some of them behave non linearly. It would be interesting to try and fit different trendlines to these plots in the future.
    - Mule deer had the highest R2 correlation to temperature with more deer occurances seen the higher the temperature is for the day
    - Humans had low occurances seen below 40 degrees F, but then above 40 degrees F the occurances of humans gets much higher. This makes sense due to humans not living in the wild and being able to pick days to go hiking when it is warm out.
    - Moose were interesting because that had a perfectly flat trendline in relation to temperature. This shows that moose don't really care about the temperature and are equally active whether it is hot or cold.
    - Raccoons were also interesting becuase the showed a negative correlation to temperature. This would make since if racoons are more nocturnal animals and generally avoid sunshine and heat.
    - Black bears only had 1 obervation on a day colder than 55 degress F and all other observations are seen above 55 degrees. This makes since if black bears are hibernating during the cold month and hence are only seen during warm days
Total Rain Accumulation:
    A lot of animals did not show a strong correlation with rain fall. This could be due to Utah not getting a lot of rain in general so we don't have a lot of data to look at. Also, animals generally don't change their habits due to rain. That being said, their were a few interesting data points to look at.
    - On days with high rain accumulation, there are much less humans seen. Just like with temeparute, this makes since due to humans generally avoiding rainy days for hiking.
    - Muskrats have one of the highest R2 correlation with rain and it appears to show that on rainy days their are more muskrats seen. This makes since because muskrats are semi aquatic rodents and so would prefer wetter weather.
    - Uinta ground squirrels also showed a high correlation with rain and were more active on rainy days.
    - Both Red Fox and Eastern Fox Squirrels both had a negative correlation with rain and seem to prefer drier days.(Powerpoint pagesa 11-12)(Temp_Rain_Analysis.ipynb)

Do Animal groups prefer specific weather types?
In this case we split the animals into their Orders and summarized the count of observations by weather type. Sunny, Cloudy, Rainy and Snowy. 
As worked progressed however, we found that with the T-Tests, Null hypothesis and P-Value reviews the data was not sound enough to continue as it was originally defined.  (Powerpoint page 13)(Animal_Order_Weather_Conditions_part1.ipynb)
This work was modified and regrouped on animal species instead and we extended the weather conditions from 4 groupings to 12.
Which Animals prefer specific weather types?
With this new data set there were several key conclusions that could be observed. First, all animals saw a decrease in observations and weather conditions worsened from Sunny to Snow. Second, Muskrats, in a similar observation with Charlie's data saw and increase in observations and had the lowest R2 rating when weather conditions worsen. Finally, Moose had the highest observations of any group when the weather conditions were noted and snowy.(Powerpoint page 14)(Animal_Weather_Conditions.ipynb)

