---
title       : Iris Data Set Prediction Model Analysis
subtitle    : Investigating the influence of seed and model
author      : Marisa Gioioso
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
transition  : fade
widgets     : [mathjax]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
logo        : question_logo.png
--- 
## Background

The model selection process may not be the most important part of the data analysis
process. This is because:

- Many prediction models have similar accuracy on certain data sets

- Other factors have a much bigger impact, like:

  - Quantity of data

  - Appropriate partitioning of data set to pre-empt overfitting

- [My shiny app](https://mgioioso.shinyapps.io/ShinyAppProject) is an interactive
way to investigate the impact of model type and seed on a Species
classification of the Iris dataset. 

--- {bg: lightblue}

## App Benefits

- The app can be used by any user even with minimal understanding of the statistics behind the predictive modeling process
- Can be used to create an experimental environment where users can compare
and understand the difference between different models and seeds
- Shows in graphical form how the accuracy changes and how the sample of
points changes with different seeds
- Ultimately shows the minimal impact that model and seed have on this problem,
at least among the predictive models provided by this app.

--- {bg: lightblue}

## Demonstration

- To illustrate the point here, let's see the difference between two very different models
and two different seeds for each model.
- If we choose the GBM and LDA models, and two seeds--123 and 8989--we get the following results for accuracy:


```
##      Seed 123 Seed 8989
## GBM 0.9333333 0.9777778
## LDA 0.9777778 1.0000000
```

- Since there are only 45 points in the testing set, if one model predicts just 
one more point accurately over the other, it results in an accuracy gain of .0222. So the results above are very close.

--- {bg: lightblue}

## Demonstration cont.

- Using the app, you can visualize the differences calculated in the last slide:

<div style='text-align: center;'>
    <img height='350' src='ShinyAppScreenshot2.png' />
</div>

- Notice the highlighted points that correspond to wrong predictions

  - These are the only 2 of 45 points that were incorrectly classified
  
  - This corresponds with the high accuracy calculated in the previous slide
