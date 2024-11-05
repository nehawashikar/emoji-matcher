# EmojiMatcher

A machine learning model that suggests emojis based on the sentiment of a given text input. This project aims to enhance digital communication by providing users with the most relevant emoji suggestions, improving user experience on social media platforms.

Example:

<img width="839" alt="IMG_6734" src="https://github.com/user-attachments/assets/9471f262-e334-426f-8c07-d7b695a1748c">


## Problem Statement

People often struggle to find the right emoji to express their emotions accurately. Emoji Matcher addresses this by suggesting probable emojis based on text sentiment, making it quicker and easier to compose expressive messages.

## Dataset

- **Training Data**: 70,000 labeled entries, mapping text to emojis represented as numbers (0-19).
- **Testing Data**: 25,958 unlabeled entries.
- **Data Statistics**:
  - 648,941 total words with 101,162 unique words.
  - Average message length: 11.58 words.

## Preprocessing

- Converted text to lowercase, removed tags, numbers, punctuation, and stop words.
- Split data into training and test sets with an 80-20 ratio.
- Transformed numerical labels to categorical labels for model compatibility.

## Model Architecture

We used an LSTM-based neural network with the following layers:
- **Bidirectional LSTM Layers**: 2
- **Dropout Layers**: 2 (0.4 dropout rate)
- **Dense Layers**: 3 (ReLU activation)
- **Output Layer**: Softmax activation

### Hyperparameter Tuning

Various hyperparameters were adjusted to achieve optimal results:
- Learning rate, batch size, early stopping criteria, validation split ratio, and dropout rate.
- We tested different architectures and identified issues with overfitting, which led to using a simpler model with kernel regularization.

### Model Performance

Key metrics:
- **Training Accuracy**: 81.62%
- **Testing Accuracy**: 73.16%

## Pretrained Model: BERT

In addition to the LSTM model, we experimented with fine-tuning a BERT model:
- **Training Loss**: 3.013
- **Training Accuracy**: 0.165
- **Testing Loss**: 3.057
- **Testing Accuracy**: 0.215

## Challenges and Limitations

- **Long Training Time**: Due to the dataset size, a random sample of 30,000 entries was used for initial testing.
- **Data Imbalance**: Class imbalances impacted model performance.
- **Unlabeled Test Set**: Required splitting the dataset to create labeled test data.

## Future Improvements

To enhance the model:
1. Increase accuracy with advanced techniques like custom embeddings.
2. Introduce additional metrics like F1-score and ROC AUC.
3. Further modularize data preprocessing steps.
4. Optimize hyperparameters to reduce training time.

## Conclusion

Emoji Matcher demonstrates the complexities of sentiment analysis with emojis, revealing insights into data preprocessing and text structure in predicting sentiment. Custom embeddings and thorough preprocessing can significantly improve model outcomes in NLP tasks.

## Authors

- Neha Washikar
- Sanjana Jagarlapudi

