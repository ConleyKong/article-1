# Review prediction with Neo4j and TensorFlow

We show how to create an embedding to predict product reviews, using TensorFlow machine learning framework and the Neo4j graph database. It achieves 98% validation accuracy.
Introduction

A common problem in business is product recommendation. Given what a user has liked so far, what should we suggest they purchase next? Just as a waiter asking if you’d like another drink drives higher revenues, so does successful recommendations.

There are many approaches to recommendation. We’re going to focus on review prediction: given a product a person has not reviewed, what review would they give it? We can then recommend to that person the products we predict they will favorably review.

## Running

The data for this experiment can be generated by executing `./generate.py --dataset article_1` from our [generate-data](https://github.com/Octavian-ai/generate-data) repository

Setup your environment:
```
pipenv install
pipenv shell
```

Then in the virtualenv:
```
python -m src.train
```

Finally, check out the results:
```
tensorboard --logdir ./output
```