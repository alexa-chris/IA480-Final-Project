# Classifying Tweets Based on Sentiment Using Naive Bayes 
## Introduction
This project applied a RapidMiner function to collect tweets containing #BrettKavanaugh. These collected tweets were then used as data to apply Naïve Bayes to conduct a sentiment analysis on the tweets. #BrettKavanaugh was chosen because of the amount of discussion over Twitter on his Supreme Court nomination and the allegations of his sexual assault by multiple women. Brett Kavanaugh was nominated to the Supreme Court in July. Soon after he was accused of sexual assault. Discussion arose across the U.S. on this topic, especially during his confirmation hearings and testimonies. Kavanaugh was later appointed to the Supreme Court in early October. However, controversy over Kavanaugh is still discussed on Twitter as some continue to question his eligibility to serve as a Supreme Court justice. Therefore, using #BrettKavanaugh provided plenty of data. The ultimate goal of using collected tweets was to teach the machine to identify tweets based on whether they were positive (supporting Brett Kavanaugh’s confirmation to the Supreme Court), negative (opposing Brett Kavanaugh’s confirmation to the Supreme Court), or neutral (tweets that were not related to the Supreme Court nomination but referenced Kavanaugh in other contexts, or that were not positive or negative about Kavanaugh). 

## Data  
The data used was tweets containing the keyword #BrettKavanaugh. 1,600 tweets were collected in total. These tweets were collected into two different excel files so that ten percent of the tweets could be hand-classified for training data. There were 160 tweets collected for training data. A sentiment analysis was conducted by hand on these tweets, categorizing them as positive (supporting Brett Kavanaugh’s confirmation), negative (opposing Brett Kavanaugh’s confirmation), or neutral (tweets that were not related to the Supreme Court nomination but referenced Kavanaugh in other contexts, or that were not positive or negative about his confirmation). After the sentiment analysis, 81 tweets classified as positive, 45 tweets were classified as neutral, and 34 were classified as negative. These hand classified tweets were then used as training data for the Naïve Bayes model.

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
In this project, Naive Bayes was used. Naive Bayes was used due to its advantages for this type of research. Naive Bayes is often used in text analysis, including sentiment analysis, which made it a clear choice for this project. It also works very quickly and can handle large data sets relatively well which was important due to the sheer number of tweets collected. However, it can also be used without enormous data sets required for other processes, such as logistic regression, which allowed us to do it with smaller subsets of tweets once the tweets had been classified and filtered based on predicited sentiment. 2,000 tweets were collected so that there was a suffi

## Conclusion: 

### Insight From Data and Models

***Quantitative Visualization of Training Data***

![oflabelledtweetsintraining](https://user-images.githubusercontent.com/42848654/49690856-aebf9700-fb05-11e8-8672-7d3cd258796a.PNG)

Screenshot of bar graph created in Tableau showing how many tweets were labelled by hand as "positive", "negative", and "neutral" in the original set of tweets that were then used to train RapidMiner to predict which sentiment label to apply.

***Quantitative Visualization of Tweets Classified in RapidMiner***

![oflabelledtweetsinpostclassify](https://user-images.githubusercontent.com/42848654/49690911-59d05080-fb06-11e8-8816-88559bebc300.PNG)

Screenshot of bar graph created in Tableau showing how many tweets were labelled by RapidMiner. When the two graphs are compared, one can see that, proportionalty, the graphs are about the same. When RapidMiner was given access to the large amount of unlabelled tweets, it was able to label them in about the same proportion that they were hand labelled. This could be influenced by the high amount of retweets in the data set, so this correlation does not necessarily indicate accurate predictions. 

***Visualizations from Orignal Training Data/Collected Tweets***

![trainingdatawordcloud](https://user-images.githubusercontent.com/42848654/49689912-69e03400-faf6-11e8-9480-92c0bb5010f1.png)

Screenshot of wordcloud created in Voyant Tools showing relative word frequency of top 105 words in the original training data. Contains many of the same words in similar frequencies to the wordcloud created from final set of classified data.

![collectedtweetsfrequencies](https://user-images.githubusercontent.com/42848654/49689952-fa1e7900-faf6-11e8-8ccb-b9b65278240c.JPG)

Screenshot from Voyant Tools of chart showing relative frequencies of most common words found in original tweets collected

***Visualizations from Tweets Classified in RapidMiner***

![alltweetswordcloud](https://user-images.githubusercontent.com/42848654/49689981-87fa6400-faf7-11e8-8ad2-88b2059ccc4b.png)

Screenshot of wordcloud created in Voyant Tools showings relaetive frequency of top 105 words in the data set of tweets that had predictied sentiment labels applied to them by RapidMiner

![alltweetsfrequencies](https://user-images.githubusercontent.com/42848654/49689996-c7c14b80-faf7-11e8-8781-f2407a78f8b6.JPG)

Screenshot of a chart created in Voyant Tools showing frequency of most used words in the entire set of collected tweets. When compared to the frequency chart from the training data, it becomes apparent that, while there is cross-over between some of the words, there are different words as well. There is also a similarity between the patterns in the charts, indicating proporitonal similarities between the two. Another interesting observation is that some of the patterns between the two are similar despite them being differnt words, such as the similarty in shape between the the lines for "anonymous" in the first and "kavanaugh" in the second

***Visualizations of "Positive" Labelled Tweet Data***

![positivetweetwordcloud](https://user-images.githubusercontent.com/42848654/49690119-934e8f00-faf9-11e8-9e31-0ca97c931bc5.png)

Screenshot of wordcloud showing relative frequency of top 105 words created out of only the tweets that RapidMiner had labelled as posessing a "positive" sentiment. The difference between this and the wordcloud from all the tweets becomes immediately apparent.

![positivegraph](https://user-images.githubusercontent.com/42848654/49690161-27205b00-fafa-11e8-9f2b-065ce03670be.PNG)

Screenshot of the chart created showing relative frequencies of the top 5 words in the tweets labelled by RapidMiner as "positive". 

***Visualizations of "Negative" Labelled Tweet Data***

![negativetweetwordcloud](https://user-images.githubusercontent.com/42848654/49690264-e295bf00-fafb-11e8-9de1-39cda942014c.png)

Screenshot of wordcloud showing relative frequency of top 105 words in the tweets assigned a "negative" sentiment by RapidMiner

![negativeschart](https://user-images.githubusercontent.com/42848654/49690310-ab73dd80-fafc-11e8-8260-e593681abffa.PNG)

Screenshot of chart showing frequencies of the top 5 words in tweets assigned a "negative" sentiment in RapidMiner. When compared to the positvely labelled tweet chart, one can see that the top 4 "words" in each are the same, while in the first chart contains "democrats" in high frequency while the second contains "metoo in high frequency.

***Visualizations from "Neutral" Labelled Tweet Data***

![neutralwordcloud](https://user-images.githubusercontent.com/42848654/49690451-52597900-faff-11e8-89f9-31b0ce94ca3b.png)

Screenshot of wordcloud showing frequency of top 105 terms using only the tweets labelled as a "neutral" sentiment by RapidMiner

![neutraltweetgraph](https://user-images.githubusercontent.com/42848654/49690463-71f0a180-faff-11e8-8a21-712d02790f55.PNG)

Screenshot of graph showing relative frequency of top 5 terms appearing in tweets RapidMiner judged to have a "neutral" sentiment. When compared to both the "positive" and "negative" charts discuessed previously, the differences are immense. Not only is there only one common term between the three ("brettkavanaugh"), but the pattern of the frequency in which the other top four terms appear is entirely differnt than the other two. 

***Visualizations from Tweets Filtered To Remove Retweets***

![nortwordcloud](https://user-images.githubusercontent.com/42848654/49690574-42db2f80-fb01-11e8-85be-807f01c4ccad.png)

Screenshot of wordcloud created after all the labelled tweets were subjected to an additonal filter in which all tweets containing the term "RT", denoting a "Retweet", were filtered out and then written into a new excel file. This allowed analysis to be performed on only unique, individual tweets. 

![nortgraph](https://user-images.githubusercontent.com/42848654/49690649-5dfa6f00-fb02-11e8-9a3e-699d229fe194.PNG)

Screenshot of chart created showing relative frequency of top 5 terms appearing in tweets after they had been filtered again to remove all retweets. Since this chart was formed using data containing "positive", "negative", and "neutral" labels, it makes sense to compare it to the chart from the full set of classified tweets. When one does this, they can observe the differences. They only have one term in common ("brettkavanugh") and the patterns in which the other top terms appear is different. In the No-RT graph, there is a clear divide between the apperances of the top 3 words and the top two words, a divide that does not exist in the chart pertaining to all the classified tweets. 

## Findings
The machine was ran more than once to filter out retweets (RTs) after the first run. The accuracy after the first run was 92.50% and the kappa was 0.900. Filtering out RTs was simply used as a test to identify whether or not the accuracy would improve after doing so. Filtering out RTs improved the accuracy to 97.50% and the kappa rose to 0.966. This is likely the result of overfitting as filtering out retweets provided less training and testing data overall. In this case, overfitting likely occurred because the model was too complex for the amount of data present. The Kappa in both cases is very close to one and unrealistically high. This again may be the result of having too complex a model for the amount of data present. 

### Limitations of Research
***Sentiment Analysis***
One limitation of this research comes from the biases when conducting the sentiment analysis for the training data. First, the tweets were classified by hand based on perceived sentiment. However, considering Twitter is an online platform that contains various kinds of opinions, including satirical ones that would not easily be understood without understanding the goals of the author of the Tweet, there is plenty of room for human error. Although there was an attempt to conduct as much research on the Twitter authors as possible, there were still some difficulties in how to best classify certain tweets. Second, words that do not necessarily carry a positive or negative sentiment in them are present in many of the tweets. Instead, the sentiment comes from the overall statement. Thus, some words are going to be present in the positive, negative, and overall statements. This may skew the results as the machine attempts to learn. Finally, the way the tweets were classified contained inherent biases. Classifying the support of Brett Kavanaugh’s position on the Supreme Court is biased in that not everyone believes that supporting him is positive and vice versa. Thus, inherent biases were imparted on the data and the model as it learned from the hand-classified training data.  
***Images and Links***
Many of the tweets collected contained images and links that portrayed Kavanaugh in certain ways. However, RapidMiner does not look at the content of these images and links, it only takes the content from the tweet itself. Thus it does not understand the sentiment of these tweets. We chose to classify these tweets as neutral, however the actual content of the tweet (the image or link) may not have been neutral. 
***Suggestions for Improvement***
***Filtering out Images and Links***
One way to improve this model would be to filter out any tweets that contained images or links so that they would not be used as training data. One way this could have been done is by classifying these tweets as image or link if they contained them. This would help the model learn while also removing them from the neutral category. Thus tweets that actually contained neutral content rather than just links or images would have been provided for the model. This would have improved how the model understood and categorized neutral content, as well as content with links and images.  The tweets also could have been classified into more neutral categories. The words “positive” and “negative” carry certain connotations with them. One more content-neutral way of doing so would be to classify them as “supportive”, “unsupportive”, and “neutral”. This would hopefully remove some of the inherent biases imparted on the data.  Another way to improve this model would be to have more tweets for both training and testing.
 

