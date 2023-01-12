# SXSW - Twitter Sentiment Analysis

Author: Simran Kaur

![title](images/sxsw_logo.jpeg)

## Problem

South by Southwest ("SXSW") is a world premier event that showcases new music, films and interactive media. It takes place in Austin, Texas every year. Event coordinators have released an app called "SXSW GO" and it is the official app for getting the most out of the show if you are attending.

Festival directors have reached out to see what improvements can be made to the app so that it can be improved for this year's festival. They would also like to measure tweet sentiment after this year's festival.

Twitter tweets from last year's event will be used to observe overall app sentiment. This analysis will use Natural Language Processing ("NLP") to develop models that can determine how SXSW Go users feel about the app.

## Data

Data was taken from [data.world](https://data.world/crowdflower/brands-and-product-emotions). It contains approximately 4,600  tweets with the festival hashtag, the device it was shared from as well as if there is a positive, negative or neutral emotion tagged to the tweet.

## Methods

The notebook is broken down into two parts - EDA and modeling. 

In the EDA section, a lot of cleanup was performed on the tweets. Mentions, URLs, white spaces, punctuation marks and nonalphabetical characters were removed. An analysis was performed on tweet length and WordClouds were created. THe he most common hashtags were plotted on barcharts. Subsequently, an N-gram analysis was performed. Count vectorization was applied and the text was converted to numerical data. Finally, to address the class imbalance in the "emotion" column, SMOTE was applied. 

Five different model versions were ran, which included four different types of models. 
* First, a logistic regression model was ran. This served as the baseline model.
* Secondly, a Support Vector Classifier Model was ran. 
* Thirdly, the Complement Naive Bayes Classifier Model was ran. This model was used instead of the normal Naive Bayes as this one caters to class imbalances. 
* The fourth model ran was the Random Forest Classifier. 
* Finally, the model with the highest accuracy was hyperparameter tuned.

## Results

Accuracy and F1 score were used to compare the original four models ran. Accuracy is the best performance metric in this business case as it is the percentage of correct predictions for the test data. The original random forest classifier had the highest accuracy, at 65.4%. 

## Suggestions

1. **Improve how the app appears on iPhones.** IPad users had an overall positive and neutral experience whereas iPhone users had more of a negative experience.
2. **Make the app less crashy.** One of the common compliant negative tweet users had was that the app was "crashy". A couple of ways to prevent this is to ensure the app is simple and compatible with a lot of devices, including low-end ones. 
3. **Spend time on the android interface.** Google was the most common hashtag under neutral tweets and the hashtag andriod came up in all three common hashtag plots. This indicates there is room for improvement on the android interface. 

## Next Steps

The final model yielded an accuracy if 65.1%, which is a number that can possibly be better. Some ideas to better performance are as follows:
* Running the analysis with a larger population of tweets and narrowing down the number of neutral tweets in the population. 
* Tagging an initial emotion to the tweet should be done by a few people. This will allow the tagged emotion to be more likely correct. 
* Collecting more features for the next analysis. Some insightful variables are the device the tweet was made from, when the tweet was made and the information on the different reactions tweets got. 

## Further Information

See the full analysis in the [Jupyter Notebook](https://github.com/simrank3/phase-4-project/blob/main/notebook.ipynb) or review the [presentation](https://github.com/simrank3/phase-4-project/blob/main/presentation.pdf).

For additional information, contact Simran Kaur at simran.kaur@flatironschool.com

## Repository Structure
```
├── images
│   ├── sxsw_logo.jpeg
├── notebook.ipynb
├── presentation.pdf
├── README.md
└── tweet_data.csv