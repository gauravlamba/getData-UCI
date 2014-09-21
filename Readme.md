---
title: "Readme.md"
author: "Gaurav Lamba"
date: "Sunday, September 21, 2014"
output: html_document
---
The original dataset has following  files:

'features.txt': List of all features.

'activity_labels.txt': List of class labels and their activity name.

'train/X_train.txt': Training set.

'train/y_train.txt': Training labels.

'train/subject_train.txt': ID's of subjects in the training data

'test/X_test.txt': Test set.

'test/y_test.txt': Test labels.

'test/subject_test.txt': ID's of subjects in the training data


The cleanup script (run_analysis.R) does the following:

- Merges the training and the test sets to create one data set.
- Extracts only the measurements on the mean and standard deviation for each measurement.
- Uses descriptive activity names to name the activities in the data set
- Appropriately labels the data set with descriptive activity names.
- Creates a tidy data set with the average of each variable for each activity and each subject.

Steps:
 1. Program requires reshape2 and data.table packages
 
 2. Read activity labels and features from respective files in the same directory
 
 3. Extract feature which are either mean or std deviation
 
 4. Load activity labels
 
 5. Put the subject Ids and column bind test data
 
 6. Repeat same steps for train data
 
 7. Join test and train data
 
 8. label the data set with descriptive activity names.
 
 9. Rejoin the entire table, grouping by subject/acitivity pairs, applying the mean function which creates the clean dataset.
 
 10. Write the clean data set with "row.names=FALSE"
 