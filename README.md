# **INTRO**

The purpose of this project is to explore and compare the spatial distribution of bike trips and identify key factors influencing bikeshare activity.
1. **How does the spatial activity of Divvy bikeshare users differ between customers and subscribers?**
   - Are there significant patterns in the trip origins for one-time customers compared to regular subscribers? Do customers tend to cluster in specific areas, and how do these patterns compare with those of subscribers?

2. **What are the differences in the spatial distribution of bike trips between male and female users?**
   - Are there any spatial trends or significant differences in activity between male and female riders?

3. **How does bikeshare usage vary between weekdays and weekends?**
   - Is there a noticeable shift in trip patterns during the weekends compared to weekdays? Are certain areas of the city used more frequently on weekends, indicating leisure activity, while weekdays show patterns of commuting or regular use?

4. **What are the implications of these spatial patterns for infrastructure and marketing strategies?**
   - Where should the marketing team focus their efforts, considering the most densely clustered areas?
  
# **DATA**

This project uses DIVVY Chicago Bike Share trips data (https://divvybikes.com/system-data). It includes precise timestamps for when trips began and ended. Dataset provides information on the geographic locations of trip origins and destinations, recorded as latitude and longitude coordinates, as well as station-specific metadata such as station IDs and names.  Demographic data is also included, specifying user type (subscriber or casual customer) and gender. Weather data, including temperature and information on weather events like rain or snow, is linked to trips. Station dock capacities at both the starting and ending points of trips are also provided.


# **DATA PREPROCESSING:**
1. Datetime conversion
2. Missing value detection
3. Duplicate record identification
4. Trip duration calculation and outlier detection using IQR method
5. Coordinate validation within Chicago's boundaries
6. Visualization of trip duration distribution
7. Data cleaning by removing outliers and invalid records

# **EDA:**
1. Temporal patterns:
- hourly distribution shows peak usage times
-daily patterns reveal weekday vs weekend differences
-seasonal analysis captures weather and daylight impacts

2.User demographics (helps in targeted marketing and service improvements):
  - user type distribution (Subscribers vs Customers)
  - gender distribution to understand user base composition

3.Trip duration analysis:
 - statistical measures by user type
 - distribution visualization through box plots
 - identifies typical trip lengths and variations

4.Station analysis (helps in capacity planning):
- identifies most popular start/end points
- reveals high-demand areas

5.Weather impact (for operational planning):
- temperature effects on ridership
- weather event impacts

6.Spatial patterns (for system expansion planning):
- heatmap visualization of trip concentrations
- identifies high-activity areas

7.Correlation analysis for predictive modeling):
- relationships between numeric variables


# **KDE**

In this case, the data points (such as spatial locations) themselves act as a "proxy" for a random variable representing the frequency or intensity of occurrences in a given space. Each point represents an "event," and KDE estimates the density of these events across a continuous surface. I have already plotted a simpler follium heatmap, but lets look at the smoother kernel distribution


# **LISA**
This uses trip_duration_minutes as the analyzed attribute for spatial autocorrelation.


# **NET GAIN/LOSS STATION ANALYSIS**

The graph visualizes net change trends of Divvy bike stations throughout the day, categorizing stations into three distinct groups: Net Gain, Net Loss, and Net 0 stations.


# **CONCLUSION**

Project ends with a cluster analysis and a storytelling line.

Analysis reveals that weekday bike usage is primarily driven by commuters, whereas weekend usage is dominated by tourists or occasional riders.

We also observed that bike movement between stations is not evenly distributed, leading to imbalances where some stations accumulate more bikes than others. While this was expected, the critical insight lies in understanding where the bikes are going. Downtown stations experience significant bike losses, while stations near popular destinations consistently gain bikes. Additionally, there is another significant group of users who take bikes from downtown stations in the afternoon. These are likely one-way commuters or riders heading to leisure destinations for activities after work.
