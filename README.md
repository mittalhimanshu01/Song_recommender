# Song_Recommender

## A content based song recommeder system that recommends top 5 songs based on a song you like

**Dataset used** :- *https://www.kaggle.com/datasets/joebeachcapital/57651-spotify-songs*

*(Note:- The orginal dataset has over 57000 rows but I only used 10000 so as to speed up the process)*

The model is based on bag-of-words technique for feature extraction, which is a popular technique used in natural language processing (NLP)

**Read More**:- *https://en.wikipedia.org/wiki/Bag-of-words_model*

**Approach**:- Tags have been created using the artist name and the lyrics (most suited for content based filtering) and then the top 500 words have been selected to access similarity between different songs.

To ensure these tags are relevant. Stopwords(words which do not convey meaning to a sentence but are used to add different words together) have been removed.

![stopwords](https://github.com/The-Honoured-One/Spotify_Song_Recommender/assets/152301760/5255689b-7f37-42f9-a98c-6ab86c6eb5c3)

Then, a vector is created using those scores and the similarity between those vectors is calculated using Cosine similarity ( I chose not to use Euclidean distances as it might not give good results in higher
dimension vectors). 

Lastly, the top 5 (excluding the song itself) songs are displayed based on this similarity score calculated earlier, to the user.

![example](https://github.com/The-Honoured-One/Spotify_Song_Recommender/assets/152301760/5eea0356-4914-4256-b38a-1641650c08e7)
