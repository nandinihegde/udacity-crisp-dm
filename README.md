This project is part of the submission for UDACITY CRISP-DM Project.

**Summary/Motivation for the project:**
Covid-19 forced several states in the United States to announce lockdowns which had its impact on several businesses. Specifically the City of Los Angeles went into lockdown starting March,2020.
This project is an Impact analysis of COVID lockdowns on Airbnb listings in Los Angeles. A comparitive approach has been used to conduct this analysis wherein the Bookings trends of early 2019 were compared to that of early 2020.
**Blog-post:**
My medium blogpost is available to read on https://medium.com/@hegdenandini/impact-analysis-of-covid-lockdowns-on-airbnb-listings-in-los-angeles-19597b8c
 
**Datasets used:**
The datasets are fairly large in size and could not be included in the repository but can be found on http://insideairbnb.com/
To describe briefly, the Inside Airbnb website provides the calendar, listings and reviews dataset scraped for each month dating back several years. For the purpose of this analysis only the calendars and listing dataset scraped for bookings made in Los-Angeles between Jan to June 2019 and 2020 were utilised

**Business Questions posed**
For the purpose of conducting this analysis, I have tried to derive the answers to the following three questions.
  1. Is there a major change in the trend of bookings made from Jan to June in 2020 when compared to 2019?
  2. What is the estimated impact on Total Daily Bookings and revenue (Sales)?
  3. What are the Features/Characteristics of the listings that were most important in 2019 vs 2020 in predicting the bookings?
 
**Files in the repository**
The analysis is broken down into 2 parts which can be found in the files as named below.
- Part-1 CRISP-DM Project-Part 1 Calendar analysis_20201003_final.ipynb: Consists of exploratory data analysis on the Calendars dataset to explore the trend in bookings and revenue. This part helps derive answers to the first two questions.
- Part-2 CRISP-DM Project-Part 2 Lisitings analysis_20201003_final.ipynb: This part explores the Listing datasets in conjuctions with the Calendars dataset to build a Machine learning model to identify the features that most affected bookings during these two years. This part majorly answers the third question.
f6ac
 
 **Libraries used:**
 The following Python libraries were used to support the analysis:
 
 #For Data reading and manipulation
    import pandas as pd
    import os
    import datetime
    import re
    import locale
    import numpy as np
    import calendar

    #Data visualization
    import matplotlib.pyplot as plt
    import matplotlib.dates as mdates
    import matplotlib.cbook as cbook
    import seaborn as sns

    # Machine learning model evaluation 
    from sklearn.model_selection import train_test_split
    # Import the model we are using
    from sklearn.ensemble import RandomForestRegressor
    from sklearn.model_selection import RandomizedSearchCV
    from sklearn.impute import SimpleImputer
    import category_encoders as ce
    from sklearn.model_selection import GridSearchCV


    #Saving models and printing params
    import pickle
    from pprint import pprint

    #Google cloud connectivity related libaries
    import gcsfs
    from google.cloud import storage
    from IPython.core.display import display
    import pandas_gbq

    #garbage collector to free memory
    import gc

**Summary of the results of the analysis:**
The following findings and insights were a result of the analysis:
 - There was a pretty striking increase in cancellations from the month the lockdowns started in March 2020 which resulted in an estimated dip of 3500 to 5000 bookings daily on an average.
 - ALthough the initial months of the lockdown in 2020 saw a dip in Daily revenue resulting from the cancellations, the advanced bookings towards the end of year in 2020 were currently still showing as higher compared to the stats during the same months of 2019
 - Time based variables/features had the most impact in predicting the bookings, however in 2020 the months of march-june shows a striking impact in precitability which sends a strong indication that the Bookings were simply affected by them being during these months of lockdown rather than any other factor
 
 **Acknowledgements**
 Several sources were referenced in the completion of this project some of which are listed as below.
 - https://towardsdatascience.com/random-forest-in-python-24d0893d51c0
 - https://towardsdatascience.com/running-jupyter-notebook-in-google-cloud-platform-in-15-min-61e16da34d52
 - https://towardsdatascience.com/hyperparameter-tuning-the-random-forest-in-python-using-scikit-learn-28d2aa77dd74
 - https://medium.com/greyatom/why-how-and-when-to-scale-your-features-4b30ab09db5e
 - https://www.analyticsvidhya.com/blog/2016/01/guide-data-exploration/
 
 
