# Personalised-Cancer-Diagnosis
# Conclusion and Steps Followed :
1. Determined the set of Business objectives of Problem such as Low latency requirement,interpretability etc.    
2. Problem Statement is defined and converted the real world problem into Machine Learning Problem through set of objectives                     
3. Identified it as Multiclass Classification Problem with Nine classes.     
4. Decided our KPI's to be a> Multiclass Log loss  and b>Confusion Matrix.                  
5. Because Given Data is not Temporal Data hence we splitted into 64:16:24 corresponding to Train,CV and Test data Randomly by ensuring each of them will get similar distributions of classes.                    
6. Through Distributions of these 3 types of splits we observed it as imbalanced Dataset and are distributed similarly in all of these types.        
7. To Decide the threshold value of log-loss to evaluate performance of model,we made a random model and generated its log-loss using random numbers(from Normal Distribution).                              
8. We converged to threshold value of log-loss to be 2.5.                     
9. We performed univariate analysis on Gene,Variation and Text Features to identify how much they are contributing to predict the class label.                         
10. We observed all are to be stable features with best feature among them as Gene Feature in predicting model.         
11. As both gene and Variation are categorical random variables we have featurised by one-hot encoding(TF-idf vectorizer) and Response coding.Text Feature is also featurised by one hot encoding(TF-idf vectorizer) and Response encoding.           
12. Then through Stacking of these featurised data , we have trained models using certain algorithms which gives results accoridng to our problem objectives.                           
13. Types of Models trained and Results are shown in first table below as part of Task 1 results.                 
14. we observe that Logistic Regression(one hot encoding) and KNN(Response encoding) works well.                      
15. Then instead of using all the feature words we have used top 2000 words having high tfidf values.we observed the results are quite improved from first procedure.                                   
16. Results are showed as part of Task 2 table where we observe logistic regression performs better than other models.     
17. we tried with other feature engineering techniques such as bi-grams(1,2),tri-grams(1,2,3) and four grams(1,2,3,4) to reduce the log-loss less than to 1 using count vectoriser.these results can be seen as part of Task 3.               
18. But we couldn't reduce the log-loss value to less than to one.                              
19. Then with basic Feature Engineering Techniques such as Frequency of occurences for Gene and Variation Feature,string Length and number of words in Text Features,sticking to top 2000 words using max_feature parameter(uses tfidf score) in Tfidf vectorizer we trained Logistic Regression Model .                      
20. Finally its value got reduced to under 1.These values are shown as part of Task-4 Results.             
                      
