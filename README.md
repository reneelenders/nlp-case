# Case description
You're going to construct an NLP-based movie recommender. The idea is that you provide a movie to the recommender, and the recommender passes back similar movies.
Your task is to present your suggestions for the movie: The American President and explain how you came up with these suggestions.

Python is the go-to language for Machine Learning, since there are a lot of algorithm implementations.
It is recommended to use a virtual environment (instead of Anaconda).

## Step 1: Read data
Using pandas. 

Pandas documentation at: `https://pandas.pydata.org/docs/`

## Step 2: Document embeddings
### Option 1: Create TF-IDF yourself
You can choose to implement TFIDF yourself, but you can also use an existing implementation. It's in scikit-learn (sklearn) and can be imported via:
`from sklearn.feature_extraction.text import TfidfVectorizer`

Sklearn's TFIDF documentation at:
`https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html`

### Option 2: Use implementation of W2V
Word2Vec (W2V) is implemented in Spacy. After installing spacy in your Python environment, you can install a pretrained W2V model via your terminal:

`python -m spacy download en_core_web_md`

Note: Check that `python` refers to the relevant Python interpreter.

Next, you can load the model by:
`model = spacy.load('en_core_web_md')`

Spacy documentation at:
`https://spacy.io/usage/models`

## Step 3: Cosine similarity
Recall that the cosine similarity is defined as:
![img.png](img.png)

For implementing a dot product, you can use e.g. numpy.

Now you've got all the elements required to make your recommender work: For a given movie, you can compute all the pairwise cosine similarities, and check which movie(s) are most similar.

## Step 4: Extra's
If you want, you can also add some filters, e.g. on genre level. Or visualize the stuff you have in a dashboard, or make some other things you think are cool :-)

## Step 5: Presentation
Create a presentation which has your top 5 suggestions for the movie: The American President and explain how you came up with these suggestions.
