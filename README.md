# Project Summary

- Team 13

## 1. Motivation and problem definition

<div style="text-align: justify"> The idea of this project is to predict the rating that a user can give to an unvisited restaurant based on his previous interests/behavior. This prediction can be beneficial both for the business and for the users. It is an opportunity to recognize its possible customers and design a business plan to maximize the satisfaction of their target society. In addition, Yelp can use it to recommend new businesses to its own users and increase platform usage. This creates a magical loop where the user uses the platform more frequently and then makes the business's rating more accurate (creating an endless cycle that generates data). 

## 2. Algorithm and methods

There are two main approaches for the recommendation system which we plan to design.

### 2.1 Content-based approach

Content-based filtering uses item features to recommend other items similar to what the user likes, based on their previous actions (e.g., visiting a website) or explicit feedback (e.g., rating).
In this scenario, we have to build a separate profile for users and for the restaurants and define a metric to measure the distances between the two restaurants. For example, we can use the cosine distance between the vectors of the item and the user to determine its preference. The item profile for restaurants may include city, state, category, etc, while the user profile will be the weighted average of the rated item profile.



### 2.2 Collaborative filtering (CF)

CF uses similarities between users and items simultaneously to provide recommendations. This allows recommending an item to user A based on the interests of a similar user B. In order to find these similarities, we can use some well-known approaches such as Jaccard Similarity, Cosine Similarity, and Pearson Correlation Coefficient.
Furthermore, to achieve better results,  we can also leverage hybrid methods which combine Content-Based Filtering and CF.



## 3. Dataset and features

In this project, we will use Yelp’s dataset, more specifically the restaurant category. The dataset is composed of three JSON files:
1. business.json contains 160,585 businesses including location, attributes, and categories.
2. review.json contains 8,635,403 review text,  user’s id, restaurant’s id, and the restaurant rate (1-5).
3. user.json contains data about 2,189,457 users, such as popularity, friends, and names.


## 4. Metrics to evaluate model

We will use Root Mean Square Error (RMSE) and Mean Average Error (MAE), which are popular measures to evaluate regression problems.
</div>
