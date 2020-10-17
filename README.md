# hotel-bookings
Supervised classification ML project predicting if a booking will be canceled or not


# Description 

## Data 
Original data was 119k rows with 32 features. Data was messy, lots of duplicated rows. After cleaning ~80k rows remained. 

## Target variable
Target variable was whether or not the booking was canceled. ~37% of all bookings were canceled in dataset

## Preprocessing pipeline

Numeric features: 
- StandardScaler()
- SimpleImputer()

Categorical features: 
- SimpleImputer()
- OneHotEncoder()

## Model Selection

Performance was assessed for the following classification models:
- SVC()
- DecisionTreeClassifier()
- RandomForestClassifier()
- LogisticRegression()
- KNN()
- GaussianNB()

using 5-fold cross-validation

RandomForestClassifier() had the best performance. 

## Hyperparameter tuning
Default settings had the best performance. Evaluated in GridSearch with 5-fold cross-validation.
