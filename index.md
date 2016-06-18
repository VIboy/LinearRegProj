---
title       : Simple Linear Regression
subtitle    : Prediction of Diamond Prices using Linear Regression
author      : WC Hoh
job         : Retired
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Slide 2
Simple Regression Model:
 Defines relationship between a dependent variable, and
 a single independent predictor variable.
 The equation for this relationship:
###      y = a + bx
      
#### y: dependent variable
#### x: independent predictor variable
#### a: intercept
#### b: change in y given an increase in x

--- .class #id
## Slide 3
## Diamond Dataset:

#### 48 observations of 2 variables: price and weight

### Using the following linear regression equation:
### fit <- lm(price ~ carat, data=diamond)
### the relevant coefficients are:

```
## (Intercept)       carat 
##   -259.6259   3721.0249
```

--- .class #id
## A Plot to show the linear relationship between the price and weight in carats
![plot of chunk unnamed-chunk-2](assets/fig/unnamed-chunk-2-1.png)

--- .class#id

### Prediction equation:
#### As an example, if weight=0.2 carats, the predicted price will be:


```r
price = coef(fit)[1] + coef(fit)[2]*0.2

price # In Singapore dollars
```

```
## (Intercept) 
##    484.5791
```
#### The price of 0.2 carat diamond is estimated to be S$ 484.58




