---
title: "Reproducible Research: Peer Assessment 1"
output: 
  html_document:
    keep_md: true
---


## Loading and preprocessing the data

```r
unzip("activity.zip")
activity <- read.csv("activity.csv")
byDate <- aggregate(activity$steps, by=list(date = activity$date), FUN = sum, na.rm=TRUE, na.action=NULL)
names(byDate)[2] = "steps"
```


## What is mean total number of steps taken per day?

```r
hist(byDate$steps)
```

![plot of chunk unnamed-chunk-2](figure/unnamed-chunk-2-1.png)
The mean of steps per day is 9354.2295082.
The median steps per day is 10395.


## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
