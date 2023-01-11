# Twitter Sentiment Analysis
__________________________________________________________________________________________________________________________________
Author: Simran Kaur

![title](images/twitter_logo.jpeg)

## Problem

Twitter's CEO, Elon Musk, wants to add emojis, users can click, as responses to tweets. Currently there are no emojis available, only the option to "heart" a tweet. He wants to understand the overall sentiments of tweets users share, to determine which emojis would be best to add.

This analysis will use Natural Language Processing ("NLP") to understand overall tweet sentiment.

## Data

Data was taken from [data.world](https://data.world/crowdflower/brands-and-product-emotions). It contains over 9,000 different tweets with the device it was shared from as well as if there is a positive, negative or neutral emotion to the tweet.

## Methods

The notebook is broken down into two parts - EDA and modeling. 

In the EDA section, a lot of cleanup was performed on the tweets. Mentions, URLs, white spaces, punctuation marks and nonalphabetical characters were removed. An analysis was performed on tweet length and WordClouds were created. Subsequently, an N-gram analysis was performed. Count vectorization was applied and the text was converted to numerical data. Finally, to address the class imbalance in the "emotion" column, SMOTE was applied. 

Five different model versions were ran, which included four different types of models. 
* First, a logistic regression model was ran. This served as the baseline model.
* Secondly, a Support Vector Classifier Model was ran. 
* Thirdly, the Complement Naive Bayes Classifier Model was ran. This model was used instead of the normal Naive Bayes as this one caters to class imbalances. 
* The fourth model ran was the Random Forest Classifier. 
* Finally, the model with the highest accuracy was hyperparameter tuned.

## Results

Accuracy and F1 score were used to compare the original four models ran. Accuracy is the best performance metric in this business case as it is the percentage of correct predictions for the test data. The original random forest classifier had the highest accuracy, at 68.8%. 

## Suggestions

1. Twitter should implement a thumbs up and a thumbs down emoji as responses to tweets. These are basic emojis that people are very likely to use. 
2. Twitter should also keep their heart emoji as it has been around for a long time and users are familiar with it. Familiarity is directly tied to comfort. 

## Next Steps

The final model yielded an accuracy if 68.8%, which is a number that can possibly be better. Some ideas to better performance are as follows:
* Running the analysis with a different population of tweets and narrowing down the number of neutral tweets in the population. 
* Factoring in major events that may be taking place. Tweets tend to focus on events and as seen above, the data was surrounded around SXSW. 
* Tagging an initial emotion to the tweet should be done by a few people. This will allow the tagged emotion to be more likely correct. 

## Further Information

## Repository Structure
├── images
│   ├── twitter_logo.jpeg
├── notebook.ipynb
├── presentation.pdf
├── README.md
└── tweet_data.csv
