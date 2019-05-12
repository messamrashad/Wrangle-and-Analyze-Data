# Wrangle-and-Analyze-Data
Data Analyst Nanodegree - Udacity

### Introduction
The purpose of this project is use what I learned in data wrangling lesson from Udacity Data Analysis Nanodegree program. The dataset which will be wrangled is the tweets archive of Twitter user @dog_rates, also known as WeRateDogs. 

WeRateDogs downloaded their Twitter archive and sent it to Udacity via email exclusively for us to use in this project. This archive contains basic tweet data (tweet ID, timestamp, text, etc.) for all 5000+ of their tweets as they stood on August 1, 2017. 

The goal of this project is to wrangle the WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations. The challenge lies in the fact that the Twitter archive is amazing, but it only contains very basic tweet information that comes in JSON format. So I need to gather, asses and clean the Twitter data for a worthy analysis and visualization.

### Key Points
We only want original ratings (no retweets) that have images. Though there are 5000+ tweets in the dataset, not all are dog ratings and some are retweets.
We do not need to gather the tweets beyond August 1st, 2017. We can, but note that we won't be able to gather the image predictions for these tweets since we don't have access to the algorithm used.
Fully assessing and cleaning the entire dataset requires exceptional effort so only a subset of its issues (eight (8) quality issues and two (2) tidiness issues at minimum) need to be assessed and cleaned.
Cleaning includes merging individual pieces of data according to the rules of tidy data.

### The Data
###### Enhanced Twitter Archive
The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not everything. One column the archive does contain though: each tweet's text, which I used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced.".We manually downloaded this file manually by clicking the following link: twitter_archive_enhanced.csv

###### Additional Data via the Twitter API
Back to the basic-ness of Twitter archives: retweet count and favorite count are two of the notable column omissions. Fortunately, this additional data can be gathered by anyone from Twitter's API. Well, "anyone" who has access to data for the 3000 most recent tweets, at least. But we, because we have the WeRateDogs Twitter archive and specifically the tweet IDs within it, can gather this data for all 5000+. And guess what? We're going to query Twitter's API to gather this valuable data.

###### Image Predictions File
he tweet image predictions, i.e., what breed of dog (or other object, animal, etc.) is present in each tweet according to a neural network. This file (image_predictions.tsv) hosted on Udacity's servers and we downloaded it programmatically using python Requests library on the following (URL of the file: https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv)

### Project Details
Fully assessing and cleaning the entire dataset would require exceptional effort so only a subset of its issues (eight quality issues and two tidiness issues at minimum) needed to be assessed and cleaned.

###### The tasks for this project were:
1- Data wrangling, which consists of: Gathering data, Assessing data & Cleaning data.
2- Storing, analyzing, and visualizing our wrangled data.
3- Reporting on my data wrangling efforts and my analyses and visualizations about the dataset.

###### Installing
Install Jupyter Notebook to run wrangle_act.ipynb.
Need consumer_key, consumer_secret, access_token, access_secret to query from Twitter API.

### Require the following libraries installed.

Python's libraries: Pandas, Numpy & matplotlib.pyplot

Importing requests library

Importing tweepy library

Importing json library

### Files
1- act_report: Communicates the insights and displays the Visualizations produced from the wrangled data.
2- ./Data/image_prediction.tsv: Data downloaded using Requests library and URL.
3- ./Data/tweet_json.txt: Data gathered from twitter API.
4- ./Data/twitter-archive-enhanced.csv: File downloaded from Udacity.
5- ./Data/twitter_archive_master.csv: The clean DataFrame 1.
6- ./Data/twitter_image_predictions.csv: The clean DataFrame 2.
7- wrangle_act.ipynb: The main file containing all the gathering, wrangling and analyzing work.
8- wrangle_report: Briefly describes my wrangling efforts.

Resources
[Twitter API ](https://developer.twitter.com/content/developer-twitter/en.html)
