# **Peer-graded Assignment: Getting and Cleaning Data Course Project**

*This repository contains the files necessary to download, extract, and clean the available dataset from UCI's [Human Activity Recognition Using Smartphones Data Set](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) project.*[^1]

### **Repository Files**

*** 

#### CodeBook.md

*Describes the contents of* run_analysis.R *in greater detail and provides descriptions of variables.*

#### run_analysis.R

*This file acquires the data and performs the approriate analysis. As a note, the libraries 'plyr' and 'dplyr' are required to run this script*

1. Downloads the required [data](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) from UCI.
2. Extracts contents of the .zip file and reads necessary data files into R tables.
3. Appropriately labels data with the provided "features" and "activity labels".
4. Attaches the separate variables "subject", "y", and "X" with `cbind()` and mergers the "training" and "test" data with `rbind()`.
5. Activity labels are substituted into the data set based on their numeric reference value.
6. Extracts the data containing only "mean" and "standard deviation" values.
7. Modifies the variable labels to be descriptive and intuitive.
8. Outputs a *FinalDataset.txt* file with the average of each variable for each activity and each subject.

### **Project Objectives**

***

- [X] Merges the training and the test sets to create one data set.
- [X] Extracts only the measurements on the mean and standard deviation for each measurement.
- [X] Uses descriptive activity names to name the activities in the data set.
- [X] Appropriately labels the data set with descriptive variable names.
- [X] Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

[^1]: *All work described herein has been completed by Kyle Rozic.*