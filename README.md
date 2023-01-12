# SXSW - Twitter Sentiment Analysis

Author: Simran Kaur

![title](images/sxsw_logo.jpeg)

## Problem

South by Southwest ("SXSW") is a world premier event that showcases new music, films and interactive media. It takes place in Austin, Texas every year.

Festival directors have reached out to see what improvements can be made from this year's festival so that it can be improved for next year.

This analysis will use Natural Language Processing ("NLP") to develop models that can determine Twitter tweet sentiments. Tweets from this year's festival will be used to observe sentiment.

## Data

Data was taken from [data.world](https://data.world/crowdflower/brands-and-product-emotions). It contains approximately 4,600  tweets, with the festival hashtag, with the device it was shared from as well as if there is a positive, negative or neutral emotion to the tweet.

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

Accuracy and F1 score were used to compare the original four models ran. Accuracy is the best performance metric in this business case as it is the percentage of correct predictions for the test data. The original random forest classifier had the highest accuracy, at 65.4%. 

## Suggestions

 

## Next Steps



## Further Information

See the full analysis in the [Jupyter Notebook](https://github.com/simrank3/phase-4-project/blob/main/notebook.ipynb) or review the [presentation](https://github.com/simrank3/phase-4-project/blob/main/presentation.pdf).

For additional information, contact Simran Kaur at simran.kaur@flatironschool.com


## Repository Structure
```
├── images
│   ├── twitter_logo.jpeg.jpeg
├── notebook.ipynb
├── presentation.pdf
├── README.md
└── tweet_data.csv
