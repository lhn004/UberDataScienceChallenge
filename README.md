# UberDataScienceChallenge

## Problem
Uber’s Driver team is interested in predicting which driver signups are most likely to start driving. To help explore this question, we have provided a sample dataset of a cohort of driver signups in January 2016.The data was pulled a few months after they signed up to include the result of whether they actually completed their first trip. It also includes several pieces of background information gather about the driver and their car.

The goal of the challenge is to understand what factors are best at predicting whether someone who signs up will actually drive, and offer suggestions to how to put those insights to use in order to help Uber. With that being said, there are 3 steps to complete:

* 1. Clean, Explore, Visualize the data as needed to find out what fraction of the signups took an initial first trip.

* 2. Build, Run, and Evaluate a Predictive Model that will help Uber determine whether or not someone who signs up will start driving. Possibly run a model selection process to discuss why the chosen model was selected, any alternatives that were considered, and any concerns that may have come up.

* 3. Discuss the insights drawn from the model and how Uber may leverage them to get more signups to take their first trip.

## Dataset Description
* `id`: driver_id
* `city_id`: city_id this user signed up in
* `signup_os`: signup device of the user (“android”, “ios”, “website”, “other”)
* `signup_channel`: what channel did the driver sign up from (“offline”, “paid”, “organic”, “referral”)
* `signup_timestamp`: timestamp of account creation; local time in the form ‘YYYY MM DD’
* `bgc_date`: date of background check consent; in the form ‘YYYY MM DD’
* `vehicle_added_date`: date when driver’s vehicle information was uploaded; in the form ‘YYYY MM DD’
* `first_trip_date`: date of the first trip as a driver; in the form ‘YYYY MM DD’
* `vehicle_make`: make of vehicle uploaded (i.e. Honda, Ford, Kia)
* `vehicle_model`: model of vehicle uploaded (i.e. Accord, Prius, 350z)
* `vehicle_year`: year that the car was made; in the form ‘YYYY’

## Insights and Recommendation
### Insights
* The main factor that is best at predicting whether someone who signs up completes their first drive is the time it takes them to submit their background check consent form. Uber may want to come up with ways to encourage their signups to complete their background check consent form as soon as possible.

* The analysis revealed that although Uber receives most of their signups through the Paid channel, more signups who completed their first drive signed up through a Referral. This could be a good opportunity for Uber to increase their signups by referrals.

* During the Chi-Squared Test, I noticed that most signups who completed their first drive signed up using an iOS device. If Uber make plans to somehow target apple users a little more, it may help increase the first driver rate.

### Improvements
Collecting more positive samples to balance out the data would have improved the model’s sensitivity and specificity. This is always a bottleneck with Machine Learning algorithms. The higher the quality of the data, the higher the performance of the ML models.

* Univariate Analysis - The features that I removed in the cleaning process could have been explored more. Maybe the year of the vehicle contributed heavily to whether a signup completed their first drive. For example, what if cars produced after 2011 were more likely to drive after signing up. 

* Better Models - By incorporating more variables into our model that predicts whether Uber drivers start driving, we can potentially enhance its performance. Additional variables, such as driver demographics, vehicle information, historical trip data, and external factors like weather or surge pricing, can provide valuable insights into driver behavior and help uncover influential factors that influence their decision to start driving. By considering these variables, we can create a more comprehensive and accurate model that better captures the underlying patterns and improves predictions of driver activation.
