## Kickstarting Kickstarter
The goal of the project is to investigate Kickstarter Dataset to discover what makes a Kickstarter Project successful. We will be exploring machine learning model for predicting the success or failure of any given Kickstarter. 

Kickstarter Success is defined by "Funding Goal has been Reached within Time Limit".Success is related to paramaters such as backers, pledged, and state

## Project Background
This is a Xccelerate Machine Learning Group Project. Our team of talented data scientists include Alex Li, Hancock, and myself, Hui-Ee. We are proud to share our 3 days project with you the initial exploration of machine learning model exploration and evaluation. Sit back, relax, and enjoy the following.

## 1 -- Data Analysis and Data Cleaning
    Import Libraries
    Data Analysis
    Data Cleaning -- Finding Anomalities in the Data
    STATE — Consolidate “State” to “Successful & Failed”
    STATE — Convert “State” to Binary Format
    BACKERS — Overview
    BACKERS — Overvew in Backers_Log
    BACKERS — Backers vs Success
    BACKERS — Outliers
    PLEDGED — Pledges vs Success

## 2 -- Data Visualisation
We plot data to visualise and understand dataset. We will then use these insights to add or remove features for predicting the outcome.
#### 2.1  Data Visualisation — General Statistics
    Kickstarter projects are approximately 1/3 success and 2/3 failed
    Main Category — Film & Video + Music together contain 30% of the total projects 
    Sub Categories — Top 10 Most Successful 
    Sub Categories — Top 10 Most Failed 
    Countries — Top 10 Frequented -- 78% of the projects are from USA
    
#### 2.2  Data Visualisation — Measuring Success
"state" shows how successful is the project

    Success and Goal — The higher the goal amount set, the less likely a projects is to be successfully funded
    Success and Goal and Pledged — In 99% of the cases, as long as the pledged amount exceeds the goal, it is successful
    Success and Project Length on Launched to Deadline — Longer Campaign have higher failure rates. This occurs pretty much for all categories
    Success and Currency — No Correlation
    Success and Characters / Words Length — Weak Correlation.
    Character Limit at 60, set by Kickstarter
    Word Frequencies — The most Popular Words on the Successful / Failed project name
    
#### 2.3  Data Visualisation — Heatmap
    Heatmap that confirms strong relationship between pledged amount and backers. Nothing out of ordinary
    
## 3 -- Machine Learning
Explore Machine Learning model to find one with higher accuracy of ability to predict probability of Kickstarter success. We separate the parameter of user-defined parameters and prediction parameters. This is to allow the machine learning model to predict success or failure on its own.

User-defined parameters such as "name", "category", "currency", "project length", "goal in usd"

Prediction parameters such as "state"

Ultimately XGBoost shows the best performance with a greatest Accuracy Score of 70%. In general, after grid-searched, the Accuracy Score range is around 68%. Best Balance between "Precision" and "Recall" or 0.15 to 0.45.

The 3 major action taken to get a better prediction model is 1)Scaling to a different range to give greater weight for certain features 2) Taking Log Scale of "Goal Amount" provided marginally better results 3) Attempts at reengineering features resulted in <1% change for model.

#### 3.1  Decision Tree
    Before Tuning -- 62.2%
    After Tuning -- 68.6%
#### 3.2  Random Forest
    Before Tuning -- 66.0%
    After Tuning -- 68.5%
#### 3.3  Logistic Regression
    Before Tuning -- 68.4%
    After Tuning -- 69.1% 
#### 3.4  XGBoost
    Before Tuning -- 69.7%
    After Tuning -- 70.2% 
#### 3.5  AdaBoost
    Before Tuning -- 64.4%
    After Tuning -- 67.9%

## 4 -- Conclusion
To Kickstart Kickstarting success, it requires both the effort outside of the comfort of  Model Prediction. Hence, we suggest to prioritise the project properies such as 1) being featured by Kickstarter 2) social media features 3) have more than 20 backers. These 3 features build a strong foundation to place the project in the success category.

Then deploy XGBoost classifier model to determine success rate of a project launch, at approximately 68% is a good sign, prior to an official launch. 



