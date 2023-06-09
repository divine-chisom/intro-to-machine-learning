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
### Deploy an RBF Kernel
- Keep the training set slice code from the last quiz, so that you are still training on only 1% of the full training set. Change the kernel of your SVM to “rbf”. **What’s the accuracy now, with this more complex kernel?**

```
No. of Chris training emails :  7936
No. of Sara training emails :  7884
Training Time: 0.073 s
Predicting Time: 0.998 s
0.8953356086461889
```
### Optimize C Parameter
- Keep the training set size and rbf kernel from the last quiz, but try several values of C (say, 10.0, 100., 1000., and 10000.). **Which one gives the best accuracy?**

### Accuracy after Optimizing C
- Once you've optimized the C value for your RBF kernel, **what accuracy does it give? Does this C value correspond to a simpler or more complex decision boundary?**

```
No. of Chris training emails :  7936
No. of Sara training emails :  7884
Training Time: 0.069 s
Predicting Time: 1.453 s
0.8998862343572241
```
### Optimized RBF vs. Linear SVM: Accuracy
- Now that you’ve optimized C for the RBF kernel, go back to using the full training set. In general, having a larger training set will improve the performance of your algorithm, so (by tuning C and training on a large dataset) we should get a fairly optimized result. **What is the accuracy of the optimized SVM?**

```
No. of Chris training emails :  7936
No. of Sara training emails :  7884
Training Time: 99.182 s
Predicting Time: 15.828 s
0.9960182025028441
```

### Extracting Predictions from an SVM
- What class does your SVM (0 or 1, corresponding to Sara and Chris respectively) predict for element 10 of the test set? The 26th? The 50th?

```
No. of Chris training emails :  7936
No. of Sara training emails :  7884
Training Time: 0.064 s
Predicting Time: 0.953 s
0.8998862343572241
1
0
1
```
### How Many Chris Emails Predicted?
- There are over 1700 test events--how many are predicted to be in the “Chris” (1) class? (Use the RBF kernel, C=10000., and the full training set.)
```
No. of Chris training emails :  7936
No. of Sara training emails :  7884
Training Time: 99.496 s
Predicting Time: 16.574 s
0.9960182025028441
866
```