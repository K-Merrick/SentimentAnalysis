# SentimentAnalysis
Create model to classify reviews as positive or negative.

In creating a new and edgy community for classical movie enthusiasts, the Film Junky Union is hoping to develop a system for filtering and categorizing movie reviews. As part of the team, our job is to develop a model that automatically detects negative reviews. In building a model for classifying positive and negative reviews, we will be using a dataset containing IMDB movie reviews with polarity labelling. The measure of an adquate model will be one which has an F1 score of no less than .85.

**Summary**: The aim of this project was to develop an NLP machine learning model that can classify movie reviews according to whether they are positive or negative with an F1 score of no less than .85. In carrying out this task, we first preprocessed our data, which included removing all but letters and apostrophes from each review. We then carried out exploratory data analysis, with one of the main goals being to ensure that classes are balanced between testing and training datasets; in doing so, we found that there are nearly an equal number of positive and negative reviews in the dataset, as well as that there is a roughly equal distribution of movie ratings in each dataset. Next, we built and tested a number of neural networks, each of which involved some sort of lemmatization and tokenization process (except for the dummy model). The models we built may be characterized as follows:

    Model 1: Dummy Classifier
    Model 2: NLTK + TF-IDF + Logistic Regression
    Model 3: spaCy + TF-IDF + Logistic Regression
    Model 4: spaCy + TF-IDF + LGBMClassifier
    Model 5: BERT + Logistic Regression

In general, the lower numbered models were far quicker to train and obtain predictions from than the higher numbered ones, with Model 5 taking the longest, which is largely due to the CPU/GPU intensive embedding process. Given this fact, we expected that each subsequent model would perform better than the previous one; however, this was not the case. Rather, we found Model 2 to provide the highest scores overall and models 4 and 5 to provide the lowest. The F1 scores for each model on the testing datasets are as follows:

    Model 1: .5
    Model 2: .88
    Model 3: .87
    Model 4: .85
    Model 5: .86
