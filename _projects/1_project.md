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

### An h3 header ###

Now a nested list:

 1. First, get these ingredients:

      * carrots
      * celery
      * lentils

 2. Boil some water.

 3. Dump everything in the pot and follow
    this algorithm:

        find wooden spoon
        uncover pot
        stir
        cover pot
        balance wooden spoon precariously on pot handle
        wait 10 minutes
        goto first step (or shut off burner when done)

    Do not bump wooden spoon or it will fall.

Notice again how text always lines up on 4-space indents (including
that last line which continues item 3 above).

Here's a link to [a website](http://foo.bar), to a [local
doc](local-doc.html), and to a [section heading in the current
doc](#an-h2-header). Here's a footnote [^1].

[^1]: Some footnote text.

Summary and Next Steps
------------ 

Tables can look like this:

| Header 1 | Header 2                   | Header 3 |
|:--------:|:--------------------------:|:--------:|
| data1a   | Data is longer than header | 1        |
| d1b      | add a cell                 |          |
| lorem    | ipsum                      | 3        |
|          | empty outside cells        |          |
| skip     |                            | 5        |
| six      | Morbi purus                | 6        |


A horizontal rule follows.

***

Here's a definition list:

apples
  : Good for making applesauce.

oranges
  : Citrus!

tomatoes
  : There's no "e" in tomatoe.

Again, text is indented 4 spaces. (Put a blank line between each
term and  its definition to spread things out more.)

Here's a "line block" (note how whitespace is honored):

| Line one
|   Line too
| Line tree

and images can be specified like so:

![example image](https://github.com/shubhamtiwari10/fitbit-analysis/blob/main/visualizations/1.PNG?raw=true)

Inline math equation: $\omega = d\phi / dt$. Display
math should get its own line like so:

$$I = \int \rho R^{2} dV$$

And note that you can backslash-escape any punctuation characters
which you wish to be displayed literally, ex.: \`foo\`, \*bar\*, etc.
