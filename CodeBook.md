---
title: "CodeBook.md"
author: "Gaurav Lamba"
date: "Sunday, September 21, 2014"
output: html_document
---

Getting and Cleaning Data Course Project: Codebook
Introduction

This file describes the original data set, the variables of the clean data set and the analysis script which contains transformations or work that we performed to clean up the data.

Data Source

The original dataset is derived from the "Human Activity Recognition Using Smartphones Data Set" which was originally made available here:
  
  http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones.

More specifically, the data set for the project is here:
  
  https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

This data set is split into a training and a test set (70% and 30%, respectively). Each part is also split into three files that contains the measurements from the accelerometer and gyroscope, activity label and an identifier for the subject. In other words, the dataset included the following data files:
  
  features.txt: List of all features.
activity_labels.txt: List of class labels and their activity name.
train/X_train.txt: Training set.
train/y_train.txt: Training labels.
train/subject_train.txt: ID's of subjects in the training data.
test/X_test.txt: Test set.
test/y_test.txt: Test labels.
test/subject_test.txt: ID's of subjects in the training data
Tidy Dataset

The final and clean tidy dataset will be a dataframe 
  
subject: ID the subject who performed the activity for each window sample. Its range is from 1 to 30.

activity: Descriptive name of each subject's activity. The factor values are WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING.

The selection of the remaining variables is based on the features.txt file where we extracts only the measurements on the mean and standard deviation for each measurement according to the assignment. For this reason, we included all variables having to do with mean or standard deviation. For each variable we report the average for each activity and each subject.
