## Alpha Testing: Riding Conditions Short Term Forecasts in Boulder/Denver Region

### Find the tool at: http://ridecast.s3-website-us-east-1.amazonaws.com/html_map.html

This is part of a project I am doing for my masters. This is a tool for cyclists in the Boulder/Denver area to assess riding weather conditions before they go out riding. 

**How it works:**
**Eventually** users will be able to have a "profile" where they get to set:

 - Ideal Temperature
 - Lowest Ridable Temperature
 - Highest Ridable Temperature
 - Highest Ridable Wind Speeds
 - Highest Ridable Wind Gusts
 - If they are willing to ride in Light, Moderate or Heavy Precipitation
 - The greatest chance of thunderstorms they would ride in
 - If they are willing to ride on any snow depth or ice

For **now** I have the following set conditions that are "unrideable":

- Ideal Temp of 70F
- Lowest Temp of 35F
- Maximum Temp of 100F
- Highest Ridable Wind 35mph
- Highest Ridable Gust 45mph
- Any precipitation 
- Over a 60% Chance of Thunderstorm
- Any snow depth 

My resulting map will range in color from light green (close to ideal riding conditions) to red (ridable but poor). **There is an abrupt change from red to purple. Purple is conditions that are unrideable** (one of my thresholds are exceeded). 

Users can adjust the image transparency and select different times.

 **FAQ:**
 How often does the forecast update?
 The forecast updates once an hour during daytime hours and early morning 4am-8pm
 
 How far out does the forecast go?
 The current forecast goes out about 30-34 hours. I will eventually get around to making a better "live conditions map" and an extended forecast. 
 

**Apps that Already Exist:**

There are already some apps out there that allow you to upload route files and get a specific forecast along the route once you enter the start time. There are 3 issues with this app:
1. The weather data quality: I did some digging on the data source they use for this app and it's the same data that is displayed on the apple weather app. It's custom model by Dark Sky. So if you hate what your apple weather forecast because it's always wrong it will be just as wrong with this app. That model was not developed by meteorologist it was developed by ML engineers who only focus on basic metrics for accuracy. These apps always fail when the weather is out of the norm. 
2. You need to have route files on hand: Most of the time, especially for shorter rides I don't have a route file of exactly where I am going. If I am just heading to my local climb to do intervals I don't need a route file for that. 
3. The app uses your average speed estimation to estimate your location at a given time. If your average speed is 18mph and the first hour of the ride is a climb you won't be averaging 18mph on that. Therefore your "location estimation" will be wrong. 

**Why is this better?**
1. Weather Data Quality: My app uses the NBM by NOAA. This is a blend of many high and low resolution models from (mostly) NOAA. This is the model of choice for most NWS short term forecasts. To put it simply this "model" was designed BY Meteorologists. This model is the best one they have for all around weather forecasts. This model has both deterministic and probabilistic forecast outputs. 
2. You don't need to upload  route file to use the app. If you're just looking to ride you won't need to make a bunch of routes and then upload a bunch of files to "compare and contrast" the forecasts. That's way overcomplicated for an afternoon 2hr endurance ride. This app, for now, is designed to show you where you can ride and how ideal or not ideal conditions will be. 


### Warnings to Users:
The pop up with specific values may not update as quickly as the map. Check the "Valid Time" at the top of the pop up as that time will be the valid time of the weather data below. The image WILL always be correct with the time you selected. It can take a few seconds to load the image and even longer for pop up data to display on the screen if you are selecting different times rapidly. If nothing is rendering try to refresh the page. **The site requires decent wifi/cell service to render**. I will be working to improve this. Remember this app uses FORECASTS. Forecasts will always be wrong to some degree. **This product is still in VERY early testing and I know it's not a super pretty interface!** Please report bugs/feature requests to keabbot@gmail.com


## Use case Example:

I have a 2 hour session with some intervals (6x2min). I want to ride my local climb this afternoon at around 3pm. My local climb is about 12 miles away at Lookout Mountain. The weather in Denver is OK but what will conditions be on the mountain? Super cold? Is there snow? How windy?

When I zoom into lookout mountain I can see that the top half of the mountain is in purple, so I won't ride all the way up. The bottom part of the climb is in orange so I can expect poor riding conditions. If I tap/click on a location on the map a pop up will pull up specific values. Based on this I will dress for 30's and breezy conditions. 

![enter image description here](https://imgur.com/JD07LED.png)


All of this took only a few clicks and seconds of my time!



## Future Work:
Eventually I want to make this a one stop shop application for any kind of riding conditions you could ever need. Future work will be around making a highly detailed current map that takes in a bunch of weather sensors to provide the best estimate of current conditions in the area. There will also be simple riding outlooks for the more distant future (2-7 days). I will also develop route-specific forecasts. **Please provide feedback and feature requests! to keabbot@gmail.com**