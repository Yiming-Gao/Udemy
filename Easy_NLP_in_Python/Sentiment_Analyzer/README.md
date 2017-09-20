Github page: https://github.com/lazyprogrammer/machine_learning_examples/tree/master/nlp_class

- sentiment: how positive or negative some text is
- Amazon reviews, Yelp reviews, hotel reviews, tweets

Our data: https://www.cs.jhu.edu/~mdredze/datasets/sentiment/index2.html


### Outline of our sentiment analyzer
- We'll just look at the electronics category, but you can try the same code on others
- We could use 5 star targets to do regression, but let's just do classification since they are already marked "positive" and "negative"
- XML parser (BeautifulSoup)
- Only look at key "review_text"
- We'll need 2 passes, one to **determine vocabulary size and which index corresponds to which word**, and one to **create data vectors**
- After that, we can just use any SK-Learn classifier as we did previously
- We'll use logistic regression so we can interpret the weights

### NLTK
Natural language toolkit

"sudo pip install nltk"

***nltk.download()*** if you're missing a resource

1. POS tagging

***nltk.pos_tag("Machine learning is great")***: takes in an array of tokens, and split it into tokens

2. Stemming and lemmatization

- both reduce words to a "base" form
- useful because vocabulary can get too large easily
  - but "dog / dogs" or "jump / jumping" probably have the same meaning
- What's the difference?
  - stemming is more "crude"

***PorterStemmer()***

3. NER (Named entity recognition)

"Albert Einstein" to person; "Apple" to organization

s = "Albert Einstein was born on March 14, 1879."

tags = nltk.pos_tag(s.split())

***nltk.ne_chunk(tags)*** # need to install maxent_ne_chunker

***nltk.ne_chunk(tags).draw()*** # draw the tree
