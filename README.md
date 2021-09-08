# Sentiment-Analysis
NLP course final project

This project is focusing on text classification using pretrained transformers and configurations of them trying to achieve the best possible accuracy
for different datasets, get some insights about the data and exploring advantages and disadvantages for each approach.
The main differences between the network that were trained:
1. Using different pretrained models (BERT, RoBERTa, XLNet): Exploring different architectures and check which of them will be more appropriate for classification task or more compatible to our datasets.
2. Using different versions of the pretrained models: Checking the trade off between large models with many parameters which consumes a lot of time to train and the accuracy.
3. Training the whole model vs training only the classification layer: As in 2, when updating less parameters we expect shorter training time and lower accuracy. If training is significantly shorter and the accuracy decreases in a conceivable way maybe finetuning only the last layer is more reasonable for some tasks.
4. Using different hyperparameters for each network: Exploring different hyperparameters such as learning rate, batch size etc and their effect on running time and accuracy.

In order to add some creativity for this project, we tried to explore if it is possible to use our fine tuned model for unsupervised classification tasks.
To do so we implemented feature extraction from the last layer of the model, then we did dimensionality reduction using TSNE and then applying clustering algorithm using most of the times GMM (since it gave the best results).
Doing feature extraction also helped us to visualize and better understand the data distribution.
