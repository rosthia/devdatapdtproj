App to Predict Vehicle MPG
========================================================
author: R.Thia
date: Sept 2015

========================================================
<H1> Introduction</H1>
The following shiny app is still under development due to the short time frame.
The simple app allows the user to input some basic details about vehicles and estimate its MPG.
The app is based on a simple GLM algorithm and the data data set "auto MPG" from the UCI Machine Learning Repository located [here](http://bit.ly/1sgiKaS).

========================================================
<H1>The Algorithm</H1>

```r
library(RCurl)
library(caret)
mpg<- getURL("https://docs.google.com/spreadsheets/d/12s5WVmzalqI4rwVkahBrtewMxFFPJwue4-vOq_atv4M/pubhtml")
mpg<- read.csv(text = mpg)
modFit <- train(mpg ~ cyl + disp + horse + weight + accel + year + origin, method="glm", data=mpg)
```
- The simple GLM model has a $RMSE$ of 3.35, and an $R^2$ of 0.818.  
Whereas other more complex algorithms were implemented, they yielded small improvements at the cost of much longer execution times so the GLM model was chosen as the backbone of the shiny app.

========================================================
<H1>Algorithm Predictions </H1>

<a href="http://tinypic.com?ref=so8eab" target="_blank"><img src="http://i58.tinypic.com/so8eab.png" border="0" alt="Image and video hosting by TinyPic"></a>


***
- The relative 45 degree line shape of this simple plot of actual vs. predicted MPG values demonstrates the simple GLM's decent fit.

========================================================
## Shiny App

<a href="http://tinypic.com?ref=i4mm8j" target="_blank"><img src="http://i62.tinypic.com/i4mm8j.png" border="0" alt="Image and video hosting by TinyPic"></a>

***
- This is a screenshot of the deployed shiny app.  It was tested and worked for various combinations of numeric inputs. It is available [here](https://rthia.shinyapps.io/devdatapdtproj/).
