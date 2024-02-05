# 🚀 Sigma Cabs - multi-class classification

This repository contains research for multi-class classification use case.

Task: We will work with data from the taxi aggregator Sigma Cabs. Depending on the characteristics of the trip, one of three types of increased pricing needs to be predicted: [1, 2, 3]. Thus, this will help the company optimally match taxis and customers.

## DATA Review
| Field name | Overview |
| ------ | ------ |
| GTrip_ID | ID for TRIP |
| Trip_Distance | The distance for the trip requested by the customer |
| Type_of_Cab | Category of the cab requested by the customer |
| Customer_Since_Months | Customer using cab services since n months; 0 month means current month |
| Life_Style_Index | Proprietary index created by Sigma Cabs showing lifestyle of the customer based on their behaviour |
| Confidence_Life_Style_Index | Category showing confidence on the index mentioned above |
| Destination_Type | Sigma Cabs divides any destination in one of the 14 categories |
| Customer_Rating | Average of life time ratings of the customer till date |
| Cancellation_Last_1Month | Number of trips cancelled by the customer in last 1 month |
| Var1, Var2 and Var3 | Continuous variables masked by the company. Can be used for modelling purposes |
| Gender | Gender of the customer |
| Surge_Pricing_Type | Target (can be of 3 types) |

## Brief Overview of the Files:
### 1. requirements.txt
Before running code locally please install dependancies from requirements.txt

### 2. research/sigma_cabs.ipynb
Main research file

### Metrics: classification report (precision, recall, f1-score and average across all classes using micro, macro and weighted avg)

### Results:
1. EDA
2. Fill in the gaps in real features with the median, and in categorical ones - with the most popular class
3. Processing categorical features(one-hot encoding)
4. Trained different models:
	- OneVsRestClassifier(LogisticRegression())
	- OneVsOneClassifier(SGDClassifier())
5. GridSearchCV() - search for optimal parameters (validate the parameters using accuracy)

As a result, it isn't possible to say unequivocally which approach was better: One-vs-Rest or One-vs-One. Each of them seems to have its pros and cons.




