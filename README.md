# Correlation via clustering 
Read me
This work shows how clustering can contribute towards Natural Language Processing. The problem statement for the said purpose is to predict the number of retweets for tweets during demonetization in India. Domentization was an exercise by the government of India in 2016 aimed at curbing corruption. 
The data set consists of 14000 tweets along with other attributes like time of tweet, date of tweet, retweet count etc. I attempted to predict the approximate number of retweets for a given tweet. 
To begin with, K-means was applied on the number of retweets attribute to divided the retweet counts into 4 clusters, each representing a range of retweet count. Each tweet based on their retweet count was present in one of the four clusters. 
This smart grouping (K-Means clustering) brought together the tweets that have similar potential of generating retweets.
As a result, the tweets in a cluster will have high correlation. This correlation (within a cluster of tweets) would make it easier for an LSTM model to classify the tweets into the four clusters which would inturn, improve the efficiency of forecast. 
The right number of K-Means clusters can be calculated using elbow method. In this code I had set the number if clusters as 4. 
