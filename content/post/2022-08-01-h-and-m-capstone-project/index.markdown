---
title: H&M Capstone Project
author: R package build
date: '2022-08-01'
slug: h-and-m-capstone-project
categories: []
tags: []
---


```r
knitr::opts_chunk$set(echo = FALSE, warning = FALSE, message = FALSE)
```


# 50 year olds shopping at H&M? What’s that all about? 

## Question

For those who are unfamiliar with H&M, it’s a fast fashion retailer known for its affordable, youthful and trendy styles. My whole life I have been into fashion. Who knows? Maybe when I’m 50 I will still be shopping at H&M or similar stores, like Zara. However, even in my 30s, If I venture into H&M I feel noticeably older than everyone else there. So, where are these 50 year old and who are they? This lead me to questioning, does age actually matter for perceivably ‘younger’ and trendy stores like H&M? Are the different generational age groups actually purchasing different things? Spoiler alert, they are not. So what does this mean? Who are these 50 year olds and why are their purchase habits similar to the 20 somethings? 


## Context

The importance of these questions lies within the realm of demographics and marketing. Traditionally we believe that location, age, gender all matter and make a difference. And… they do. But, what if they don’t? In order to make appropriate and informed decisions it is important to do proper analysis to make sure we’re not assuming something about someones age or gender that ends up being incorrect. That is the beauty of data. We can dive in the deep end and really see what is beneath the surface of human bias. 


## Summary

I started this project with a very different question in mind. However. the very first thing I checked in the data was the age distribution. I really only did this to verify my own assumption that it would peak somewhere in the mid 20s and then continue to taper off as age increased. I was definitely surprised to see this somewhat bimodal distribution with a second peak around 50 years old. I remember thinking, “What?? That is so bizarre.” Twice as many 50 somethings as 30 somethings seemed just, wrong. 

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-2-1.png" width="672" />

My immediate thought was that it is a group of ‘young at heart’ and fashion conscious 50 year olds. Then, as I looked a little closer at the distribution I did the math and realized the peaks moved almost identically within about 30 years of each other. That logically seems pretty close to a parent-child age gap. This lead me to the question, does the age even matter? If the 50 year olds are actually purchasing for their children the items would be virtually the same.


## Data Description

The data set I’m analyzing comes directly from H&M spanning 1.3 million customers (ages 16-99), 53 online markets, 4,850 retail stores and 31 million transactions over 2 years. It came with three relational data frames with details on Customers, Articles (clothing items) and Transactions. 


## Exploratory Data Analysis

Given the question and data that I have, I decided to make age the outcome variable. How can we predict the difference between the young and mature generations? To start, I split the data into the two age groups, “young” (<=39) and “mature” (>=40). This is where I would start my exploratory analysis to see what differences I could find. 

I started with, what are the most popular items in each age group? This might show me if there are any differences. As we can see here, the top 3 items are identical. However, the fourth item is different. This piqued my interest since that fourth items seems 

#### Mature Top Items
![](images/0706016001.jpg)
![](images/0706016002.jpg)
![](images/0372860001.jpg)
![](images/0610776105.jpg)

#### Young Top Items
![](images/0706016001.jpg)
![](images/0706016002.jpg)
![](images/0372860001.jpg)
![](images/0759871002.jpg)


### What is the summary of price per age group?

```
##      Min.   1st Qu.    Median      Mean   3rd Qu.      Max. 
## 0.0000339 0.0169322 0.0254068 0.0287606 0.0338814 0.5915254
```

```
##      Min.   1st Qu.    Median      Mean   3rd Qu.      Max. 
## 0.0000169 0.0152373 0.0250339 0.0273048 0.0338814 0.5915254
```


### How many items are each group purchasing per transaction?

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##     1.0     3.0     5.0     6.6     8.0   336.0
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##   1.000   3.000   5.000   7.617  10.000 570.000
```


### What are the most popular unique items in each age group?
#### Young



What are the top descriptive words for the unique items in each age group?
 
library(tidyverse)
library(wordcloud)



wordcloud(young_cor_words_u, scale = c(2, 1), min.freq = 600, colors = rainbow(30))
wordcloud(mature_cor_words_u, scale = c(2, 1), min.freq = 300, colors = rainbow(30))

head(young_wordcounts, 10)

head(mature_wordcounts, 10)


What about percentage of descriptive words?

all_graphic_pct <- read.csv(‘/Users/rochellerafn/RStudio Files/h-and-m-personalized-fashion-recommendations/all_graphic_pct’)

head(all_graphic_pct)

Is there a noticeable difference in graphic appearance for each age group?







