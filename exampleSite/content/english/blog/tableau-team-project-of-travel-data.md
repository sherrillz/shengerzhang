+++
author = "Shenger Zhang"
date = 2021-12-07T05:00:00Z
description = ""
image = "/images/big_data_visualization_shutterstock_arthead.png"
image_webp = "/images/big_data_visualization_shutterstock_arthead-copy.webp"
title = "Tableau: Team project of travel data"

+++
This is a school project. All the questions refer to the assignment documents.

A.

![](/images/blog/730data model/teamass1/ta101.png)

The histogram was created placing the Trip Duration variable in the row and the Count of trip duration variable in the column. The bins were adjusted to 120 by right-clicking the Trip Duration variable and selecting the edit function in the tableau. Based on the histogram shape, the distribution is significantly right-skewed (highly positive skewed) showing that more trips were of shorter duration than longer. This means that the maximum trip duration was between 400-500 seconds (tallest bin with 17,602 )while the shortest trip duration was between 2700-2800 seconds (shortest bin).

B.

![](/images/blog/730data model/teamass1/ta102.png)

\-From the above map, we can observe that the stations with a higher number of trips taken have a larger bubble. Trips with a greater average trip duration are colored red while trips with lower duration diverge from light green to a dark green color scale. We can observe that the majority of trips are of shorter duration across regions (as depicted by light and dark green colors ). There is one area located in the west of the San Francisco region and one on the southeast side that notably has trips with a higher trip duration than others. One such area is also visible in the west part of the east bay region.

Stations with a higher number of trips are concentrated in the San Francisco region followed by the east bay region. San Jose sees the least amount of trips per station.

C.

![](/images/blog/730data model/teamass1/ta303.png)

D.

![](/images/blog/730data model/teamass1/ta105.png)

The visualization was created by placing the group’s San Francisco, East Bay, and South Bay in the rows. Count of Ride ID and Count of Start Station Name were calculated in columns.

\- Total number of trips (Ride ID Count)

From the left chart above, the highest number of trips were taken in San Francisco County with 120856 trips as well as the most start stations of 256 compared to the other regions like east bay and south bay.

\- Number of stations (Start Station Name Count)

San Francisco has the largest number of stations (256), followed by East Bay (120) and lastly South Bay (81)

E.

![](/images/blog/730data model/teamass1/ta106.png)

The visualization was created by placing the groups (south, east, and San Francisco in the rows, and summary stats like average and Standard deviation were calculated for the Trip Duration placing them in columns to get the horizontal bar graph.

From the above comparison, we don’t see any significant difference in the average and Standard deviation of trip duration across the three regions.

\- Average Trip Duration

The average trip duration of San Francisco, East Bay, and South Bay are 729.6, 792.8, and 649.8 separately.

\- Trip Duration Standard Deviation

The STDEV trip duration of San Francisco, East Bay, and South Bay are 493.2, 553.0, and 544.5 separately.

Note that despite San Francisco has a higher number of stations and number of trips, however, East Bay region has a higher average trip duration and standard deviation than San Francisco. A reason is a potential that East Bay commuters need to travel longer distances than commuters from San Francisco.

F.

![](/images/blog/730data model/teamass1/ta107.png)

From the above map, we observe that stations that have a higher number of trips have larger bubbles and average trips are color-coded in the graph (longer trips in blue and shorter trips in red). The station with maximum trips was Powell ST BART Station. The station with the longest average trip duration is 30 th St at San Jose Ave

**Question 2**

a.

![](/images/blog/730data model/teamass1/ta108.png)

The visualization was created following the below-mentioned steps :-

A) Geographical Role - We started our analysis by creating the appropriate geographical roles by generating latitude and longitude with respect to location variables in the data.

B) We created the map using the latitude generated and longitude generated. Longitude variable needed to be assigned a geographic role.

C) We colored the map using total cases confirmed. (Higher number of cases in red and lower cases in green)

D) We made sure that the date is filtered up to 7/26/2021 to capture the cumulative aspect as of that date.

E) Lastly, we used the color aspect to visually highlight the extremities of the covid cases (highest cases by RED, lower cases by GREEN).

b.

![](/images/blog/730data model/teamass1/ta109.png)

The visualization was created following the below-mentioned steps:-

1. We first created a Date filter between 2/24/2020 to 6/24/2021.
2. We created the time series chart with DAY in the column and Total Case in the rows.
3. Then we filtered the TOP 10 countries and excluded the continents and WORLD variables from the data.
4. We Used color with respect to locations to highlight the Top ten countries in the time series chart.