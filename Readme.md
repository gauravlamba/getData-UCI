---
title: "Readme.md"
author: "Gaurav Lamba"
date: "Sunday, September 21, 2014"
output: html_document
---

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
 