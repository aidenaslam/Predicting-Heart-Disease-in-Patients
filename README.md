# Classifying Heart Disease in Patients

The Framingham Heart Study is a long-term, ongoing cardiovascular cohort study of residents of the city of Framingham, Massachusetts. The study began in 1948 with 5,209 adult subjects from Framingham and is now on its fourth generation of participants. The Framingham Heart Study is now considered one of the longest, most important epidemiological studies in medical history. Cardiovascular diseases (CVDs) are the number one cause of death globally and in 2016 they represented 31% of all global deaths. CVDs include coronary heart disease (CHD), cerebrovascular disease and rheumatic heart disease to name a few. In this study, the aim is to use the Framingham Heart Study data in order to accurately classify whether a participant has developed CHD over the ten-year period of the study. Various machine learnings are implemented to identify the best model. The analysis was carried out using jupyter notebook which can be found in the uploaded zip file. 

## Exploratory Data Analysis (EDA)
* The box-and-whisker plot showed potential outlier values in many features however, the values were found to be correct and not due to instrument or reporting error.
<img src="https://github.com/aidenaslam/Predicting-Heart-Disease-in-Patients/blob/master/Figure%201.png" width="650" height="400" />

* The histogram distribution of each feature shows that the numerical features are apporoximately normally distributed, with the exception of *cigsperday*
<img src="https://github.com/aidenaslam/Predicting-Heart-Disease-in-Patients/blob/master/Figure%202.png" width="650" height="400" />

* There is a strong positive correlation between whether a person is a smoker and the number of cigarettes they smoke per day (0.77). There is also a strong positive correlation between whether a person has diabetes and their glucose level (0.62). Likewise for sysBP and dialBP there is a correlation of 0.78 between these attributes. These high correlation values indicate that not all the attributes will be required for modelling and thus as part of the data preparation stage, some attributes will not be selected.
<img src="https://github.com/aidenaslam/Predicting-Heart-Disease-in-Patients/blob/master/Figure%203.png" width="650" height="400" />

## Data Preparation
* Missing data was removed, given the time frame of the project - in the future imputation techniques would be an improved method

* Feature selection was carried out using Chi Squared method and the top-10 features were selected for modelling.
<img src="https://github.com/aidenaslam/Predicting-Heart-Disease-in-Patients/blob/master/Figure%204.png" width="150" height="300" />

## Modelling Results
* Three machine learning algorithms were considered: logistic regression, decision tree (with and without pruning) and neural network.

* K-fold cross validation accuracy and AUC were selected as the evaluation criteria

* The best model was the decision tree with pruning.
<img src="https://github.com/aidenaslam/Predicting-Heart-Disease-in-Patients/blob/master/Figure%205.png" width="300" height="100" />

## Limitations and Future Work
* Although many algorithms were used for this dataset and their parameters fine-tuned, further work would include applying sampling techniques to overcome the issue for class imbalances. Class imbalance was only used for logistic regression.

* Furthermore, no validation set was used due to the small dataset size. In the future, more data can be supplied, and a validation set can be used to evaluate the models. 

* Although decision trees performed well, they can be further improved using ensemble methods. 


## References 
[1] https://www.kaggle.com/amanajmera1/framingham-heart-study-dataset/data
