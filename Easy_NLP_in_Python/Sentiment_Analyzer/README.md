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
