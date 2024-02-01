# Data_Assn2

Description:
This is the second data analysis assignment, The requirements are as follows:

## Requirements

Purpose
This assignment will help you practice using Python libraries to collect data from the web. Collect-
ing data directly from Twitter can be expensive. Therefore, I’ve chosen to use previously
collected Twitter data for your practice in data processing.
Google Maps Geocoding API
Apply for Google Maps Geocoding API. Set up Python access to this API using the sample codes presented
in the lectures.
1. [20 points] FIFAWorldCup2022.json (from Data directory on Canvas) includes 5000 tweets containing
“#FIFAWorldCup2022”.
Extract city and country from ‘place’ field (if they exist). Then, print the number of tweets per city
and country in descending order, e.g.:
City Number of Tweets
Doha 120
Buenos Aires 95
New York City 60
Country Number of Tweets
Qatar 350
USA 170
France 90
2. [30 points] “followers.json” and “followees.json” contain my Twitter followers/followees in the JSON
format.
a) [15 points] Construct a Pandas data frame from the followers and followees data that includes these
fields: id, name, screen name, follower or followee, location, description, followers count,
friends count (number of followees), favorite count, creation time (in datetime format), number
of tweets (statuses count) and verified.
b) [15 points] Using the constructed data frame, compute the following items:
I) The average followers count of your followers
II) The average followers count of your followees
III) The average followees count of your followers
IV) The average followees count of your followeees
V) The number of your verified followers/followees (separately and combined).
VI) The average favorites count of your followers/followees (separately and combined).
VII) The average number of tweets of your followers/followees (separately and combined).
VIII) Extract the number of your followers and followees per year using the creation time field,
e.g.:
1
Assignment 2 CS5850/CS6850 (Introduction to Data Analysis) Utah State University
Year Number of followers
2019 23
2016 21
2013 46
Year Number of followees
2020 6
2017 18
2013 20
4. [30 points] Use BeautifulSoup python package and retrieve project information and descriptions from my
lab’s research website https://cs.usu.edu/people/HamidKarimi/projects.html. The program should
save the results in an array of tuples [(t1,d2, l1), (t2,d2,l2), · · · ] where ti and di are the title and description
of the i-th project, respectively. li is a list of areas (items) below each project. For instance, t1 is “Social
Media Mining,” d1 is “Social Media Mining involves the representation, analysis, ...”, l1 is [ “Making
sense of user-generated content: Developing ...”, “Investigating friendship patterns: Analyzing the”, ...,
· · · ].
5. [20 points] Extract the latitude and longitude of each tweet of ‘geo tagged tweets.json’ file (available in
the Data folder on Canvas) and use Google Maps Geocoding to convert them to human-readable addresses.
Print the addresses and extract cities and states. All tweets are from the United States.
Here is how you can load the tweets from ‘geo tagged tweets.json’:
import json
json_str=json.load(open(‘geo_tagged_tweets.json’,‘r’))
tweets=json.loads(json_str)
Deliverables
• Assignmnet2.ipnyb: Your python notebook containing the code for all questions. Please properly
separate the solution to each question.
• Data files: FIFAWorldCup2022.json and nytimes-favorites.json
• Compress two previous items in a zip file named Assignment2.zip and submit it via Canvas.
