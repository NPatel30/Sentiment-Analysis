# Sentiment-Analysis
## Context
#### This is the sentiment140 dataset. It contains 1,600,000 tweets extracted using the twitter api . The tweets have been annotated (0 = negative, 4 = positive) and they can be used to detect sentiment .
## Content
#### It contains the following 6 fields:
#### target: the polarity of the tweet (0 = negative, 2 = neutral, 4 = positive)
#### ids: The id of the tweet ( 2087)
#### date: the date of the tweet (Sat May 16 23:58:44 UTC 2009)
#### flag: The query (lyx). If there is no query, then this value is NO_QUERY.
#### user: the user that tweeted (robotickilldozr)
#### text: the text of the tweet (Lyx is cool)
## Data Cleaning & Preprocessing
#### We'll remove unnecessary characters, lowercase the text, and tokenize words
#### Lowercasing – Convert all text to lowercase to maintain consistency.
#### Removing Punctuation & Special Characters – These don’t add value to sentiment analysis.
#### Tokenization – Split sentences into individual words.
#### Removing Stopwords – Words like "the," "is," and "at" don’t contribute much meaning.
#### Lemmatization/Stemming – Convert words to their root form (e.g., "running" → "run").
## Cleaning Tweets:¶
#### To improve the quality of our dataset, we need to clean the tweets by removing unnecessary elements like links, special characters, and stopwords. Let's go through the function step by step:
### 1. Importing Required LibrariesWe first import the necessary libraries for text processing:
#### re: For regular expressions, which help in text cleaning.
#### nltk: A powerful library for natural language processing (NLP).
#### stopwords from nltk.corpus: A list of common words (e.g., "the", "is", "and") that don't add much meaning.
#### PorterStemmer: A stemming algorithm that reduces words to their root form (e.g., "running" → "run").
#### STOPWORDS from wordcloud: Another set of common words to remove.
### 2. Downloading and Defining Stopwords:
#### We download the stopwords list using nltk.download('stopwords').
#### We create a set of stopwords for faster lookups.
#### We add extra stopwords: "amp", "rt", "lt", and "gt" (often seen in tweets but aren't meaningful).
## Exploratory Data Analysis - EDA¶
#### After cleaning the data, the next step is to understand its characteristics using statistical analysis and visualizations.
#### "First, we'll convert the sentiment labels to their original meanings for better readability:
#### 0 → Negative 😠
#### 4 → Positive 😊
## Sentiment Distribution¶
#### Objective: Determine whether the dataset is balanced or biased toward a particular sentiment.
## Data Modeling
#### "Data Modeling" is the next phase in our pipeline. In this stage, we build and train models that can predict sentiment based on the processed tweet text.
#### Feature Extraction: Convert cleaned tweet text into numerical features using techniques such as TF-IDF, bag-of-words, or word embeddings.
#### Splitting the Data: Divide the dataset into training and testing subsets to evaluate model performance.
#### Model Selection: Choose a suitable algorithm (like logistic regression, SVM, or deep learning models) for sentiment classification.
#### Training the Model: Fit the chosen model on the training data.
#### Evaluation: Assess model performance on the test set using metrics like accuracy, precision, recall, and F1-score.
#### Feature Extraction: In this stage, we will use the Bag-of-Words technique.
#### Bag-of-Words is a method for converting text data into numerical features that can be used by machine learning algorithms. The process involves:
#### Vocabulary Creation: Building a list of all unique words found in the corpus (in this case, all tweets).
#### Vectorization: Representing each tweet as a vector, where each element corresponds to the count (or frequency) of a word from the vocabulary in that tweet.
#### Simplicity and Efficiency: This technique ignores the grammar and word order, focusing solely on the occurrence of words, which makes it simple yet effective for many text classification tasks such as sentiment analysis.
