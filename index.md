---
title       : BMIApp
subtitle    : An Intuitive Body Mass Index Calculator
author      : Kokako
job         : Data Scientist
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Why BMI?

Body mass index (BMI) is a simple calculation based on a person's height and weight that is used as a screening tool to identify possible weight issues in adults. It's key features:

1. BMI has been shown to correlate strongly with body fat percentage, but is much easier and cheaper to implement than most body fat measurement techniques.
2. This relationship means that ranges of BMI values can indicate the weight status of an individual (underweight, normal, overweight, or obese).
3. BMI is easy for everyone, from doctors to the public, to calculate and understand. 

---

## Features of BMIApp

BMIApp takes a user's height (in feet and inches) and weight (in pounds) and calculates their BMI. In addition, it displays the weight status of the user predicted by their BMI.

Example: Suppose I am 5' 3" and 120 lbs. I enter in my information and the following code is performed:


```r
bmi <- round(weight / (height)^2 *703, digits=1)
## Threshold numbers from the CDC
if(bmi < 18.5) {
    weightstatus <- "underweight"
} else if(bmi >= 18.5 & bmi <= 24.9) {
    weightstatus <- "normal"
} else if(bmi >= 25.0 & bmi <= 29.9) {
    weightstatus <- "overweight"
} else {weightstatus <- "obese"}
print(paste("Your BMI is", bmi, "which means you are", weightstatus, "."))
```

```
## [1] "Your BMI is 21.3 which means you are normal ."
```

---

## Disclaimers

Please note that the BMIApp is meant for simplifying the BMI calculation only, not for health assessment.

Body mass index is meant as a screening tool only: it can indicate where there may be a problem with your weight, but only a healthcare professional can fully assess your overall health (of which weight is only one component).

---

## Resources

Start using the BMIApp now! 
[Link to shinyApps](https://kokako.shinyapps.io/Assignment/)

Read about the Centers for Disease Control and Prevention's guidelines on BMI: 
[CDC website](http://www.cdc.gov/healthyweight/assessing/bmi/adult_bmi/)

Thank you for your support.



