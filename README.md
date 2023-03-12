# EECS-6893-final-project

- The Myers-Briggs Type Indicator (MBTI) is an introspective self-report questionnaire that indicates different psychological preferences in how people perceive the world and make decisions. Knowing MBTI can help users understand themselves and adjust the life and work according to their own personality tendencies.  
- This project provide a simple system to make predictions of Twitter user’s MBTI personality. The input of the system is user’s twitter name, and the system should return MBTI personality type predicted based on the user's tweets.
Compared to the traditional way of filling out questionnaires, we using social platform data to train classification model and make prediction. We also build a user-friendly web application which let users get their personality type result faster and easier.


[![demo](https://github.com/Larry-Wendy/MBTI_classification/blob/main/coverpage.png)](https://youtu.be/aFgrYO8kDU4 "demo")

__Dataset:__  
This is a dataset that contains 106K records of preprocessed posts online from the PersonalityCafe forum and Reddit. Where each post is 500 words long and has been annotated with personality type. The dataset was covered by Dylan Storey and Mitchell Jolly. The dataset has a volume of 346MB. The velocity of the dataset is 0 since it stopped updating. There are a total of 16 personalities included. The original dataset has an unbalanced distribution of personality. Therefore, we have used an oversample to balance the dataset and made each personality have 25K entries.

__Analytics:__    
Two parts of this project's data are preprocessed in different ways  
For Twitter API streaming data: 
1. Filte punctuation, stopwords, and emoji from the original data
2. Implement lemmatization to convert the format of text to the normal state
3. Reconstructure the text into equal size chunks (500 words)
For the MBTI dataset:
1. Oversampling through Synthetic Minority Oversampling Technique (SMOTE) due to imbalanced data distribution

__Machine learning algorithms:__
1. Naive Bayes-BernoulliNB
2. Naive Bayes-ComplementNB
3. Logistic Regression
4. K-Nearest Neighbors algorithm (KNN)
5. Random Forest

__System Modules:__  
The system is designed in several parts. The dataset comes from Kaggle and is a trained NLP model in GCP Dataproc. The Web application is set up on a GCP virtual machine and it requests the streaming data from API provided by Twitter. The visualization figures and predict results are displayed to the User on the web. The User should enter their Twitter User Id to get these results.

__Visualization:__  
1. The prediction result of the User's personality
2. Some famous people have the same personality
3. Some Job recommendations for this type of personality
4. Word Cloud visualization for most commonly used words
5. Model visualization figures
