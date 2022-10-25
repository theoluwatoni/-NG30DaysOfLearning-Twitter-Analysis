# TWITTER ANALYSIS-OF-'#30DaysOfLearning and #NG30DaysOfLearning' HASHTAGS
Data cleaning, analysis, and report creation for the #30DaysOfLearning and #NG30DaysOfLearning tweet hashtags in PowerBI.


## INTRODUCTION
This project is a product of my participation in the #NG30DaysOfLearning initiative, which was put together by Olanrewaju Oyinbooke and his team to keep students occupied and assist them in learning throughout the 2022 ASUU strike. The items are included in the documentation:
1. Problem Statement
2. Data Collection
3. Data Cleaning Transformation 
4. Report Design
5. Findings 
6. Conclusion

## 1. PROBLEM STATEMENT
This project examined tweets which contained the  '#30DaysOfLearning and #NG30DaysOfLearning' hashtag from the period of Jun 1 - Jul 31, 2022 and examined a variety of elements that may contribute to each tweet. Some of my personal goals or inquiries were as follows:
1. What number of tweets were recorded during the period?
2. What number of people made use of the hashtag ?
3. What data analysis tools did people mention the most?
4. What connection exists between tweets and the days of the week/month?
5. Where were the most spoken about words?
6. What are the most popular locations of people that used hashtag?
7. Who are the most active users?


## 2. DATA COLLECTION
The data was obtained from Twitter and contained  the full contents of tweets with the #30DaysOfLeaning or #NG30DaysOfLearning hashtags, from June 1st - July 31st 2022. 
The data originally had 1246 rows and 10 columns. The main features of the dataset include:
* Date - Date (yyyy/mm/dd) and Time (24hr format) of the tweet
* TweetUrL - A link leading directly to each tweet
* User - User/Username that made each tweet
* Source - Device used to tweet (Twitter for Android, Twitter for IPhone, etc)
* Location - The location on the User's profile
* Tweet - Content of each tweet which contained any of the hashtags
* Likes_Count- Total number of likes on each tweet
* Retweet_Count - Total number of retweets on each tweet
* Quote_Count- Total number of quoted tweets on each tweet
* Reply_Count- Total number of  replies on each tweet

The dataset was extracted with Python and was later downloaded as a csv file to my local computer.


## 3. DATA CLEANING & TRANSFORMATION
Before being imported into PowerBI, the data was originally scraped with 'snscrpae' using Python in Jupyter Notebook. SNSCRAPE is a scraping tool for social networking services (SNS). It scrapes information like user profiles, hashtags, searches, and threads and returns the discovered items. It was released on July 8, 2020, and it is capable of scraping data from a variety of platforms, including the following:
* Twitter
* Instagram
* Reddit
* Facebook
* Weibo
* Telegram
* Mastodon
On Twitter, it can scrape users, user profiles, hashtags, searches, tweets (single or surrounding thread), list posts, and trends.

To carry out fundamental operations, pandas, a library that deals with dataframes had to be loaded. 
After scraping the required columns/features for this particular project, it was converted to a dataframe format using the pd.DataFrame() function. the dataframe had 1246 entries and 10 columns. There were no null values in the data. The data was now saved to my local disk as a .csv file.
You can access the Python file used for the scraping here.
The csv file was now loaded into PowerBI and some data manipulations were observed here. The Date column had to be split into its respective years, months, dates(1-31), day of the week and time.
The location column was really untidy because some locations that users have do not exist, e.g. 'everywhere', 'migrating', etc. Also, it was noticed that in most instances, the location column was filled as states, then country while others were just blank. Since some users were not in Nigeria, only the states were extracted and used as location to form a new column called 'New Location'.

## 4. REPORT DESIGN
The layout for this report was created using Figma, a design tool that enables you to create designs for mobile and web interfaces as well as any other kind of design you can think of. After choosing the queries to be answered and the reports to use, several card designs were created for each viz and integrated into a single design. The Figma icon plugin iconify is where all of the icons used in this report were acquired from. Color schemes and shades were selected from adobe.color.com. You can access all necessary images and icons [here](https://github.com/theoluwatoni/-NG30DaysOfLearning-Twitter-Analysis/tree/main/images%20and%20icons).


And here is what the final combined report design looks like:
![image](https://user-images.githubusercontent.com/112688755/197814544-cd9c126a-6057-4b37-8d1d-757159ae4efa.png)


## 5. FINDINGS
* There were a total of 1241 tweets made by 312 distinct users
* There was significantly more activity in June, than July and this is because most part of the program occurred in June.  
* TheOyinbooke and Richie4love were the most active users
* People were more active during weekdays that weekends.
* PowerBi and GitHub were the most mentioned tools with about 150 mentions while Excel had 106 and Azure, the least, had 27 mentions.
* The hashtags were what people spoke about the most following TheOyinbooke, Data, Covid, Dashboards, etc.


## 6. CONCLUSION
I had a lot of fun learning new concepts and doing new things. If you want to replicate, I hope my documentation is clear enough for you to comprehend. I've included all necessary details to help you do that. You are welcome to change my scripts or designs to create something more beautiful. If you do, kindly mention me on Twitter by using the handle @superweirdpm. 🚀
To view the report's complete functionality and User Experience, explore the [interactive session](https://app.powerbi.com/view?r=eyJrIjoiOGIyZWJmY2YtMmI3OC00MjRlLTk3ODYtMDM1YTNlM2U1NTAwIiwidCI6ImYxMDIxMjliLTQwMjUtNDFlOC05ZDAyLThlMzRmNmE1ZjQyNCJ9).
