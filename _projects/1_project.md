---
layout: post
title: Fitbit Data's Exploratory Analysis
description: Analyse Fitbit data from Fitbit API.
---
You Can see the code i used [here](https://github.com/shubhamtiwari10/fitbit-analysis){:target="_blank"} on github.

Using Fitbit API to perform exploratory analysis on its data.
============

I have tried to analyse my FitBit data to see how my sleep affects my activity level and to check wether or not i have built up sleep deficit.

Note: In order to get my Fitbit data, I first had to set up a Fitbit API. Then, I ran a separate script.

Question 1: Does the amount of sleep I get the night before be used to predict or correlate my activity level for the next day ?
------------

Notice that the distribution appears to be bimodal. However, I happen to know that this is because I take naps, and those tend to be 2 hours or less. Also, my Fitbit had some software bug initially, so it would sometimes run out of batteries in the middle of the night randomly.

![1](https://github.com/shubhamtiwari10/fitbit-analysis/blob/main/visualizations/1.PNG?raw=true)

For the purposes of this project, I will omit naps and/or artificially shortened sleep (< 3 hours).

![2](https://github.com/shubhamtiwari10/fitbit-analysis/blob/main/visualizations/2.PNG?raw=true)

Looks pretty normal.
 
Here, I define activity level as the number of steps taken. My activity distribution looks normal.

![3](https://github.com/shubhamtiwari10/fitbit-analysis/blob/main/visualizations/3.PNG?raw=true)

My sleep and activity data over the week:

![4](https://github.com/shubhamtiwari10/fitbit-analysis/blob/main/visualizations/4.PNG?raw=true)

Question 1 Results: My sleep does not predict my activity level the next day.

So, we can see from the regression table that how many hours I slept the previous night ('hours_prev') does not significantly predict the amount of steps I take the next day (p = .63). This might be for a variety of reasons.

First, I don't have a lot of data yet! I have only used my Fitbit for a couple months. Second, I am a graduate student, and my sleep is incredibly variable. Third, I love to be active! Even if I am tired, a run usually makes me feel better. Long story short is, I need more data.

![5](https://github.com/shubhamtiwari10/fitbit-analysis/blob/main/visualizations/5.PNG?raw=true)

 That flat line shows that there is no linear relationship.

Question 2: Do I need more sleep the night after I don't get a lot of sleep? In other words, am I building up a sleep deficit?
------------

In the model below, I predict the difference in amount of sleep for a given day from the previous nights' hours of sleep. To do so, I created a variable to capture the difference in amount of sleep I got from the night before. I then used an ordinary least squares regression model. 

Question 3 Results: Yes, I have built up a sleep deficit.

![6](https://github.com/shubhamtiwari10/fitbit-analysis/blob/main/visualizations/6.PNG?raw=true)

The regression table shows that how many hours I slept the previous night ('hours_prev') negatively predicts the difference in amount of sleep I get the next day. Put more simply, this means that if I get a good night's sleep, the next night, I don't need as much sleep. Conversely, if I don't get a lot of sleep, the next night, I make up for it by sleeping longer.

To make this finding easier to digest, let us visualize the relationship.

![7](https://github.com/shubhamtiwari10/fitbit-analysis/blob/main/visualizations/7.PNG?raw=true)

Here is the negative linear relationship as seen in our regression table.


Summary and Next Steps
------------ 

to recap, I imported data using Fitbit's API, worked with .json data, visualized my data, ran linear models, and performed a t-test. I found that (1) my activity level is independent from how much sleep I get, and (2) I built up a sleep deficit over time.


What I would like to do next is collect more data! I would also like to create some interactive visuals and run some more sophisticated models on my data. Finally, I would like to more thoroughly explore my heart rate data. The closer I get to defending my critique, the higher it seems to get. Should be fun to test if that is statistically significant.

 

