# Binary-student-classification-of-Twitter-users

Steps:

1. Install R.
2. Install Rstudio.

3. Load the User data into the workspace(Rda files). 
   command:load("FinalDataSet.Rda")

FinalDataSet.Rda contains:
- features.final - dataframe containing final features of all 304 users and student data tagging for use with "Model Training and Testing.Rmd"
- streamusers.nonstudents - dataframe containing list of stream twitter users profile info for use with "Feature_Creation.Rmd"
- (streamusers.students, unccuser.students, unccusers.nonstudents not included but can be made available if necessary)

***
Warning, this step will take a long time due to fetching of thousands of user tweets.
Skip to step 8 and use features.final for classification training and testing
***
4. Create Features for both students and non students:
   a. Open the "Feature_Creation.Rmd" file.
   b. assign students user dataframe name to twitter_user_data.
   c. assign new students feature dataframe name to ns_metrics_working.(Example name: student_features)
   d. run the notebook by selecting run all.
   e. repeat steps b-d for nonstudents (user files not included)

**
Steps 5-7 continues with final features datafile creation but can be skipped
(requires datafile not included with submission - can be made available if necessary)
**
5. add a column to student_features with value 1. (student_features$student <- 1)
6. add a column to student_features with value 1. (nonstudent_features$student <- 0)
7. combine ns_non_student_metrics and ns_student_metrics dataframe using rbind. (features.all <- rbind(student_features,nonstudent_features))

***
classifier training and testing
**
8. open "Model Training and Testing.Rmd"
9. change first line of code to read "working_dataset <- features.final"
10. run all code and observe results of classification


