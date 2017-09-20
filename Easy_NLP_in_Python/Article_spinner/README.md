- Very useful tool for Internet marketers
- Allows us to use computers to do work for us (automation)
- Scale
- Content-creation and generation
- Can no longer just repeat a keyword 1000 times in invisible text for SEO
- Now duplicate content is heavily penalized (can't just copy your high ranking article 1000 times)
- Search engine users want the most useful results (not just what you want to sell them)

### What is article spinning?
- Take an article and slightly modify it (synonyms, replace phrases that have the same meaning)
- Results in a new article with different terms, but same meaning

### Using Context
- Label our words w(1), w(2), ..., w(N)
- Model w(i) using w(1), ..., w(i-1), and w(i+1),..., w(N)
- Probabilistic: P{w(i)|w(1), ..., w(i-1), w(i+1),..., w(N)}

### Trigrams
- Specific instance of "N-gram" where N = 3
- We'll model P{w(i)|w(i-1), w(i+1)}
- **How?** Use a Python dictionary with {w(i-1), w(i+1)} as the key, and lookup w(i)
- Replace each term with p = 0.2
- This and LSA are unsupervised learning
