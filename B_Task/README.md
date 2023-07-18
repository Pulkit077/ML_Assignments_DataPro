# Task B
Implement a natural language processing (NLP) task such as sentiment analysis or text classification using a pre-trained model. Discuss the steps involved, including data preprocessing, feature extraction, and model integration.

## My Approach
I've built a NLP Sentiment Analyzer using BERT pre-trained model.

### Steps Involved
• This model uses a data financial sentiment analysis research from [Kaggle](https://www.kaggle.com/datasets/sbhatti/financial-sentiment-analysis).<br>
• The data set contains two columns - Sentences and Sentiments.<br>
• Sentiments are converted to int64 data type representing as follows: 0 -> Negative | 1 -> Neutral | 2 -> Positive<br>
• The data is divided in 80-20 split for training and validation respectively.<br>
• Each sentence in Sentences column is converted into token. The tokenize_sentences function takes a list of sentences as input and returns a tuple of three lists: tokenized sentences, token type ids, attention masks.<br>
• It uses the `BertTokenizer` (pre-trained tokenizer) to tokenize sentences.<br>
• The `train_dataset` and `val_dataset` variables are created by calling the `tokenize_and_create_dataset` function on the train data and val data respectively.<br>
• The train dataset is used to train the model, and the val dataset is used to evaluate the model's performance.<br>

### Evalution Metrics
`Training accuracy`: ~83.3%<br>
`Validation accuracy`: ~75.7%<br>
