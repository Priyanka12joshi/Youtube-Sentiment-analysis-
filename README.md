YouTube, one of the largest video-sharing platforms in the world, hosts an immense amount of content across various genres.
Each video can receive a multitude of comments from viewers, expressing a wide range of sentiments.
Sentiment analysis of YouTube comments can provide valuable insights into viewers' opinions, emotions, and overall engagement with the content. 
This analysis is beneficial for content creators, advertisers, and researchers to understand audience reactions and improve content strategy.

1. Creation of API Key Using Google Cloud Console:
o	The first step involved setting up a project in the Google Cloud Console to generate an API key. This key is essential for authenticating requests to the YouTube API.
o	Detailed steps on how to create the API key include navigating to the console, setting up a new project, enabling the YouTube Data API v3, and finally generating the API key.
Utilizing the YouTube API for Data Collection:
•	With the API key ready, the next step was to use the YouTube API to fetch data. The API provides access to a wealth of information about videos, channels, and playlists.
•	Specific endpoints were used to gather data from various YouTube channels and videos. This data included video titles, descriptions, view counts, like counts, comment counts, and the actual comments themselves.
•	The data collection process involved writing scripts to make API calls, handle responses, and store the collected data in a structured format for further analysis.

2. Utilizing the YouTube API for Data Collection:
 •	With the API key ready, the next step was to use the YouTube API to fetch data. The API provides access to a wealth of information about videos, channels, and playlists.
•	Specific endpoints were used to gather data from various YouTube channels and videos. This data included video titles, descriptions, view counts, like counts, comment counts, and the actual comments themselves.
•	The data collection process involved writing scripts to make API calls, handle responses, and store the collected data in a structured format for further analysis.

3.Importing Important Libraries for Sentiment Analysis
When performing sentiment analysis on YouTube video data using Python, several libraries are essential for data manipulation, visualization, sentiment scoring, and text analysis. Here’s a brief overview of the libraries mentioned and their usage in sentiment analysis:
1.	googleapiclient.discovery:
o	This library is crucial for interacting with the YouTube API. It allows you to build a service object that can make requests to the API, fetch data such as video details and comments, which is fundamental for data collection.
python Copy code:
from googleapiclient.discovery import build
2.	pandas:
   o	Pandas is used for data manipulation and analysis. It provides data structures like DataFrames, which are ideal for storing and analyzing tabular data fetched from YouTube using the API.
python
Copy code
import pandas as pd
3.	seaborn:
o	Seaborn is a statistical data visualization library based on Matplotlib. It is used to create more attractive and informative statistical graphics, which can be useful for visualizing sentiment distributions or relationships in the data.
python
Copy code
import seaborn as sns
4.	plotly.graph_objects and plotly.express:
o	Plotly is a library for creating interactive plots and dashboards. plotly.graph_objects and plotly.express provide different interfaces for creating a variety of plots such as scatter plots, bar charts, and more advanced visualizations.
python
Copy code
import plotly.graph_objects as go
import plotly.express as px
5.	collections.Counter:
o	Counter is a part of the Python collections module and is used for counting hashable objects. It is helpful for tasks such as counting word frequencies in text data, which can be useful for understanding common sentiments expressed in comments.
python
Copy code
from collections import Counter
6.	textblob:
o	TextBlob is a simple NLP library for processing textual data. It provides an easy-to-use API for tasks such as part-of-speech tagging, noun phrase extraction, sentiment analysis, classification, translation, and more.
python Copy code
from textblob import TextBlob

8.	vander api:
o	Assuming this refers to vaderSentiment, it is a library specifically designed for sentiment analysis. It uses lexicons of sentiment-related words to analyze sentiments expressed in text.
python Copy code
from vaderSentiment.vaderSentiment import SentimentIntensityAnalyzer

9.	wordcloud:
o	WordCloud is used for creating word clouds from text data. It visually represents the most frequently occurring words in a dataset, which can provide insights into the dominant sentiments or topics in comments.
Python
Copy code
from wordcloud import WordCloud

Usage in Sentiment Analysis
•	Data Collection: Use googleapiclient.discovery to fetch video details, comments, and other relevant data from YouTube.
•	Data Manipulation: Utilize pandas for storing and manipulating data in DataFrames, making it easier to clean and preprocess data.
•	Visualization: seaborn, plotly.graph_objects, and plotly.express help in creating visualizations to explore data distributions, sentiment trends, and more.
•	Sentiment Analysis: textblob and vaderSentiment aid in determining the sentiment polarity (positive, negative, neutral) of comments or text data.
•	Word Clouds: wordcloud can generate visual representations of the most frequent words in comments, providing a quick overview of prevalent sentiments or topics.

CONVERT  COLLECTED DATA INTO CSV FILE 
1.	Install the langdetect library :
pip install langdetect
2.	Use the langdetect library to detect the language of each comment and filter out the ones that are not in English or Hindi.
Explanation:
1.	Install and Import: Ensure you have langdetect installed and then import it along with pandas.
2.	Set Seed: Fix the random seed for consistent results from langdetect.
3.	Language Detection: Define a function detect_language to detect the language of a given comment. Handle exceptions where the language cannot be detected.
4.	Filter Comments: Use list comprehension to filter out comments that are not in English (en) or Hindi (hi).
5.	Create DataFrame and Save to CSV: Create a DataFrame from the filtered comments and save it to a CSV

6.	Working on streamlit:
1: Install Streamlit
Open your command prompt and run the following command to install Streamlit:
 python code - pip install streamlit
Step 2: Verify the Installation
After installation, you can verify that Streamlit is installed correctly by running:
python -c "import streamlit; print(streamlit.__version__)"
Step 3: Run the Streamlit App
Navigate to the directory containing your app.py file and run the Streamlit app:
streamlit run app.py
If you encounter any further issues, make sure you are using the correct Python interpreter and environment. You can check your Python interpreter by running:
python --version
And you can ensure you're using the correct environment by activating it if you're using a virtual environment:
For Windows:
.\venv\Scripts\activate
          Complete Example Code (app.py)
          Here is the complete code for app.py:

7.	


