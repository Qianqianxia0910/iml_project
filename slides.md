---
title:
- Group 117 Machine Learning Project
author:
- Tuomo Lehtonen, Qianqian Xia
theme:
- Antibes
date:
- December 14, 2022
---

# Overview

# Model selection
- Separately for binary and multi-label
    - Train multi-label classifier using only samples with associated event
- Considered models
    - Logistic regression (softmax function for multi-label)
    - Random forests
    - Support vector machine
- Feature selection
    - Separately for each model
    - Recursive feature elimination with 5-fold CV 
        - a variant of backwards feature elimination

# Chosen models and results
- Binary: 
    - Random Forest classifier
    - 15 selected features
    - Increased number of trees to 1500
    - Decent accuracy
        - 0.86 CV accuracy, 0.89 validation set accuracy
        - Actual test accuracy: 0.862

- Multi-label
    - Random Forest classifier
    - Trained on samples with an event class
    - 1500 trees 
    - Quite poor multi-label accuracy
        - Actual test accuracy: 0.666
        - Probably bad strategy chosen

