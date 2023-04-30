# Text Classification (Data Science)

![image](https://user-images.githubusercontent.com/68069100/235378909-c51248d2-6773-4bc3-b5f3-da14d1cef8fe.png)

## Problem Statement

To perform a text classification on consumer complaint dataset into following categories 

0 Credit reporting, repair, or other
1 Debt Collection
2 Consumer Loan 
3 Mortgage 

## Index 

* Dataset
* EDA 
* Text Pre- Processing 
* Multi Classification model
* Comparison of model performance and Model Evaluation
* Prediction 
* References

## Dataset 

Data set used -- click this [link](https://catalog.data.gov/dataset/consumer-complaint-database)

Dataset is not included in this repository due to it's large size. 

Dataset after extracting the required columns 

![Screenshot (147)](https://user-images.githubusercontent.com/68069100/235378868-64ad383e-51bb-4b36-bcf6-5266917bcb02.png)

Product (Categories) we need 

![Screenshot (148)](https://user-images.githubusercontent.com/68069100/235378881-711f5dd6-971a-43ca-972d-b5bd1b9b9248.png)


## EDA 

Explanatory Data Analysis 

Number of complaints Vs Product (Categories)  

![output_15_1](https://user-images.githubusercontent.com/68069100/235378265-e6830d70-e559-4889-a445-aa813b5e766a.png)

From the above, we can conclude: 
- Complaints regarding `Credit reporting, repair, or other` are the highest
- Complaints regarding `Consumer Loan` are the least 

Viz. for the whole dataset (sampled) with all Product

![output_16_1](https://user-images.githubusercontent.com/68069100/235378479-97505ef5-8f2e-44e6-bb5a-86c3ab3ba568.png)

Two models used: 
To train and fit the data - LinearSVC: The objective of a Linear SVC (Support Vector Classifier) is to fit to the data you provide, returning a best fit hyperplane that divides, or categorizes, your data.

Naive Bayes is a powerful algorithm that is used for text data analysis and with problems with multiple classes: MultinomialNB 

![output_23_0](https://user-images.githubusercontent.com/68069100/235378773-8388d468-5c31-4479-a9e9-50a82bf50a5c.png)


Actual Vs Predicted (heatmap) 

![output_26_0](https://user-images.githubusercontent.com/68069100/235378788-a30c8ef7-d109-403e-9362-76ad4f850f20.png)

## Text Preprocessing

Text should be processed to vectors so that it is readable by the model and make predictions. Term Frequency - Inverse Document Frequency [(TF-IDF)](https://www.learndatasci.com/glossary/tf-idf-term-frequency-inverse-document-frequency/) is a widely used statistical method in natural language processing and information retrieval. It measures how important a term is within a document relative to a collection of documents (i.e., relative to a corpus). Importance of a word is determined in terms of frequency. Hence, the name is justified. 

## Multi Classification model 

Classification models used are : 

- LinearSVC
- MultinomialNB 

Resources to study the above: 
1. [LinearSVC](https://scikit-learn.org/stable/modules/generated/sklearn.svm.LinearSVC.html)
2. [LinearSVC II](https://pythonprogramming.net/linear-svc-example-scikit-learn-svm-python/#:~:text=The%20objective%20of%20a%20Linear,the%20%22predicted%22%20class%20is.)
3. [Learning from LinearSVC example](https://www.datatechnotes.com/2020/07/classification-example-with-linearsvm-in-python.html)
4. [MultinomialNB](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.MultinomialNB.html#:~:text=The%20multinomial%20Naive%20Bayes%20classifier,tf%2Didf%20may%20also%20work.)
5. [MultinomialNB II](https://www.upgrad.com/blog/multinomial-naive-bayes-explained/)

## Comparison of models performance and model Evaluation

The data was divided into features(X) and target(Y), further split into train data(75%) and test(25%). We all know how train and test works! Trained data is tested on test the data from dataset but unknown to the model. (To put in simple terms)

- Mean Accuracy and Standard deviation was calculated. 
- Finding the three most correlated terms with each of the product categories. Complaints by consumer for a certain product category with most of these terms. 
- Precision was determined (Refer to jupyter notebook) 

More the sampled data, more will be the precision. 

It's is also appropriately depicted in confusion matrix (refer to EDA section) 

## Predictions

The final result are as follows : 

![Screenshot (149)](https://user-images.githubusercontent.com/68069100/235379485-2a45ce25-afab-4531-aa38-f768fcc8e6fe.png)

## References: 

* [Random State](https://medium.com/mlearning-ai/what-the-heck-is-random-state-24a7a8389f3d)
* [TF-IDF](https://www.geeksforgeeks.org/tf-idf-for-bigrams-trigrams/)
* [For syntax](https://stackoverflow.com/questions/27697766/understanding-min-df-and-max-df-in-scikit-countvectorizer)
* [Confusion Matrix](https://towardsdatascience.com/understanding-confusion-matrix-a9ad42dcfd62)
* [Multi-class text classification](https://towardsdatascience.com/multi-class-text-classification-model-comparison-and-selection-5eb066197568)





