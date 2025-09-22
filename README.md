# Emoji-Prediction-Traditional-SVM-Algo-TimeLM
A classification task based on predicting 100 hetrogenoues emojis by leveraging SuperTweetEval Twitter dataset (2020–2023). The project compares traditional SVM with modern Transformers architecture, evaluating with top-1 and top-5 accuracy, plus error analysis on emoji clustering and class imbalance.
## Dataset
This project uses the **SuperTweetEval - Emoji** dataset (2020–2023), released by CardiffNLP.  
You can access it here: [SuperTweetEval Emoji on Hugging Face](https://huggingface.co/datasets/cardiffnlp/super_tweeteval/tree/main/data/tweet_emoji)
## Results

We evaluated three models on the **SuperTweetEval - Emoji** dataset:

| Model     | Top-5 Accuracy | Top-1 Accuracy |
|-----------|----------------|----------------|
| LinearSVM | **0.32766**    | **0.12244**    |
| TimeLM    | **0.32288**    | **0.12244**    |
| Baseline (Naive Bayes + Tfidf) | 0.15710 | 0.03862 |

- **LinearSVM** with bag-of-char n-grams and bag-of-word n-grams outperformed the baseline.
- **TimeLM** achieved competitive performance, though slightly below the SuperTweetEval benchmark (35.46% Top-5).
- Results highlight that emoji prediction with 100 heterogeneous classes remains challenging.
