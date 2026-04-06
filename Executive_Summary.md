
## Executive Summary

Through the MovieLens dataset, this project creates and evaluates four types of recommender systems (Non-Personalized, Collaborative Filtering, Content-Based, Context-Aware). It aims to run an assessment of the proposed solutions on a unified evaluation setup and explore their strengths and weaknesses.

T he temporal split approach was used for training and testing the models. Many sets of metrics were used for measuring the quality of the predictions: accuracy metrics (Root Mean Squared Error, Mean Absolute Error), ranking metrics (Precision@K, Recall@K, Normalized Discounted Cumulative Gain) and extra-accuracy ones like Coverage, Diversity and Serendipity.

Therefore, Non-Personalized serves as a good baseline, Collaborative Filtering does well in personalization and ranking. On the other hand, the Content-Based model is very consistent, but it suffers from low feature-based items expressiveness description. Last but not least, the Context-Aware algorithm brings little changes around situational adjustment of recommendations.

An A/B testing method was simulated to evaluate the proposed models performance and it came out that both Non-Personalized and Collaborative Filtering show a slight lead over each other based on HitRate@10 in offline evaluation space.
