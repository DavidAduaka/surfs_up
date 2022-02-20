# Surfs_up by David Aduaka 

## Overview of the Surf's Up Challenge
In the Challenge scenario, I am looking to open a Surf and Shake Shop that would serve ice cream year-round in Hawaii. After meeting with W. Avy, an investor who wants to back my venture, he shares concerns about the effects of the weather on the viability of the business. In the Challenge, he asks me to run weather analytics on data from Oahu for June and December, in order to determine if the surf and ice cream shop business is sustainable year-round.

## Resources
Data Sources: hawaii.sqlite

Software: Anaconda 4.10.1, Pandas, json, numpy, time and sqlalchemy Libraries, PythonData kernel; Jupyter Notebook

## Results
The following table was created from the Measurements table in the hawaii.sqlite file, filtered by June and December.
![image](https://user-images.githubusercontent.com/70069730/154860005-5ce2d8d1-0dfa-4517-a6a8-1255492ef004.png)

There are several key differences in weather data between June and December are the following:

- June has approximately 200 more data points than December.
- The average temperature in June (74.9) is approximately 4 degrees higher than the average temperature in December (71.0).
- The standard deviation of December Temperatures is higher than that of June. This implies that there is greater variance and range in December temperature data.
- Both June and December data have a similar max temperature.

## Summary 
#### Additional Queries
One additional query that can be done is gather more data for December. As mentioned, June has 200 more data points than December. The current data ends in August 2017, so it excludes December 2017. This may level out any average or standard deviation discrepancies that showed up in my key differences. Data can be retrieved via an API call using OpenWeatherMap's Historical Weather Data API. and searching for Oahu.

Another additional query that can be done is analyzing precipitation. I wrote a query in a similar manner to the challenge deliverables that described precipitation data for June and December. The resulting table is shown below.

![image](https://user-images.githubusercontent.com/70069730/154860064-2689b2f2-a97f-4538-8c68-eaa06f5bc0f6.png)

I also read the Measurement data from SQL to a DataFrame and exported it to Excel. There I ran an additional query regarding the amount of days in each month that experienced precipitation. The resulting table is shown below.

![image](https://user-images.githubusercontent.com/70069730/154860083-9e74a989-01ff-4f67-a3ae-a3d7b62d8d72.png)

From these two results, one can determine that December experiences a higher average precipitation than June, and that it experiences more days of precipitation as a percentage of its total data.

#### High Level Summary

The results can be summarized as follows:

- December has fewer data points than June because the data ends in August 2017. Additional data should be collected as prescribed in the additional queries.
- The average temperature in June is 4 degrees higher than the average temperature in December. The standard deviation of December is higher than that of June, implying greater variance in temperature data.
- Precipitation can also be used as a query. There is higher average precipitation in December than in June, and the percentage of precipitation days is higher in December.
- The 4 degree lower average temperature, the higher standard deviation, and the higher precipitation totals in December can be causes for concern for investor W. Avy. Based on his previous investment history, he may be averse to supporting this venture, as the data shows the temps are lower and the rain is higher in December. It may affect the viability of selling ice cream year-round.
