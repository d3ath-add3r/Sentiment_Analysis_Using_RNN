# Sentiment_Analysis_Using_RNN
This repository contains google colab notebook developed over visualization, data preprocessing and Recurrent Neural Network model building to predict the sentiment of a tweet.

## **About the dataset :**
The Social Dilemma, a documentary-drama hybrid explores the dangerous human impact of social 
networking, with tech experts sounding the alarm on their own creations as the tech experts 
sound the alarm on the dangerous human impact of social networking. This dataset brings you the 
twitter responses made with the #TheSocialDilemma hashtag after watching the eye-opening 
documentary "The Social Dilemma" released in an OTT platform(Netflix) on September 9th, 2020.

**Attribute Information:**
1. user_name - The name of the user, as they’ve defined it.
2. user_location - The user-defined location for this account’s profile.
3. user_description - The user-defined UTF-8 string describing their account.
4. user_created - Time and date, when the account was created.
5. user_followers - The number of followers an account currently has.
6. user_friends – The number of friends an account currently has.
7. user_favourites - The number of favorites an account currently has.
8. user_verified - When true, indicates that the user has a verified account.
9. date - UTC time and date when the Tweet was created.
10. hashtags - All the other hashtags posted in the tweet along with #TheSocialDilemma
11. source - Utility used to post the Tweet, Tweets from the Twitter website have a source 
value – web
12. is_retweet - Indicates whether this Tweet has been Retweeted by the authenticating user.
13. clean_text – Cleaned text of the tweet.
14. Sentiment (target) - Indicates the sentiment of the tweet, consists of three categories: 
Positive, neutral, and negative.

**About the model**

Model: "sequential_1"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
text_vectorization_1 (TextVe (None, None)              0         
_________________________________________________________________
embedding_1 (Embedding)      (None, None, 64)          128000    
_________________________________________________________________
simple_rnn_1 (SimpleRNN)     (None, 64)                8256      
_________________________________________________________________
dense_2 (Dense)              (None, 64)                4160      
_________________________________________________________________
dense_3 (Dense)              (None, 3)                 195       
=================================================================

Total params: 140,611
Trainable params: 140,611
Non-trainable params: 0

The input for the model is from encoder which encodes the text tweet into machine understandable data.

**Training and Validation Accuracy and Loss curves:**
![image](https://user-images.githubusercontent.com/84405967/157660762-a49d2d5b-3291-43d5-a5ce-1db901553104.png)
The curves are pretty smooth and model is good.

The accuracy of the RNN model : 86.17 % 
