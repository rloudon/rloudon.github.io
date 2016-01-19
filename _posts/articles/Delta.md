---
title: "Delta"
layout: post
date: 2015-08-31
categories: articles
tags: [data science, R, data.table, R package, data wrangling]
comments: true
share: true
---
  
* Table of Contents
{:toc}

#### Tips and tricks learned along the way 

This is mostly a running list of `data.table` tricks that took me a while to figure out either by digging into the [official documentation], adapting StackOverflow posts, or more often than not, experimenting for hours.  I'd like to persist these discoveries somewhere with more memory than my head (hello internet) so I can reuse them after my mental memory forgets them.  A less organized and concise addition to DataCamp's sweet [cheat sheet for the basics](https://s3.amazonaws.com/assets.datacamp.com/img/blog/data+table+cheat+sheet.pdf).

Most, if not all of these techniques were developed for real data science projects and provided some value to my data engineering.  I've generalized everything to the `mtcars` dataset which might not make this value immediately clear in this slightly contrived context.  This list is not intended to be comprehensive as DataCamp's data.table cheatsheet is.  OK, enough disclaimers!

Some more advanced functionality from `data.table` creator Matt Dowle [here](http://user2014.stat.ucla.edu/files/tutorial_Matt.pdf).



# Portable R with Shiny

1. Preparing

2. Packaging

3. Publish

Bonus: Top



{% highlight text %}
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##    2.00   26.00   36.00   42.98   56.00  120.00
{% endhighlight %}



## R Markdown

This is an R Markdown presentation. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown.



# Slide with R Code and Output


{% highlight text %}
##      speed           dist       
##  Min.   : 4.0   Min.   :  2.00  
##  1st Qu.:12.0   1st Qu.: 26.00  
##  Median :15.0   Median : 36.00  
##  Mean   :15.4   Mean   : 42.98  
##  3rd Qu.:19.0   3rd Qu.: 56.00  
##  Max.   :25.0   Max.   :120.00
{% endhighlight %}
