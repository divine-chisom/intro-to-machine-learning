ud120-projects
==============

## intro-to-machine-learning

### Author ID Accuracy
- Create and train a Naive Bayes classifier in naive_bayes/nb_author_id.py. Use it to make predictions for the test set. **What is the accuracy?**

```
No. of Chris training emails :  7936
No. of Sara training emails :  7884
Training Time: 2.067 s
Predicting Time: 0.194 s
0.9732650739476678
```
### SVM Author ID Accuracy
- Import, create, train and make predictions with the sklearn SVC classifier. When creating the classifier, use a linear kernel (if you forget this step, you will be unpleasantly surprised by how long the classifier takes to train). **What is the accuracy of the classifier?**

```
No. of Chris training emails :  7936
No. of Sara training emails :  7884
0.9840728100113766
```
### SVM Author ID Timing
- Place timing code around the fit and predict functions, like you did in the Naive Bayes mini-project. **How do the training and prediction times compare to Naive Bayes?**

```
No. of Chris training emails :  7936
No. of Sara training emails :  7884
Training Time: 98.024 s
Predicting Time: 9.345 s
0.9840728100113766
```
### A Smaller Training Set
- features_train = features_train[:len(features_train)/100]
labels_train = labels_train[:len(labels_train)/100]

These lines effectively slice the training dataset down to 1% of its original size, tossing out 99% of the training data. You can leave all other code unchanged. **What’s the accuracy now?**

```
No. of Chris training emails :  7936
No. of Sara training emails :  7884
Training Time: 0.068 s
Predicting Time: 0.536 s
0.8845278725824801
```

