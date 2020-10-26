# NLP-Homework

### News Headlines Sentiment

Objective: Attempt to understand public sentiment around cryptocurrencies, specifically Bitcoin and Ethereum.
PROCESS:
Used NewsApiClient to pull articles in English on both, Bitcoin and Ethereum, and create DataFrames of sentiment scores for each cryptocurrency.
Displayed DataFrames showing Compound, Negative, Neutral, and Positive scores for each article.
Used .describe() to summarize scores into Count, Mean, STD, min, max, and percentile scores for each crypto.

FINDINGS:
Q: Which coin had the highest mean positive score?

A: BITCOIN [0.061050]

Q: Which coin had the highest compound score?

A: BITCOIN [0.726900]

Q. Which coin had the highest positive score?

A: BITCOIN [0.186000]

### Natural Language Processing

Objective: Tokenize text for each crypto. Generate ngrams and word frequency. Create word clouds for each coin.
PROCESS:
Completed a 'Tokenizer' function to remove punctuations, remove stopwords, change all letters to lower case, and lemmatize the words. 
Applied the 'Tokenizer' function to the text in each coin's articles and create a new 'tokens' column in each coin's dataframe.
Generated all the Bigrams for each coin's tokens. Created a 'Counter' function to count each coin's bigrams and listed the top 20.
Used a 'token_count' function to generate and display the top 10 words from each coin.
Joined all text in articles for Bitcoin and Ethereum to generate a single big string per coin.
Generated a word cloud for each coin with the content from each big string summarizing the most relevant terms in the news for Bitcoin and Ethereum.

FINDINGS:
Satoshi Nakaboto, which the articles identify as a "robot colleague" stood out as a frequent name displayed in the Bitcoin Word Cloud. This stood out as it was the only name of a 'PERSON' that was prominent in either Word Cloud. Bigrams that included either the first or last name of this entity also peppered the Bitcoin Word Cloud.

### Named Entity Recognition

Objective: Build Named Entity Recognition models for Bitcoin and Ethereum, and visualize the tags using SpaCy.

PROCESS:
Concatenated all text from Bitcoin and Ethereum articles.
Ran the NER processor on all of the concatenated text to identify all Named Entities. 
Visualized the results along with their entity Labels.
Parsed all entities in each cryptocurrency's text and created lists displaying each entity.

FINDINGS:
Just like in the Word Cloud, the Bitcoin list of entities again prominently featured the entity named "Satoshi Nakaboto," far exceeding that of any other 'PERSON'