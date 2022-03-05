# Analysis of Theater Kickstarter Campaign Outcomes 

## Introduction 

We begin this analysis by looking at raw data for Kickstarter campaigns aimed at funding entertainment media and entertainment media-related projects. This data provides us specific campaign details such as goals and results along with a few descriptive factors. 

Specifically, this analysis takes a deeper look at Kickstarter campaigns in the field of theater. We attempt to zero in on some key factors to gain insight on what exactly drives a successful campaign. By identifying trends from past campaigns, we're able to make suggestions to future campaigns on what factors to consider when launching. 

## Analysis 

The first factor we analyzed was the launch date of campaigns across several years of data, specifically what month of the year they were launched. While this parameter is straightforward, obtaining the results was not necessarily so. While the raw data did contain launch dates for all campaigns, these were formatted as Unix timecodes and not the traditional short date format necessary for our analysis. Converting these to a standard date format required first understanding what a Unix time code represents. Our research revealed that the string of numbers that make up a Unix timecode represent the amount of seconds elapsed since January 1, 1970. With this in mind, we were able to convert each value with a simple formula that could quickly be applied to the entire data set. Each value was first divided by 60, to obtain the figure in minutes, then again by 60 to obtain hours, and finally divided once again by 24 to obtain the Unix value in days. The number of days was then added to the date 1/1/1970 to arrive at the launch date of each campaign. The formula was entered as shown below: 

