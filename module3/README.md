# Module 3: Regression 2
## Module Content
This module is labeled "Regression 2" in continuation of Module 2. It features 10 mini-lectures on the following topics:
1. Bayes Linear Regression 1
2. Bayes Linear Regression 2
3. Uses of Posterior Distribution
4. Active Learning 1
5. Active Learning 2
6. Linear Regression-2
7. Tools: Analysis
8. Tools: Lagrange Multipliers
9. Sparse Regression
10. Regression

## Project File Details
X_train.csv: A comma separated file containing the covariates. Each row corresponds to a single vector x_i.

y_train.csv: A file containing the outputs. Each row has a single number and the i-th row of this file combined with the i-th row of "X_train.csv" constitutes the training pair (x_i, y_i).


X_test.csv: This file follows exactly the same format as "X_train.csv". No class file is given for the testing data.

## Notes
The UCI Machine Learning Repository (http://archive.ics.uci.edu/ml/Links to an external site.) has a good selection of datasets for regression. While you still may not have the ground truth, you can build confidence that the outputs of your code are reasonable. For example, you can verify that your vector makes reasonable predictions and that your 10 selected measurement indexes are all unique.

## Project FAQs

FAQ 1: How to read the files? Can we use pandas?

Note the code to read the files are already given.

X_train = np.genfromtxt(sys.argv[3], delimiter = ",")
y_train = np.genfromtxt(sys.argv[4])
X_test = np.genfromtxt(sys.argv[5], delimiter = ",")
Please use this code, to appropriately read the data. This will ensure that each row of X_train and X_train is a vector and y_train’s each row is a scalar float.

 

FAQ 2: How to save the output?

See the following code - 

wRR = part1()  # Assuming wRR is returned from the function

np.savetxt("wRR_" + str(lambda_input) + ".csv", wRR, delimiter="\n") # write output to file

active = part2()  # Assuming active is returned from the function

np.savetxt("active_" + str(lambda_input) + "_" + str(int(sigma2_input)) + ".csv", active, delimiter=",") # write output to file
It already prints the data in a proper format.

 

FAQ 3: What are we supposed to output for task 2?
Index of X vectors where you will find the ground truth. Ie points of maximum uncertainty.

 

FAQ 4: What floating point precision levels to use?

Use standard floats for weight vectors. For locations (part 2) you can use integer.

 

FAQ 5: What Python version to use?

Only use python 3.x.

 

FAQ 6: What libraries can we use?

For this problem, only NumPy is needed. Other non-standard libraries might not work.

 

FAQ 7: Where to get test data sets?

You can get various regression data sets from here: http://archive.ics.uci.edu/ml/Links to an external site.

 

FAQ 8: Can we submit any number of times? 

You can submit any number of times.

 

FAQ 9: What does this error mean?

## standardization formula ##
error: dlmread: unable to open file 'active_8_3.csv'
In general, this error comes from the grader. But this does not mean the file is unreadable. Normally the file is not created at all, as your code might have an early exit due to some exception. You should do exception handling to see what exactly is the error.

 

FAQ 10: What exactly to do in Part 2?

Compute the covariance matrix. Select the location which maximizes uncertainty. Update the covariance matrix. Among the remaining points, select the index of the one which again maximizes uncertainty. Update covariance. And so on.
