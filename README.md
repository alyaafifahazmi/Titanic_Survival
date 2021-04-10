# Titanic_Survival: Project Overview
Kaggle Titanic Prediction

Source: Kaggle Competition - [Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic/data)

## Data Dictionary
1. Survival: 0 = No, 1 = Yes
2. Pclass: Ticket class, 1 = 1st class, 2 = 2nd class, 3 = 3rd class
3. Sex: Male, Female
4. Age: Age in years
5. SibSp: Number of siblings/spouses aboard the Titanic
6. ParCh: Number of parents/children aboard the Titanic
7. Ticket: Ticket number
8. Fare: Passenger fare
9. Cabin: Cabin number
10. Embarked: Porf of embarkation, C = Cherbourg, Q = Queenstown, S = Southampton

## Data Exploratory

### Sketch Ideas

1. Use info() and describe() to get overview of the data
2. Check out if separating the attributes following numerical data or categorical will be helpful.
      - Considering to use standard scaler for numerical data
      - Considering to use OneHotEncoder or get_dummies for categorical data
3. Will combining train and test data be helpful?
4. Filling in NULL values with mean/median
5. Explore the survival rate following gender

### Understanding train data

![heatmap](https://github.com/alyaafifahazmi/Titanic_Survival/blob/main/heatmap_titanic.png)

Heatmap correlation to see correlation between attributes
      - Surviving rate is higher following passenger fare (Fare) and ticket class (Pclass)

![age](https://github.com/alyaafifahazmi/Titanic_Survival/blob/main/age.png)

Bar plot grapy of passengers' age. 
The median age of the passengers is 28 years old. 

![sex](https://github.com/alyaafifahazmi/Titanic_Survival/blob/main/sex.png)

Number of passengers survived and not survived.

% of women survived: 74.2

% of men who survived: 18.89

![sex_pclass](https://github.com/alyaafifahazmi/Titanic_Survival/blob/main/sex_pclass.png)

Survival graph following sex and Pclass.
You are more likey to survive if you were a female in the 1st class. 

![cabinclass](https://github.com/alyaafifahazmi/Titanic_Survival/blob/main/cabinclass.png)
![sex_cabinclass](https://github.com/alyaafifahazmi/Titanic_Survival/blob/main/sex_cabinclass.png)

From sex and cabin class graph, female and male from cabin C have higher chance of **not** surviving compared to other cabins.

We may need to look out at the layout of Titanic to know the location for cabin C. Cabin C most probably has a long pathway to emergency exit.

But after looking at cabin class graph, cabin C has most passengers when compare to other cabins.

The congestion of people to go to exit may influence the number of survivals.


### Data with NULL values

Train data and test data are combined. 
Total 1309 entries. 

1. Age: 263 nulls
      -> Use median value as mostly are 28 years old

2. Fare: 1 null 
      -> The missing fare is from Mr. Thomas Storey from 3rd class. 
      -> Fill in the null with the median fare from 3rd class.

3. Cabin: 1014 null

![cabinclass_pclass](https://github.com/alyaafifahazmi/Titanic_Survival/blob/main/cabinclass_pclass.png)

-> Many 1st class passenger were staying in cabin class B and C. 
-> Filling in 1014 nulls with assumptions may cause biased results. 
-> It's best to leave the attributes to train the data. 

4. Embarked: 2 null


## Model Building

Use Random Forest Classifier

(WIP: to compare with other model)

## Model Performance
Accuracy Score: 0.83 (by only using train data and split it with train_test_split)

(WIP: To combine train and test data)
