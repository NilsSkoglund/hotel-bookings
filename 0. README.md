# hotel-bookings

### Data 
Original data was 119k rows with 32 features. Data was messy, lots of duplicated rows. After cleaning ~80k rows remained. 

### Target variable
Target variable was whether or not the booking was canceled. ~37% of all bookings were canceled in dataset

# Summary
Supervised classification ML project predicting if a booking will be canceled or not. In this project I was mainly focused on building a reasonable made up business use case incorporating predictions made by the model. The models "original" predictions were not useful in this made up business case, however if you only used predictions made by the model with 0.9 or higher probability score then the models predictions could be used as a key component in a profitable strategy. 

For more details about the business use case, please see the presentation available in the repo.

# Description of Pipeline

### Preprocessing pipeline

Numeric features: 
- StandardScaler()
- SimpleImputer()

Categorical features: 
- SimpleImputer()
- OneHotEncoder()

### Model Selection

Performance was assessed for the following classification models:
- SVC()
- DecisionTreeClassifier()
- RandomForestClassifier()
- LogisticRegression()
- KNN()
- GaussianNB()

using 5-fold cross-validation

RandomForestClassifier() had the best performance. 

### Hyperparameter tuning
Default settings had the best performance. Evaluated in GridSearch with 5-fold cross-validation.

# Project flaws
### Bad data-cleaning
I rushed the data-cleaning, then went on to modelling and used the models performace to build a story for the business use case. I later discovered the flaws of my data-cleaning and did a second iteration of data-cleaning. The models performance would with a high probability be significantly different if I used the data that had been cleaned properly and the business use case would break or at least have to be modified. I never ran the model with the properly cleaned data as the learning prospects of running another iteration of this does not attract me. However, lesson learned; don't rush through the data-cleaning!

### Lack of structure and clarity in feature selection
The feature selection was not straightforward. Some features had to be eliminated because they kept information that the model wouldn't have in a real world setting. Other features were causing problems when training the model and I excluded them on the basis that they did not add much explanatory value and caused problems. This process of excluding features was made in the same notebook where I did model-selection, hyperparameter tuning and evaluation of results. It was efficient in the short term to do this ongoingly in the same notebook and try out what seemed to be causing problems etc. but in the long term this causes problems. The code is not easily followed by a new reader and even for me it will take a considerable effort to understand the code if I get back to this project after some time. Lesson learned; really put an effort into making the code and thought process clear. 

# Project status
Finished project. There are lots of things that could be improved, especially for the two areas mentioned under project flaws. However the main purpose of this project was to build a business use case incorporating a machine learning models predictions and in that regard I am very happy with the project. I've learned a lot and feel I have managed to get close to real world situations and experience. 
