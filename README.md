For other data science related projects please go to [Springboard Data Science Projects](https://github.com/dametreusv/Springboard_Data_Science) or [Predicting Income Groups Using World Development Indicators](https://github.com/dametreusv/world_development_indicators/blob/master/README.md).

-------

# Amazon Customer Review Insights & Hybrid Product Recommendation System

[Amazon Customer Review Insights & Recommendation System](https://github.com/dametreusv/amazon_hybrid_recommendation_system/blob/master/APR_final_report.ipynb)

We want to build a hybrid recommendation engine that will not only recommend similar products but also recommend products in other categories, genres or fields to a shopper in order to help them find what they might not have been looking for.

-----------------

<img src='https://raw.githubusercontent.com/dametreusv/amazon_hybrid_recommendation_system/master/visuals/rating_distributions.png'>

## Table of Contents
--------------------------


### Introduction
[About the Amazon Customer Reviews Dataset](https://s3.amazonaws.com/amazon-reviews-pds/readme.html)

[The Proposal](https://github.com/dametreusv/amazon_hybrid_recommendation_system/blob/master/APR_Proposal.pdf)

[The Multilingual (US) Dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)
- The dataset is too big to upload onto github (3.63gb) but can be found under the multilingual reviews portion of the link.  Just copy and paste the line within the link to download any of the datasets.


### Data Wrangling
[Data Acquisition and Cleaning](https://github.com/dametreusv/amazon_hybrid_recommendation_system/blob/master/APR_wrangle.ipynb)


### Exploratory Data Analaysis
[Data Analysis](https://github.com/dametreusv/amazon_hybrid_recommendation_system/blob/master/APR_analysis.ipynb)
- [Data Analysis with Internal Navigation Links](https://nbviewer.jupyter.org/github/dametreusv/amazon_hybrid_recommendation_system/blob/master/APR_analysis.ipynb)


### Milestone Report
[Report via Github](https://github.com/dametreusv/amazon_hybrid_recommendation_system/blob/master/APR_milestone_report.ipynb)
- [Report with Internal Navigation Links](https://nbviewer.jupyter.org/github/dametreusv/amazon_hybrid_recommendation_system/blob/master/APR_milestone_report.ipynb)


### Recommendation Modules
[Simple Keyword Search](https://github.com/dametreusv/amazon_hybrid_recommendation_system/blob/master/APR_recommender_keyword_simple.ipynb)

[Collaborative Filtering Recommender](https://github.com/dametreusv/amazon_hybrid_recommendation_system/blob/master/APR_recommender_collaborative.ipynb)
- [Collaborative Filtering Recommender with Internal Navigation Links](https://nbviewer.jupyter.org/github/dametreusv/amazon_hybrid_recommendation_system/blob/master/APR_recommender_collaborative.ipynb)

### Final Report
[Amazon Customer Review Insights & Recommendation System](https://github.com/dametreusv/amazon_hybrid_recommendation_system/blob/master/APR_final_report.ipynb)

[APR Slide Deck](https://github.com/dametreusv/amazon_hybrid_recommendation_system/blob/master/APR_slidedeck.pdf)

--------

## Executive Summary

[Amazon](https://www.amazon.com) is a multinational technology company based in Seattle, Washington, that focuses on e-commerce, cloud computing, digital streaming, artificial intelligence and more.  One of its most popular services is the [e-commerce](https://s3.amazonaws.com/amazon-reviews-pds/readme.html) website ‘Amazon.com.’  One of the ways Amazon keeps its shoppers engaged is by way of its product recommendation system. The product recommendation system uses content and collaborative based filtering, looking at a shopper’s past purchases and purchases by shoppers who purchased similar items and then recommends items that the shopper may like based off of these two behaviors. Collaborative filtering enables the shopper to see items from other categories, while content based filtering allows shoppers to see domain specific items.

Unlike content based filtering, which suggest only similar products or domain specific products, collaborative filtering recommendation systems allows users to find similar products and jump (or switch) to other categories of products based on similarities with other users and products.  


## Overview

In our analysis we were able to:

- Look at the distribution of ratings among products and customers.
- Determine the most popular products and categories.
- Look at the highest rated categories and see what affects rating averages.
- Observe how ratings change over time.
- Determine the point where the Amazon marketplace exploded in growth.

We have found that:

- Over 60% of all reviews receive 5 star ratings.
- Most products have between 100 and 1,000 reviews.
- Most customers give between 1 and 10 reviews.
- Out of 11,500+ products, less than 250 have an average rating under 3.0.
- 90% of the Amazon marketplace revolves around books, music, movies and mobile apps.
- The top 3 categories have intangible products (digital).
- The range in the difference of average categorical ratings is 0.84, from 3.84 to 4.68.
- Over time the average annual ratings stay between 4.1 and 4.4.
- The marketplace has grown exponentially since 2011.
- Average product ratings are mostly affected by 5, 4 and 1 star reviews.
- Most reviews occur in January and December, likely because of the holidays.

In this case, we explore 3 different ways to use collaborative based filtering.

1. The first method suggests products that other users like to a specific user based on their rating of a specific product.  Essentially, it finds users that rated a product similar to the specific user and returns the top products the other users liked.

2. The second method predicts what products a user may like based on past rating history and the rating history of other users.  This method is not specific to the rating of one product like the first method.

3. The third method predicts products similar to a specific product by finding the nearest neighbors to that product.  This method is good for users who may want to purchase products as bundles.

We evaluate our methods by:
- Testing the recommendation systems to see what products they return.
- Understanding matrix factorization and how it effects collaborative filtering systems.
- Selecting and tuning various recommendation algorithms to find the best performing algorithm.
- Understanding estimated ratings vs. true ratings.
- Performing precision@k and recall@k tests.
