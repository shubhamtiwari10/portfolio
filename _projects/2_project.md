---
layout: post
title: Modeling System Resource Usage for Predictive Scheduling
description: Time-series forecasting
---

You can see how i did this [here](https://github.com/shubhamtiwari10/Modeling-System-Resource-Usage-for-Predictive-Scheduling){:target="_blank"}.

A machine learning-based solution for real-time resource allocation in the cloud (Time-series forecasting)
============

 I consulted with a company for a project using machine learning and neural networks to model and predict network usage. This company offers startups and new developers a simple yet revolutionary platform to manage their applications and cloud resources in one place. It also serves as a marketplace for additional applications and services, as well as an easy way to work with multiple APIs in one location.

As a consultant, I wanted to get a sense of company’s needs to help them reach their goals. Company was interested in gaining a sense of their current network resource usage and provisioning. In addition, Company wanted to move towards a machine learning approach to to make real-time predictions and automate scheduling of provisions. This was an exciting new challenge.

**The Challenge**
 
Historically, companies like these have to balance the competing needs of minimizing cost of paying for CPU bandwidth, for example, but also minimizing downtime by over-provisioning. This was even evidenced in the publicly available dataset from the TUDelft archive I used for my analysis. This data had similar characteristics to company’s actual data.

Therefore, my role as a consultant was to develop a model that will provide a more intelligent prediction of resource usage.

**Here is how I translated Company’s business objectives into an actionable deliverable:**

First, I used **time-series analysis, advanced regression techniques, and time series cross-validation** in Python (using scikit-learn) to characterize resource usage as well as **identify important predictive features**.

Next, I implemented DeepAR, a recently developed built-in algorithm from Amazon Sagemaker (hosted on AWS) to help Company shift towards **real-time analytics**. Amazon SageMaker DeepAR is a **supervised learning algorithm used to forecast time series using recurrent neural networks (RNN)**. Below is a summary of what I did for Company.

2nd paragraph. *Italic*, **bold**, and `monospace`. Itemized lists
look like:

  * this one
  * that one
  * the other one

Note that --- not considering the asterisk --- the actual text
content starts at 4-columns in.

> Block quotes are
> written like so.
>
> They can span multiple paragraphs,
> if you like.

Use 3 dashes for an em-dash. Use 2 dashes for ranges (ex., "it's all
in chapters 12--14"). Three dots ... will be converted to an ellipsis.
Unicode is supported. ☺


H2 Header
------------

Here's a numbered list:

 1. first item
 2. second item
 3. third item

Note again how the actual text starts at 4 columns in (4 characters
from the left side). Here's a code sample:

    # Let me re-iterate ...
    for i in 1 .. 10 { do-something(i) }

As you probably guessed, indented 4 spaces. By the way, instead of
indenting the block, you can use delimited blocks, if you like:

~~~
define foobar() {
    print "Welcome to flavor country!";
}
~~~

(which makes copying & pasting easier). You can optionally mark the
delimited block for Pandoc to syntax highlight it:

~~~python
import time
# Quick, count to ten!
for i in range(10):
    # (but not *too* quick)
    time.sleep(0.5)
    print(i)
~~~



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

![example image](https://images.unsplash.com/photo-1488190211105-8b0e65b80b4e?w=500&h=500&fit=crop "An exemplary image")

Inline math equation: $\omega = d\phi / dt$. Display
math should get its own line like so:

$$I = \int \rho R^{2} dV$$

And note that you can backslash-escape any punctuation characters
which you wish to be displayed literally, ex.: \`foo\`, \*bar\*, etc.
