Description
I started this project after watching "Machine Learning for Everybody - Full Course" by freeCodeCamp.org. In this video, Kylie Ying very clearly breaks down each of the models, how they work, and how effective each of them is. She takes us through some simple examples using some datasets from the UCI Machine Learning Repository. She first talks about the theory behind the model and then shows us how to use the model in an ipynb environment (she uses Google Colab for this). My objective for this project was to take the principles taught in the video and apply them to a separate dataset. 

Results
When the models had been created, it was apparent that any of them would accomplish the desired task. The Neural Network model had the best accuracy score with an accuracy of 84%. 

Other notable mentions are:
Support Vector Machines - Highest precision (95%) when it comes to classifying a person who makes less than $50k 
Naive Bayes - Highest recall (93%) when it comes to classifying a person who makes less than $50k
Naive Bayes - Highest precision (67%) when it comes to classifying a person who makes greater than or equal to $50k
Support Vector Machines - Highest recall (87%) when it comes to classifying a person who makes greater than or equal to $50k

Implications
When you need a model to predict if someone's yearly income was less than $50,000 based on the dataset given and we wanted to minimize the number of false positives, it would be best to use the Support Vector Machines model. This model was the most precise when classifying people who made less than $50k. This means that of all the people that were classified as making more than or equal to $50k, this model had the least number of incorrectly classified persons. 

On the other hand, if you wanted to minimize the number of false positives, it would be best to use the Naive Bayes model to classify someone who makes less than $50k. This model has the highest recall when it comes to classifying a person who makes less than $50k. This means that of all the people who actually made less than $50k, this model correctly classified the most. 

Both would be very useful in specific scenarios where you would want to prioritize either precision or recall over the other; however, when we calculate the harmonic mean (f1-score), we see that the Neural Network was the best model for classifying people who made less than $50k. If we wanted the model that could best classify people who made greater than or equal to $50k, we would use the Support Vector Machines model as it had the highest f1-score for that target value. 

Finally, if we wanted the model that penalized False Negatives and False Positives the most, we would look at the f1-score. Alternatively, if we wanted to use the model that rewarded True Positives and True Negatives the most, we would look at the accuracy. The Neural Network had the best accuracy, but as we have seen, that does not always mean it's the best model. 


Files: 1994_census.ipynb, adult.data, readme.md
