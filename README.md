# Classifying Tweets Based on Sentiment Using Naive Bayes 
## Introduction
This project used a RapidMiner function to collect tweets containing #BrettKavanuagh. These collected tweets were then used as data to use Naïve Bayes to conduct a sentiment analysis on the twitter. #BrettKavanaugh was chosen because of the amount of discussion over Twitter on his Supreme Court nomination and the allegations of his sexual assault by multiple women. Brett Kavanaugh was nominated to the Supreme Court in July. Soon after he was accused of sexual assault. Discussion arose across the U.S. on this topic, especially during his confirmation hearings and testimonies. Kavanaugh was later appointed to the Supreme Court in early October. However, controversy over Kavanaugh is still discussed on Twitter as some continue to question his eligibility to serve as a Supreme Court justice. The ultimate goal of using collected tweets was to teach the machine to identify tweets based on whether they were positive (supporting Brett Kavanaugh’s confirmation to the Supreme Court), negative (opposing Brett Kavanaugh’s confirmation to the Supreme Court), or neutral (tweets that were not related to the Supreme Court nomination but referenced Kavanaugh in other contexts, or that were not positive or negative about Kavanaugh). 

## Data 
The data used was tweets containing the keyword #BrettKavanaugh. 1,500 tweets were collected in total. These tweets were collected into two different excel files so that ten percent of the tweets could be hand-classified for training data. There were 160 tweets collected for training data. A sentiment analysis was conducted by hand on these tweets, categorizing them as positive (supporting Brett Kavanaugh’s confirmation), negative (opposing Brett Kavanaugh’s confirmation), or neutral (tweets that were not related to the Supreme Court nomination but referenced Kavanaugh in other contexts, or that were not positive or negative about his confirmation). After the sentiment analysis, 81 tweets classified as positive, 45 tweets were classified as neutral, and 34 were classified as negative. These hand classified tweets were then used as training data for the Naïve Bayes model.





 
## Process
***RapidMiner Process: Collecting Twitter Data***

![tweetcollection](https://user-images.githubusercontent.com/42848654/49676828-6d69b180-fa49-11e8-875f-cc0da4b9ad35.png)
RapidMiner process used to collect tweets

***Process: Classifying Twitter Data*** 

![handlabelledexcel](https://user-images.githubusercontent.com/42848654/49676845-82464500-fa49-11e8-8a4d-54bdbb28d73b.JPG)
Excel file in which tweets were hand-labelled by according to sentiment (positive, negative, neutral) 

***RapidMiner Process: Process Data***

![collect_tweet_process 1](https://user-images.githubusercontent.com/42848654/49676887-c3d6f000-fa49-11e8-92b3-129c3f0933ff.png)
RapidMiner process used to convert excel file into usable data in RapidMiner then store said data to be used for training and testing models

***RapidMiner Process: Training and Testing***

![finalprocess](https://user-images.githubusercontent.com/42848654/49677019-7e66f280-fa4a-11e8-8636-019b132dbf9d.png)
RapidMiner process used to import the tweet data and then use this data to train the program to predict which sentiment label will be applied to each tweet based on content and then write this into a new excel file

***Justification of Model and Process*** 
In this project, Naive Bayes was used. Naive Bayes was used due to its advantages for this type of research. Naive Bayes is often used in text analysis, including sentiment analysis, which made it a clear choice for this project. It also works very quickly and can handle large data sets relatively well which was important due to the sheer number of tweets collected. However, it can also be used without enourmous data sets required for other processes, such as logistic regression, which allowed us to do it with smaller subsets of tweets once the tweets had been classified and filtered based on predicited sentiment. 2,000 tweets were collected so that there was a suffi


## Conclusion: 
### Insight From Data and Models



### Limitations of Research
***Sentiment Analysis***
One limitation of this research comes from in the biases when conducting the senitment analysis for the training data. First, we classified the Tweets based on the sentiments we believed they portrayed. However, considering Twitter is an online platform that contains various kinds of opinions, including satirical ones that would not easily be understood without understanding the goals of the author of the Tweet, there is plenty of room for human error. While we attempted to conduct as much research on the Twitter authors as possible, there were still some difficulties in how to best classify certain tweets. Second, words that do not necessarily carry a positive or negative sentiment in them are present in many of the tweets. Instead, the sentiment comes from the overall statement. Thus, some words are going to be present in the positive, negative, and overall statements. This may skew the results as the machine attempts to learn. 
***Images and Links***
Many of the tweets collected contained images and links that portrayed Kavanaugh in certain ways. However, RapidMiner does not look at the content of these images and links, it only takes the content from the tweet itself. Thus it does not understand the sentiment of these tweets. We chose to classify these tweets as neutral, however the actual content of the tweet (the image or link) may not have been neutral. 
***Filtering out RTs and Links***
One way to improve this model would be to filter out any tweets that contained images or links so that they would not be used as training data. One way this could have been done is by classifying these tweets as image or link if they contained them. This would help the model learn while also removing them from the neutral category. Thus tweets that actually contained neutral content rather than just links or images. 

***Suggestions for Improvement*** 

