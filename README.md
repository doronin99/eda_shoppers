## About

This repository was created as part of a project on the course **"EDA and DevTools"**. The course covered the following topics: EDA, Git and GitHub, Docker, ML fundamentals. **Online Shoppers Purchasing Intention Dataset** was chosen for the course project.

## Files
* `online_shoppers_intention.csv`: data file
* `eda_shoppers.ipynb`: jupyter notebook with EDA, preprocessing and model selection
* `dashboard.html`: Explainer Dashboard saved as HTML file

## Dataset description

The Revenue attribute can be used as the class label.

`Administrative`, `Administrative Duration`, `Informational`, `Informational Duration`, `Product Related` and `Product Related Duration` represent the number of different types of pages visited by the visitor in that session and total time spent in each of these page categories. The values of these features are derived from the URL information of the pages visited by the user and updated in real time when a user takes an action, e.g. moving from one page to another.

The `Bounce Rate`, `Exit Rate` and `Page Value` features represent the metrics measured by "Google Analytics" for each page in the e-commerce site. The value of `Bounce Rate` feature for a web page refers to the percentage of visitors who enter the site from that page and then leave ("bounce") without triggering any other requests to the analytics server during that session. The value of `Exit Rate` feature for a specific web page is calculated as for all pageviews to the page, the percentage that were the last in the session. The `Page Value` feature represents the average value for a web page that a user visited before completing an e-commerce transaction.

The `Special Day` feature indicates the closeness of the site visiting time to a specific special day (e.g. Mother’s Day, Valentine's Day) in which the sessions are more likely to be finalized with transaction. The value of this attribute is determined by considering the dynamics of e-commerce such as the duration between the order date and delivery date. For example, for Valentina’s day, this value takes a nonzero value between February 2 and February 12, zero before and after this date unless it is close to another special day, and its maximum value of 1 on February 8.

The dataset also includes operating system, browser, region, traffic type, visitor type as returning or new visitor, weekend as a Boolean value indicating whether the date of the visit is weekend, and month of the year.

[Link](https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset) to the description of the original dataset.

## Summaries

 * The distribution of target variable across the classes is skewed. So, we're dealing with model evaluating problem as we can't use the accuracy as a measure of the model performance.
 * On numerical data *NB classifier* looks preferably due to higher balanced accuracy, but, on the other hand, *KNN classifier* has higher weighted F1 score.
 * Putting the categorical features into *KNN classifier* didn't give a better model performance.
 * If we need to estimate all features importances we should use *Logistic Regression* instead of *KNN classifier*, cause it have better metrics results.
 * With using of SHAP values we can see that one of the most influencing features in *LR model* are `PageValues` and `ExitRates`
