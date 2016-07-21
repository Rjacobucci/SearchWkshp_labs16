Exploratory Data Mining via SEARCH Strategies -- Lab #1
========================================================
author: Ross Jacobucci
date: 7/20/2016
autosize: true

Outline
========================================================

The first lab will go over the basics of programming in R along with covering Smoothing and Stepwise Regression

To get started, I recommend downloading Rstudio as an interface to R. Benefits include:
- Easier to download packages
- Easier to view plots
- Can load datasets without code

Loading Datasets
========================================================

Many datasets that we will be using come with installed packages

```r
library(MASS) # for boston data
data(Boston)
```
Now the Boston dataset is in your workplace

```r
head(Boston[,1:4],3)
```

```
     crim zn indus chas
1 0.00632 18  2.31    0
2 0.02731  0  7.07    0
3 0.02729  0  7.07    0
```

Load your own datasets
========================================================

Data saved as .dat

```r
data = read.table(file.choose(),sep="",header=F,na.strings="NA")
```
.csv

```r
data = read.csv(file.choose(),header=T,na.strings=".")
```
.sav for SPSS files

```r
library(foreign)
data = read.spss(file.choose(),to.data.frame=TRUE)
```

How to get help
========================================================
