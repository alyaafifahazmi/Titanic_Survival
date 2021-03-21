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
1. Use info() and describe() to get overview of the data
2. Check out if separating the attributes following numerical data or categorical will be helpful.
      - Considering to use standard scaler for numerical data
      - Considering to use OneHotEncoder or get_dummies for categorical data
3. Will combining train and test data be helpful?
4. Filling in NULL values with mean/median
5. Explore the survival rate following gender
6. Use heatmap correlation to see correlation between attributes
      - Surviving rate is higher following passenger fare (Fare) and ticket class (Pclass)
![heatmap](https://github.com/alyaafifahazmi/Titanic_Survival/blob/main/heatmap_titanic.png)

## Model Building

Use Random Forest Classifier
(WIP: to compare with other model)

## Model Performance
Accuracy Score: 0.83 (by only using train data and split it with train_test_split)
(WIP: To combine train and test data)
