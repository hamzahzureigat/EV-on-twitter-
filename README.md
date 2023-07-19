# EV-on-twitter-
it only extract data form twitter and do NLP on it. 
# Dataset Description
#### This dataset contains 5,708 tweets about electric cars (EVs) from 2014 to the present day. The data includes the following columns:
1. Date: The date when the tweet was posted.
2. Username: The Twitter handle of the user who posted the tweet.
3. Tweet Content: The text of the tweet.
4. Retweet Count: The number of times the tweet has been retweeted.
5. Like Count: The number of likes the tweet has received.


# load it into the database : 
1.I load data into githup and get url for it :

2. download mongodb compass  
4. install pymongo 
5. make a conection between python and mongodb by :

import pymongo 

client=pymongo.MongoClient("mongodb://localhost:27017") such copy the prtal ('localhost:27017') from mogodb

6. read csv file (provided in url) by : url= https://raw.githubusercontent.com/hamzahzureigat/data-/main/data3.csv


import pandas as pd 

df=pd.read_csv(url) 

7. then :

run : 
data = df.to_dict(orient='recorde')

make database and collection  in mongodb by : 

db=client['twitter']

db.Iris.insert_many(data) 

#### "the code in file name " data form twitter .ipynb " in this repository"

## Data Preparing

1. Data Profiling Stage:

1.1 Split the textual data into words.

  - split every word in the text use   while loop 
  
1.2 Print the 10 most frequent words in all textual content.

  - use  counter class 
  
1.3 Visualize the textual content using two different charts.

  - first one is bar chart represent the 10 most frequencies word 
  - secend one is  word cloud represent the word after some modifiction 
  
1.4 Print the total number of stopwords and the 10 most frequent stopwords in the text.

  - use libraries  nltk and stopwords cont of stop word use sum() 
  - and calculat the most frequenc by for loop
  
1.5 Check and identify the spelling mistakes in the text.

  - make funcion name identify_misspelled_words(dictionary_file) use dictionary for       github ulr=https://raw.githubusercontent.com/first20hours/google-10000-english/master/20k.txt such that any word not in the dictionary is misspelled word 
 
2. Data Cleaning Stage:

2.1 Remove all links, stopwords , punctuation and emoji 

  - remove all links by defition link pattern and any word in the list start with https is identfiy as a link 
  - remove stopwords and punctuation since we difine stopword in 1.4 we difiine the punction and remove all 
  
2.2 Print the 10 most fequent words in all textual content.

2.3 Print the count of unique words in the text.

  - use for loop  
 
2.4 Remove all typos with the correct word.

  - use for loop since we identify the misspelled word in 1.5 
 
2.5 Convert all words to small letters.

  - use lower ()
  
2.6 Apply a lemmatization technique.

  use WordNetLemmatizer the words get back to the root no ing or any thing like that 
  
2.7 Print the count of unique lemmatized words in the text.

  - like 2.3
### "the code in file name " data preparing.ipynb " in this repository"

# future Potential Applications

1. identify the benefits of electric cars that are most important to people
2. Addressing misconceptions about electric cars
3. Identifying the most popular electric car models or brands on social media 
