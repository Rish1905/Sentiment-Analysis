# Sentiment-Analysis
Twitter is one of the biggest social media platform on which people can express views and sentiments on variety of topics. Our project is to analysis this data and visualize it on a world map. In the first half we fetch the coordinates of the trending topics and plot it on the world map by using python libraries. In the second half we differentiate all the coordinates on the basis of sentiments (In our case Positive, neutral, negative) by doing Natural Language Processing and color code on the graph.

LIVE PLOTTING AND SENTIMENT ANALYSIS OF TWEETS ON A WORLD MAP

We are performing historical and live analysis regarding the most talked hashtag or trending topic
by searching the hashtag or word as a user input within a tweet and then doing a sentiment analysis
of those tweets. Later, this data is plotted on the world map representing the sentiments on different
continents with different colors providing an overview regarding the emotions about that topic.

@@Getting Started@@

These instructions will help you to run software on your local machine for development and testing purposes.
	
	#Prerequisites#

	1) Download latest python version from the following site
	   www.python.org/downloads/release/python-365

	2) Install the downloaded file of python and tick the checkbox (Add python version to Path)

		--Required API Keys
		  Generate and add the following keys to the respective files before running the program (We have 
		  provided all the necessary keys for fast debugging)

		--Twitter API Key
		  1) Visit the following website for creating an account and then create an application for
		     acquiring keys for Twitter API
		     https://apps.twitter.com/

		  2) Generate Access Token, Access Token Secret, Consumer key and Consumer Secret. Create a 
		     file 'auth_dict' and paste all the above-mentioned keys. 

		--Google Map API Key
		  1) Create an account and generate Google Map API key. Assign this key to variable google_map_api 
		     in 'Group11_FinalProject.py' file 

		  2) For changing the limit of total number of tweets fetched, change the 'max_limit' variable in 
		     'Group11_FinalProject.py' file.

	#Installing#

	A step by step series of examples that tell you how to get a development environment running 

	1) Open terminal / Command prompt on your local machine
	2) Update latest version of pip using following command
	   python -m pip install --upgrade pip
	3) Run the following commands for installing the required libraries
		- pip install bokeh
		- pip install tweepy
		- pip install twitter
		- pip install textblob
	4) Download the project zip folder and extract it.
	5) From your terminal / command prompt, go to the folder where your file is downloaded.
	6) Run the following command to run the .py file
	   bokeh serve Group11_FinalProject.py --show


@@Testing@@

1) After running the program, a tab will open on your browser. You can see a Text field named Hashtag. 
   Provide a user input i.e. a trending HashTag or word ( for example - 'Avengers', 'Monday', 'championsleague' etc)
2) Select the number of days, since when you want to analyze data.
3) Click on the 'Fetch Data' button.
4) This program will take few minutes according the value of 'max_limit' variable.
5) After running the program, all the field will be enabled and you can analyze the result by changing the sentiment and 
   continent parameters.
6) The amount of data displayed on the map is directly proportional to the 'max_limit'. If you want to fetch more data 
   then we would have to change 'max_limit' value.


@Functionalities@

1) We provide 4 input fields and 2 buttons to the user which are as follow:

	- HashTag: This is an input field for providing a trending hashtag by the user. 
	- Day: This is a dropdown menu for the days from which a user wants to extract data from Twitter.
	- Fetch Data: A button is provided for fetching the data based on the above inputs.
	- Sentiment: This is a drop-down menu for displaying categories of sentiment which are categorized as positive, 
		     negative and neutral.
	- Continents: This is a dropdown menu using which a user can navigate through the map based on the continents.
	- Refresh Map: This button will refresh the data plotted, and update the map by loading real time sentiment analysis
		       of tweets.


@Cautions@

1) While running the program, 'output.csv' file will be generated. Don't open that file while software is running. 
2) Software halts for 15 minutes when rate limit exceeds. Program will automatically resume after 15 minutes. 
   (For debugging purpose, we have set limit to 7000)
3) This program takes some time depending on the value of 'max_limit' variable in the program. 


@Built With@

• Jupyter notebook - Integrated Development Environment
• Python - Programming language
