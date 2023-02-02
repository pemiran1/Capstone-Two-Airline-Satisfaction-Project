![image](https://user-images.githubusercontent.com/110074006/216411185-623cf664-45d5-45cc-abaf-8af8aeb0f6d5.png)


# Predicting Airline Passanger Satisfaction 
The luxury of traveling is made of up the experience from taking a flight and getting to a destination. The part that is often not thought of is what if
there are delays, what seat will you be taking on the plane, or which airline will you be flying. With use of airline passanger satisfaction survey data, 
I will create a model to predict passanger satisfaction based on a number of metrics. 


## 1. The Data
Using Kaggle provided data, I analyzed an anonymous airline dataset. The metrics below from the dataset were analyzed: 

Gender: Gender of the passengers (Female, Male)
Customer Type: The customer type (Loyal customer, disloyal customer)
Age: The actual age of the passengers
Type of Travel: Purpose of the flight of the passengers (Personal Travel, Business Travel)
Class: Travel class in the plane of the passengers (Business, Eco, Eco Plus)
Flight distance: The flight distance of this journey
Inflight wifi service: Satisfaction level of the inflight wifi service (0:Not Applicable;1-5)
Departure/Arrival time convenient: Satisfaction level of Departure/Arrival time convenient
Ease of Online booking: Satisfaction level of online booking
Gate location: Satisfaction level of Gate location
Food and drink: Satisfaction level of Food and drink
Online boarding: Satisfaction level of online boarding
Seat comfort: Satisfaction level of Seat comfort
Inflight entertainment: Satisfaction level of inflight entertainment
On-board service: Satisfaction level of On-board service
Leg room service: Satisfaction level of Leg room service
Baggage handling: Satisfaction level of baggage handling
Check-in service: Satisfaction level of Check-in service
Inflight service: Satisfaction level of inflight service
Cleanliness: Satisfaction level of Cleanliness
Departure Delay in Minutes: Minutes delayed when departure
Arrival Delay in Minutes: Minutes delayed when Arrival
Satisfaction: Airline satisfaction level(Satisfaction, neutral or dissatisfaction)

The Dataset can be viewed with the link below: 

> * [Airline Dataset](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction)


## 2. Data Cleaning 

In this step, I cleaned the dataset by removing NaN values, and analyzing the type of data that was within each column. Since the dataset was based on a 
passanger survey there was data in numeric and string format. 

- Problem 1: The dataset had 310 missing vales, which were under the 'Arrival Delay in Minutes' column. Although this may be due there not being any 
delay upon arrival, these values were dropped from the dataset. 

- Problem 2: The dataset contained string data under columns: Gender, Customer Type, Type of Travel, and Class. The solution was to use the pd.get_dummies
function in order to convert them from categorical data into numerica. 


## 3. EDA
> * [EDA Step] (https://github.com/pemiran1/Capstone-Two-Airline-Satisfaction-Project/blob/main/airline-project.ipynb)

In this step a heatmap and other visualization graphs were used for comparison of the data. This step helped to identify which values were most important
to analyze, and which errors to fix. 

![Screen Shot 2023-02-02 at 11 47 19 AM](https://user-images.githubusercontent.com/110074006/216421136-0f7c9686-348e-4811-a146-70aecbfe830a.png)
![Screen Shot 2023-02-02 at 11 47 28 AM](https://user-images.githubusercontent.com/110074006/216421190-bda301fe-205a-46c7-8a88-75fa586d6d0a.png)
![Screen Shot 2023-02-02 at 11 47 37 AM](https://user-images.githubusercontent.com/110074006/216421200-c82f7cc9-740f-4ae1-aadf-74679f10f2d6.png)


## 4. Machine Learning 

> * [Machine Learning Step] (https://github.com/pemiran1/Capstone-Two-Airline-Satisfaction-Project/blob/main/(1)_Predicting_Airline_Passenger_Satisfaction_Modeling_(1).ipynb)

For this step I chose to work with Python's statsmodels and sklearn libraries for training the dataset. I tested the dataset with 3 ML algorithsm: 
Random Forest, LightGBM, and, KNNClassifier. 

If this modeling would go into production, it should be accounted that although LightGBM was the most accurate, it is also the most expensive to run. 

![Screen Shot 2023-02-02 at 11 55 15 AM](https://user-images.githubusercontent.com/110074006/216422606-974f30a4-27f6-4b30-9930-636fcab11c23.png)



## 5. Improvements 

- This predictive model could be improved by having additional filters for customer satisfaction based on other metrics included in the dataset. 

- Another improvement for further analysis could be to use more ML models such as decision trees, Naive Bayes, and/or Catboost.

