Yelp Data Analysis on Finding Factors that Influence Business Ratings
========================================================
author: Tianzhixi Yin
date: 11/21/2015

Summary
========================================================

Primary question: what factors influence the rating of a business?

- A predictive model for *stars*
- Word Clouds


Predictive Model
========================================================
A predictive model for *stars* with *categories*, *state*, *city*, *neighborhoods*, and *review_count* as predictors using Boosting.


```
gbm(formula = stars ~ ., distribution = "gaussian", data = businessSample[train, 
    ], n.trees = 100, interaction.depth = 4, shrinkage = 0.01)
A gradient boosted model with gaussian loss function.
100 iterations were performed.
There were 5 predictors of which 4 had non-zero influence.
```

The mean prediction error is:


```
[1] 0.7717972
```

Word Cloud
========================================================

Word cloud of the 1 star ratings.

![plot of chunk unnamed-chunk-3](Yelp5Slides-figure/unnamed-chunk-3-1.png) 

Conclution
========================================================

- People in different cities and neighborhoods tend to give different ratings.
- Various attributes of a business could be important. (For example, by appointments only or not, the noise level.)
- Food quality, waiting time and service provided are always what customers care most about

