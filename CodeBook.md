CodeBook

Data Information

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.
 
For more info a full description is available at the site where the data was obtained: 
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
The data are obtained from:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Code Information

Meets the criteria of the following course objectives:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names.
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

code procedure
1. Merges the training and the test sets to create one data set.
step 1. Set work directory;
step 2. Download the zip file from the website;
step 3. Unzip the data;
step 4. Load the data into R:
    4.1 load the training datasets into R;
    4.2 load the test datasets into R;
step 5. merge train and test data,using cbind and rbind, to create "full" with all data

2. Extracts only the measurements on the mean and standard deviation for each measurement.
step 1. Load the feature name into R,using read.table;
step 2. Extract mean and standard deviation of each measurements,
    2.1 Create vector identifying mean and std
    2.2 Extract column names

3. Uses descriptive activity names to name the activities in the data set.
step 1. Load the activity data into R,create "activityName" ;
step 2. Replace 1 to 6 with activity names;

4. Appropriately labels the data set with descriptive variable names.

5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
step: Write the dataset to .txt file

