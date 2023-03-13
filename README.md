# WeRateDogs Twitter Data Wrangling
## by Josephine Ochai


## Description of Project & Dataset Used

WeRateDogs is a very famous twitter account with over 4 million followers, that has gained wide media coverage over the years for their humorous contents about dogs and their dog ratings which usually have a denominator value of 10 and a numerator value higher than that. Its twitter archive contains basic tweet data such as tweet_id, timestamp, dog_stage, twitter url etc. Additional data was also obtained by querying Twitter's API as well as downloading programatically, a dataset about the top 3 predictions of dog breeds by an algorithm using images contained in the twitter archive.
The goal of this project was to apply data wrangling process to the tweet archive at WeRateDogs. 

The following sections documents the data wrangling steps -gather, assess & clean -taken to properly wrangle gathered data for analysis and visualization.


## Data Gathering

* The first dataset, the 'twitter-archive-enhanced' is a csv file that was read into a pandas dataframe.
* The second dataset was additional data that was obtained via twitter's api. However, I encountered some challenges with creating a twitter developer account and had to use a back up 'tweet_json.txt' file instead that contained same information.
* Using the requests library, the 3rd dataset -image_predictions.tsv was downloaded programmatically with the url provided and read into a dataframe as well.


## Assessing Data

After gathering and creating dataframes out of all 3 datasets, each of the tables were visually and programatically assesed for data quality and tidiness issues present and any observations were properly documented before attempting to clean the data.

Quality issues identified had to do with erroneous data types, inaccurate values, missing values and inconsistent values in several columns. Also, tidiness issues were identified like variable values being treated as the actual variables in one case and same type of observational units split into two tables in another.In all, 8 quality issues and 4 tidiness issues were identified.  


## Cleaning Data

Firstly, copies were created of the three datasets to have a 'fall back to' file in the event that one needed the original information present before. To achieve proper cleaning, missing values problems were first addressed across all 3 tables after which all tidiness issues identified were taken care of. Quality issues were dealt with lastly.


## Storing Data
An extensive cleaning of the data led to the datasets reduced from 3 to 1. All 3 datasets were merged as one, joining on the common tweet_id column.

The resulting table was stored in a csv file called 'twitter_archive_master.csv' as a master copy which was used for analysis and visualisation purposes. This file is also included in the repository.
