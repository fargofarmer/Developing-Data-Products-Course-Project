Developing Data Products Course Project: Iris Data Exploration
========================================================
author:PK 
date: 9/17/2016
autosize: true

Introduction
========================================================


- The Iris Data Exploration app was developed in Shiny Package, which can be used to build interactive web applications with R. 
- This app allows the user to learn the general statics of the Iris Data set.

- Users can explore the data by selecting a data variable as well as no. observations.

- The App consists of 2 plots Tabs, 1 summary Tab, 1 Covariance Tab and 1 Correlation Tab. When a user a selects a data variable and no.of observations, results and plots can be found in each tab. 

- The app can be found at https://fargofarmer.shinyapps.io/exploring-iris-data/

Code
========================================================



```r
library(knitr)  
opts_chunk$set(echo = TRUE)  
library(dplyr)  
library(ggplot2)
library(datasets)
data("iris")
##Sample Alogrithm
table(summary(iris))
```

```

1st Qu.:0.300   1st Qu.:1.600   1st Qu.:2.800   1st Qu.:5.100   
              1               1               1               1 
3rd Qu.:1.800   3rd Qu.:3.300   3rd Qu.:5.100   3rd Qu.:6.400   
              1               1               1               1 
Max.   :2.500   Max.   :4.400   Max.   :6.900   Max.   :7.900   
              1               1               1               1 
Mean   :1.199   Mean   :3.057   Mean   :3.758   Mean   :5.843   
              1               1               1               1 
Median :1.300   Median :3.000   Median :4.350   Median :5.800   
              1               1               1               1 
Min.   :0.100   Min.   :1.000   Min.   :2.000   Min.   :4.300   
              1               1               1               1 
setosa    :50   versicolor:50   virginica :50   
              1               1               1 
```
*****
-The algorithm written for Shiny application simply calculates mean and other parameters of each iris data variable. Variance in the summary can be observed with change in No. of Observations.   

Slide With Plot
========================================================

![plot of chunk unnamed-chunk-2](Iris Data Exploration-figure/unnamed-chunk-2-1.png)![plot of chunk unnamed-chunk-2](Iris Data Exploration-figure/unnamed-chunk-2-2.png)
****
Histogram Plot Shows varince in normal distribution with respct to no. observations. As No. of observations or sample size increases, a better bell curve can be achieved. Except the Petal.Width, the rest of variables typically normally distributed. 

Correlation
========================================================

```
     Sepal.Length Sepal.Width Petal.Length Petal.Width
[1,]    0.6856935   -0.042434     1.274315   0.5162707
```

```
     Sepal.Length Sepal.Width Petal.Length Petal.Width
[1,]            1  -0.1175698    0.8717538   0.8179411
```
****
In the last step, the application verifies the correlation and covariance among variables. We observed coorelation and covarience are stronger among Sepal.Length, Petal.Length and Petal.Width.
