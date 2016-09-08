# Codebook

My tidy data set taken from http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones .

## Original Study Design

The UCI HAR data set, upon which our study is based, contains the following description of how the original study was conducted (from its readme.txt):

> The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

> The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details.

## Tidy Data Study Design

1. Merges the training and the test sets to create one data set.
  I downloaded the UCI HAR data set. Since the data set is spread over a number of separate files, it was necessary to reassemble it.
  I combined the subjects, the observations, and the list of activities [using the files subject_.txt, X_.txt, and y_*.txt] into a single data.table, then applied the column names and factored the activity column using the provided activity labels (the features.txt and activity_labels.txt files).
  I repeated this for both the train and test subsets and then combined the subsets into a final data.table.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
 I removed all columns where the original name did not contain -std or -mean. 
3.Uses descriptive activity names to name the activities in the data set.
 I have renamed the metrics column names to make them more descriptive and human readable.
 
Appropriately labels the data set with descriptive variable names.
From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
2.**acivity** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
3.**meanmeanBodyAccX** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
4.**meanmeanBodyAccZ** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
5.**stdBodyAccX** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
6.**stdBodyAccZ** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
7.**meanmeanGravityAccX** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
8.**meanmeanGravityAccZ** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
9.**stdGravityAccX** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
10.**stdGravityAccZ** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
11.**meanmeanBodyAccJerkX** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
12.**meanmeanBodyAccJerkZ** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
13.**stdBodyAccJerkX** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
14.**stdBodyAccJerkZ** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
15.**meanmeanBodyGyroX** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
16.**meanmeanBodyGyroZ** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
17.**stdBodyGyroX** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
18.**stdBodyGyroZ** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
19.**meanmeanBodyGyroJerkX** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
20.**meanmeanBodyGyroJerkZ** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
21.**stdBodyGyroJerkX** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
22.**stdBodyGyroJerkZ** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
23.**meanmeanBodyAccMag** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
24.**stdBodyAccMag** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
25.**meanmeanBodyAccJerkMag** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
26.**stdBodyAccJerkMag** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
27.**meanmeanBodyGyroJerkMag** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
28.**stdBodyGyroJerkMag** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
29.**meanmeanBodyAccY** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
30.**stdBodyAccY** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
31.**meanFreqBodyAccY** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
32.**meanmeanBodyAccJerkX** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
33.**meanmeanBodyAccJerkZ** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
34.**stdBodyAccJerkX** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
35.**stdBodyAccJerkZ** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
36.**meanFreqBodyAccJerkX** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
37.**meanFreqBodyAccJerkZ** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
38.**meanmeanBodyGyroY** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
39.**stdBodyGyroY** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
40.**meanFreqBodyGyroY** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
41.**meanmeanBodyAccMag** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
42.**stdBodyAccMag** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
43.**meanFreqBodyAccMag** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
44.**meanmeanBodyBodyGyroMag** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
45.**stdBodyBodyGyroMag** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
46.**meanFreqBodyBodyGyroMag** (number) - The mean of the tBodyAcc-mean()-X variable from the UCI HAL data set
