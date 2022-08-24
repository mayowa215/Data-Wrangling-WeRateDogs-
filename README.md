# Wrangle and Analyze Data - [WeRateDogs Twitter Data]

## Project Steps Overview
My tasks in this project are as follows:

* Step 1: Gathering data
* Step 2: Assessing data
* Step 3: Cleaning data
* Step 4: Storing data
* Step 5: Analyzing, and visualizing data
* Step 6: Reporting
    your data wrangling efforts
    your data analyses and visualizations

## Introduction
The dataset to be wrangled (analyzing and visualizing) is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog.

Real-world data rarely comes clean. Using Python and its libraries, the data for this project will be gathered from variety of sources and in a variety of formats, assessed for quality and tidiness, then cleaned.

Using Python and its libraries, the data was gathered from a variety of sources and in a variety of formats, assess its quality and tidiness, then clean it. This is called data wrangling. Wtrangling efforts were documented in a Jupyter Notebook, plus showcased through analyses and visualizations using Python (and its libraries) and/or SQL.

## The Data
In this project, I worked on the following three datasets:

### Enhanced Twitter Archive
The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not everything. Of the 5000+ tweets, Udacity has filtered for tweets with ratings only (there are 2356). 
This archive is saved under this name: twitter_archive_enhanced.csv.

### Additional Data via the Twitter JSON Archive
Twitter archives are very basic, and a lot of information is missing in it, such as retweet count and favorite count. For this reason, Udacity has provided a json file called tweet_json.txt, which contains tweets' entire set of JSON data. The file was composed using Twitter's API.

In this project, I have read this .txt file line by line into a pandas DataFrame with tweet ID, retweet count, and favorite count.

### Image Predictions File
Udacity ran every image in the WeRateDogs Twitter archive through a neural network that can classify breeds of dogs*. The results: a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction. 
 The data is saved in a file named: image_predictions.tsv hosted on Udacity's servers and downloaded programmatically using the Requests Library and the following URL: https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv
 
 ## Assessing Data
 After gathering all three pieces of data, assess them visually and programmatically for quality and tidiness issues. Detect and document at least eight (8) quality issues and two (2) tidiness issues in the "Accessing Data" section in the wrangle_act.ipynb Jupyter Notebook.
 
 ### Quality issues
Twitter_archive table
* Null values are present in some columns.
* Timestamp not in datetime data type.
* Retweeted tweets are recorded, causing duplicate row entries.
* Details in source columns should be converted to 'Twitter for Iphone', 'Twitter web', 'Vine', 'TweetDeck'.
* Text column has different variables; ratings, url, text.
* Some columns are not properly named.
* Some columns are not needed.

Image_predictions table
* p1, p2, p3 not in uniform string case.
* Columns are not properly named.
* Some columns need to be dropped.

Tweet_data table
* Also, Tweet column has different variables; ratings, url, text.
* Columns need to be renamed

### Tidiness issues
* The three datasets should be merged in a table.
* Duplicated columns should be dropped.
* Dog stages are in four separate tables.

## Cleaning Data
All quality and tidiness issues documented while assessing the data was cleaned.

## Analyzing and Visualizing Data
In the Analyzing and Visualizing Data section in my wrangle_act.ipynb Jupyter Notebook, I analyzed and visualized the wrangled data to;

* produce at least three (3) insights and one (1) visualization.
* clearly document the piece of assessed and cleaned (if necessary) data used to make each analysis and visualization.

## Reporting
* Created a 300-600 word written report called wrangle_report.pdf or wrangle_report.html that briefly describes my wrangling efforts. 

* Created a 250-word-minimum written report called act_report.pdf or act_report.html that communicates all the insights and displays the visualization(s) produced from my wrangled data.
