This project explores whether embedding-based signals, independent of traditional syntactic features, can accurately predict textual complexity. By leveraging vector representations of words, I investigated the relationship between semantic structure and human-rated cognitive load.

🔑 Key Features

Model Comparison: Trained and evaluated standard Word2vec (linear co-occurrence) against Word2vecf (dependency-based embeddings) on a 60GB Wikipedia corpus.

Metric Engineering: Developed and implemented four embedding-based metrics to model cognitive load: Rarity Mean, PCA Shannon Entropy, Weighted Mahalanobis Distance, and Average Pairwise Distance.

Machine Learning Pipeline: Trained XGBoost models with bootstrap iterations to predict readability scores from the CLEAR corpus.

Model Interpretability: Utilized SHAP (SHapley Additive exPlanations) to analyze feature contributions and identify non-linear interactions between embedding metrics.


📊 Results

Dependency-based embeddings (Word2vecf) significantly outperformed standard models, achieving an $R^2$ of 0.24, suggesting that syntactic-aware embeddings better align with human text understanding.

Discovered a significant negative correlation between Pairwise Distance and text difficulty, indicating that "hard" texts often feature rare words that cluster tightly in semantic space.
