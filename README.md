# BANK-MARKETING-EFFECTIVENESS-PREDICTION

# Problem Statement

▪ **Aim:-** Predicting the effectiveness of bank
marketing campaigns

# Problem Statement:

The data is related with direct marketing campaigns of a Portuguese
banking institution. The marketing campaigns
were based on phone calls. Often, more than one
contact to the same client was required, in order
to access if the product (bank term deposit)
would be ('yes') or not ('no') subscribed.The
classification goal is to predict if the client will
subscribe a term deposit (variable ‘y’).

# 💾 Project Files Description

This Project includes 1 executable files, 1 presentation and 1 project documentation as follows:

**Executable Files:**
Bank_Marketing_Effectiveness_Prediction.ipynb Team Notebook - Complete notebook containing Data exploration/Data processing/transformation/model development.

**Presentation:**
Bank_Marketing_Effectiveness_Predictio.pdf - Contains presentation i.e pptx of the project .

**Document:**
Bank_Marketing_Effectiveness_Prediction_cohort_nilgiri.docx.pdf - Includes the documentation of the project.

# Data Summary

**Categorical Features**

▪ Marital - (Married , Single , Divorced)

▪ Job-(Management,BlueCollar,retired etc)

▪ Contact - (Telephone,Cellular,Unknown)

▪ Education (Primary,Secondary,Tertiary)

▪ Month-(Jan,Feb,Mar,Apr,May etc)

▪ Poutcome - (Success,Failure,Other,Unknown)

▪ Housing - (Yes/No)

▪ Loan - (Yes/No)

▪ Default - (Yes/No)

**Numerical Features**

▪ Age

▪ Balance

▪ Day

▪ Duration

▪ Campaign

▪ Pdays

# Target variable

The target variable ‘y’ tells us the
outcome of the campaign whether they
went ahead for the term deposit or not.
Out of 100% only 11.70% people
subscribed to the term deposit


# As per Exploratory Data Analysis EDA

• - no missing value found

• - no feature found with one value

• - 9 categorical features

• - not found any significant linear relationship amongst predictors

• - it seems some outliers found (age, balance, duration, campaign, pdays and previous
has some outliers)

# Handling Imbalance data Using SMOTE

SMOTE library used to generate synthetic data for handling the
imbalance in the dataset

● Purpose: to minimize the bias of model towards the class which has
higher percent count in our dataset.


# Model building

With duration columns:

1. KNN( K Nearest Neighbours)
2. Random Forest
3. Light GBM

Without duration columns:

1. Light GBM
2. ANN(Artificial Neural Nets)

![image](https://user-images.githubusercontent.com/66200786/161384413-aa902187-b0e5-4076-b24c-69c84194941a.png)

![image](https://user-images.githubusercontent.com/66200786/161384467-909e52c6-a661-46a5-bb9e-63a8f0168e93.png)

# Shap Summary plots for model explainability

![image](https://user-images.githubusercontent.com/66200786/161384539-6bc53a68-e919-4942-b668-fd74e02ace6c.png)

# Conclusion

Thus we come to an end of our analysis and model building to predict if the client will subscribe a term deposit or not. The most important takeaways are:
If the clients are contacted twice in first 10 days of the month, then it is more likely that call will be converted to subscription.
Clients take more subscriptions in a month of January, May or August.
If clients are already paying housing loans, then it is more likely that they will opt for term deposit.
In our dataset we were provided with call 'duration' but in real world practise that won't be the case. So, to build more realistic model we trained our models for both the cases i.e with or without 'duration'. For both the cases LGBM showed best scores of recall with 'duration' and precision without 'duration'.

# Future Scope


Our main objective is to get good precision score for without 'duration' models and good recall
score for 'duration' included model.

● So, we can initially formulate the required time to converge a lead using 'duration' included models
and then sort out precise leads for 'duration' excluded models using this formulated time.

● Here, the idea is to find out responses for any particular record with varying assumed predefined
duration range.For example let's say, to converge a call, duration ranges between 60 to 2000 sec, then using this
range we can predict all responses for each lead while iterating through this duration range. If we
get positive response for any value of 'duration' we can assign that duration time to that particular
lead.

● In this way we can help marketing team to get precise leads along with time required to converge
that lead and also, those leads that have least proability to converge (if we get no positive response
for any assumed duration). Thus, an effective marketing campaign can be executed with maximum
leads converging to term deposit.

# 📚 References

Available: https://machinelearningmastery.com/gentle-introduction-xgboost-applied-machine-learning/

Wikipedia.org, 'XGBoost'. [Online].

Available: https://en.wikipedia.org/wiki/XGBoost

Youtube.com, 'XGBoost working'. [Online].

Available: https://www.youtube.com/watch?v=OQKQHNCVf5k

Manisha-sirsat.blogspot.com, 'What is Confusion Matrix and Advanced Classification Metrics?'. [Online].

Available: https://manisha-sirsat.blogspot.com/2019/04/confusion-matrix.html

