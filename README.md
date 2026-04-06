Recommender Systems Project

Overview

This project implements and evaluates four different recommendation approaches using the MovieLens dataset:

- Non-Personalized Recommender  
- Collaborative Filtering Recommender  
- Content-Based Recommender  
- Context-Aware Recommender  

The goal is to compare these approaches under a unified evaluation framework and analyze their performance using multiple metric families.


Dataset

We use the **MovieLens (ml-latest-small)** dataset, which contains:

- User ratings (`userId`, `movieId`, `rating`)  
- Movie metadata (titles and genres)  
- Timestamps for each interaction  

The dataset is highly sparse, making it suitable for testing different recommendation strategies.



Methodology

1. Non-Personalized Recommender
- Based on global statistics (average, popularity, weighted rating)  
- Serves as a strong baseline  

2. Collaborative Filtering
- User-based collaborative filtering  
- Uses similarity measures (Pearson / cosine)  
- Provides personalized recommendations  

3. Content-Based Recommender
- Uses movie genres as features  
- Computes item-item similarity  
- Recommends similar items based on user preferences  

4. Context-Aware Recommender
- Extends content-based approach  
- Uses weekday vs weekend as context  
- Applies contextual pre-filtering  



Evaluation

Offline Evaluation
All models are evaluated using a **temporal train-test split**:
- First 80% → training  
- Last 20% → testing  



Metrics

Prediction Accuracy
- RMSE  
- MAE  

Ranking Metrics
- Precision@K  
- Recall@K  
- NDCG  

Beyond-Accuracy Metrics
- Coverage  
- Diversity  
- Serendipity  


Results

The models are compared using a standardized evaluation table:

| Model | Key Insight |
|------|------------|
| Non-Personalized | Strong baseline, high precision |
| Collaborative Filtering | Best personalization and ranking quality |
| Content-Based | Good coverage, interpretable |
| Context-Aware | Adds situational relevance, moderate gains |



A/B Testing (Simulated)

A simulated A/B test was conducted comparing:

- **Variant A** → Non-Personalized  
- **Variant B** → Collaborative Filtering  

Metric used:
- **HitRate@10**

Result:
- Non-Personalized slightly outperformed CF in this offline simulation  
- The difference is small and should be validated with a real online experiment  




