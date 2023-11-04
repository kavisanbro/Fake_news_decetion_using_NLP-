# Fake_news_detectioNLP-Project-Fake-News-Detection

Dataset Used : LIAR Dataset
Data : https://www.kaggle.com/code/dillkrish/fake-vs-real-news-detection-bert-acc-100

Original Source:
The paper did not release the source code.

List of commands:
Run all the cells in the ipython notebook.

Train :
function : train(model,architecture, use_pos, use_meta, use_dep)

params :
model : keras Sequential model
architecture : 'lstm' or 'cnn'
use_pos : boolean (tells whether the POS embeddings are to be used as input to the model for training)
use_meta : boolean (tells whether the metadata is to be used as input to the model for training)
use_dep : boolean (tells whether the Dependency parse embeddings are to be used as input to the model for training)
Evaluation on test:
function_1 : (false_predicted,true_predicted) = evaluate(model, use_pos, use_meta, use_dep)

params :
model : keras Sequential model
use_pos : boolean (tells whether the POS embeddings were used as input to the model while training)
use_meta : boolean (tells whether the metadata was used as input to the model while training)
use_dep : boolean (tells whether the Dependency parse embeddings were used as input to the model while training)
returns :
false_predicted : dictionary with keys as indices of test samples that were classified as "pants-on-fire" (false news) and values as the softmax probability for this class label.
true_predicted : dictionary with keys as indices of test samples that were classified as "true" (not a fake news) and values as the softmax probability for this class label.
function_2 : print_best_false_true_predicted(false_predicted,true_predicted)

params :
outputs from the above mentioned evaluate() function.
outputs :
prints top 5 sentences which where predicted as "pants-on-fire" (fake news) with highest softmax probabilities.
prints top 5 sentences which where predicted as "true" (not fake news) with highest softmax probabilities.
Software and Library Requirements:
Keras==2.2.2
matplotlib==2.1.2
numpy==1.15.4
pandas==0.22.0
pydot==1.4.0
scikit-learn==0.19.1
scipy==1.0.0
sklearn==0.0
spacy==2.0.18
tensorboard==1.9.0
tensorflow==1.9.0
spacy==2.0.18
nltk==3.4
