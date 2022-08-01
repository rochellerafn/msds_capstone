---
title: "H&M Capstone Project"
author: "Rochelle Rafn"
date: '2022-08-01'
slug: h-and-m-capstone-project
categories: []
tags: []
---

# 50 year olds shopping at H&M? What’s that all about? 

## Question

For those who are unfamiliar with H&M, it’s a fast fashion retailer known for its affordable, youthful and trendy styles. My whole life I have been into fashion. Who knows? Maybe when I’m 50 I will still be shopping at H&M or similar stores, like Zara. However, even in my 30s, If I venture into H&M I feel noticeably older than everyone else there. So, where are these 50 year old and who are they? This lead me to questioning, does age actually matter for perceivably ‘younger’ and trendy stores like H&M? Are the different generational age groups actually purchasing different things? Spoiler alert, they are not. So what does this mean? Who are these 50 year olds and why are their purchase habits similar to the 20 somethings? 


## Context

The importance of these questions lies within the realm of demographics and marketing. Traditionally we believe that location, age, gender all matter and make a difference. And… they do. But, what if they don’t? In order to make appropriate and informed decisions it is important to do proper analysis to make sure we’re not assuming something about someones age or gender that ends up being incorrect. That is the beauty of data. We can dive in the deep end and really see what is beneath the surface of human bias. 


## Summary

I started this project with a very different question in mind. However. the very first thing I checked in the data was the age distribution. I really only did this to verify my own assumption that it would peak somewhere in the mid 20s and then continue to taper off as age increased. I was definitely surprised to see this somewhat bimodal distribution with a second peak around 50 years old. I remember thinking, “What?? That is so bizarre.” Twice as many 50 somethings as 30 somethings seemed just, wrong. 


```r
knitr::opts_chunk$set(echo = FALSE, warning = FALSE, message = FALSE)

library(ggplot2)
customers <- read.csv('/Users/rochellerafn/RStudio Files/h-and-m-personalized-fashion-recommendations/customers.csv') 

ggplot(customers, aes(age))+
  geom_bar(fill = 'black')+
  theme_bw()+
  xlim(15, 80)
```

```
## Warning: Removed 16973 rows containing non-finite values (stat_count).
```

```
## Warning: Removed 1 rows containing missing values (geom_bar).
```

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-1-1.png" width="672" />

My immediate thought was that it is a group of ‘young at heart’ and fashion conscious 50 year olds. Then, as I looked a little closer at the distribution I did the math and realized the peaks moved almost identically within about 30 years of each other. That logically seems pretty close to a parent-child age gap. This lead me to the question, does the age even matter? If the 50 year olds are actually purchasing for their children the items would be virtually the same.


## Data Description

The data set I’m analyzing comes directly from H&M spanning 1.3 million customers (ages 16-99), 53 online markets, 4,850 retail stores and 31 million transactions over 2 years. It came with three relational data frames with details on Customers, Articles (clothing items) and Transactions. 


## Exploratory Data Analysis

Given the question and data that I have, I decided to make age the outcome variable. How can we predict the difference between the young and mature generations? To start, I split the data into the two age groups, “young” (<=39) and “mature” (>=40). This is where I would start my exploratory analysis to see what differences I could find. 

I started with, what are the most popular items in each age group? This might show me if there are any differences. As we can see here, the top 3 items are identical. However, the fourth item is different. This piqued my interest since that fourth items seems to indicate a generational difference. However, the more I dug, the less significant this difference became.

### Mature Top Items
![](images/0706016001.jpg)
![](images/0706016002.jpg)
![](images/0372860001.jpg)
![](images/0610776105.jpg)

### Young Top Items
![](images/0706016001.jpg)
![](images/0706016002.jpg)
![](images/0372860001.jpg)
![](images/0759871002.jpg)


### What are the most popular unique items in each age group?
I reduced the items even further by figuring out what each group purchased that the other did not. 

### Young Unique Items
![](images/0803545002.jpg)
![](images/0814307002.jpg)
![](images/0533261025.jpg)
![](images/0695662008.jpg)

### Mature Unique Items



On the surface it seemed that the younger group was purchasing more baby clothes and the mature generation not so much. However, each of the items were only purchased as much as 86 times out of more than 21million items purchased. Unfortunately the math here is not significant enough to consider.


### What are the top descriptive words for the unique items in each age group?
To move forward with the theme of unique items I decided to take those unique items even deeper by analyzing the descriptive words of these items. As I had guessed, the unique items really did not hold any significance due to the small amount. Also, even though the items are different, there are still many purchases by both groups that have the same descriptive words despite the specific item differing.

### Mature Top Words
![](images/mature_wordcloud.jpeg)

### Young Top Words
![](images/young_wordcloud_u.jpeg)

### Young Top Word Count 

```
##            word    n
## 1          body 4499
## 2       garment 4488
## 3  babychildren 3628
## 4         sizes 3177
## 5        cotton 2766
## 6         solid 2749
## 7        jersey 2730
## 8          dark 2693
## 9         light 2637
## 10         soft 2613
```

### Mature Top Word Count

```
##            word    n
## 1          body 2295
## 2       garment 2293
## 3  babychildren 1756
## 4      children 1595
## 5          dark 1507
## 6         sizes 1489
## 7         upper 1401
## 8         solid 1345
## 9        jersey 1227
## 10        front 1184
```

## What about percentage of descriptive words?


```
##   X graphical_appearance_name pct_difference y_graphic_pct m_graphic_pct
## 1 1                     Solid      3.2125813     57.326729     54.114148
## 2 2          All over pattern      1.1936976     12.085263     13.278961
## 3 3                   Melange      1.0134998      5.609772      6.623272
## 4 4                     Denim      0.8242733      5.918383      6.742657
## 5 5           Other structure      0.6299426      2.498354      1.868411
## 6 6                      Lace      0.5421161      2.048154      1.506038
##   y_graphic_count m_graphic_count
## 1         3459722         1872928
## 2          729357          459594
## 3          338555          229236
## 4          357180          233368
## 5          150778           64667
## 6          123608           52125
```


### Is there a noticeable difference in graphic appearance for each age group?
![](images/Rplot.jpeg)


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

