Getting and Cleaning Data Course Project Documentation


Created By Shilpi Bhatnagar

Purpose
-----------

It describes the variables, the data, and any transformations or work that is performed to clean up the data.


Location of Source Data

A full description of the data used in this project can be found at [The UCI Machine Learning Repository](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

[The source data for this project can be found here.](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)


1. Started with merging the data files into one dataset which would be required later for analysis purposes.
---------------------------------------------------------------
The following files have been read firstly into separate files each:
- x_train.txt
- y_train.txt
- subject_train.txt
- x_test.txt
- y_test.txt
- subject_test.txt
- features.txt
- activity_labels.txt


Then merged the test and train datasets into a single table with rbind function.

2. We pulled only the mean and standard deviation measurements from the table. 
-----------------------------------------------------------------------------------------

Using grep we extracted all mean and std data from the merged dataset.


3. Set activity names in the data set
------------------------------------------------------------------------
Joined data subset with the activityType table to include the descriptive activity names. 

4. Set labels on the dataset with descriptive variable names
--------------------------------------------------------------------
The gsub function was used to clean up the variable names having special characters in between.

5. Create a second tidy data set having the average of each variable for each activity and each subject. 
----------------------------------------------------------------------------------------
Using the aggregate function for the variables a single table containing the averages and means was created.(second_set.txt)


