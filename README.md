# Estimation of number of retweets for tweets during demonetzation in India

This work describes how clustering and NLP together can be used to design an efficient multi-label classifer. The problem statement is to predict the number of retweets for tweets during demonetization phase in India. Demonetization was an exercise by the government of India in 2016 aimed at curbing corruption. 
The data set consists of 14000 tweets along with other attributes like time of tweet, date of tweet, retweet count etc. I attempted to predict the approximate number of retweets for a given tweet. 
To begin with, K-means was applied on the retweet counts to divide them into 4 clusters, each representing a range of retweet count. Each tweet,based on their retweet count, was represented by one of the four clusters. 
This smart grouping (K-Means clustering) brought together the tweets that have similar potential of generating retweets.
As a result, the tweets in a cluster had high correlation. This correlation (within a cluster of tweets) would make it easier for an LSTM model to classify the tweets into the four clusters which would inturn, improve the efficiency of the prediction. 
The right number of K-Means clusters can be calculated using k-elbow method. In this code I had set the number of clusters as 4. 
The dataset can be obtained from the following location -
https://www.kaggle.com/arathee2/demonetization-in-india-twitter-data
