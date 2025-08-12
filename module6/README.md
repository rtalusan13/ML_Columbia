# Module 6: Extended Classification

## Module Content

This module is labeled "Extended Classification" in continuation of Modules 4&5. It features 8 mini-lectures on the following topics:

1. Maximum Margin Classifiers
2. Support Vector Machines
3. Primal and Dual Problems
4. Soft-Margin SVM
5. Decision Trees
6. Basic Decision Tree Learning Algorithm
7. The Bootstrap
8. Bagging and Random Forest

## Notes
The UCI Machine Learning Repository (http://archive.ics.uci.edu/ml/Links to an external site.) has a good selection of datasets for classification. While you still may not have the ground truth, you can build confidence that the outputs of your code are reasonable.


## Project FAQs
*1: What should I name my script before running executing?*

- You need to rename the script as hw2_classification.py before running it. 

*2: Why do I keep getting a singular matrix error? When I calculate the determinant of the covariance matrix using np.linalg.det(), I keep getting a value of zero for all of my classes. Has anyone had any luck troubleshooting this problem?*

- One thing you can try is to simply reset the mean and covariance to some value when you encounter a singular matrix error. Also, double-check your code to make sure your updates are being done properly.

*3: I always got the error "Your output file does not follow the correct naming format." in the Week 6 project, please help to advise why it is "Your output file does not follow the correct naming format"?*

- The reason why you are getting this error is because the script actually never executed to beyond import package lines. Sklearn should not be used in this assignment as the purpose of this assignment is to let you build those functions from scratch to further enhance your understanding of the concept of K-class Bayes classifier. Please try to finish the assignment with numpy package which is definitely sufficient for this task.
