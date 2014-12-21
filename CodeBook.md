#### Description

This document serves as a "code book" for the generation of a tidy dataset reflecting a subset of data from the "Human Activity Recognition Using Smartphones Data Set" housed at the UCI Machine Learning Repository.  

You can access the dataset at this world wide web (www) link:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

You can directly access the "Human Activity Recognition Using Smartphones Data Set" data as a compressed file at this world wide web (www) link:

https://d396qusza40orc.cloudfront.net/getdata/projectfiles/UCI%20HAR%20Dataset.zip

You can find more information about the UCI Machine Learning Repository at this world wide web (www) link:

http://archive.ics.uci.edu/ml/about.html

#### Assumptions

Please note these assumptions when inspecting the tidy dataset and executing the R programming language script that generates the tidy dataset.

* An R language script was developed to generate the tidy dataset.
* Included in this package is a compressed file that contains raw data used to create the tidy data set. The compressed file was downloaded at this time: `Friday, December 19, 2014 at 19:52 UTC`.  See the `getdata-projectfiles-UCI HAR Dataset.zip` file.
* The tidy dataset includes a subset of the subject, activity, and measurements
* See the `README.txt` file included in the raw dataset for information on the "Human Activity Recognition Using Smartphones Data Set".  It is also reproduced in the appendix below for your convenience.

#### Data Transformations

These high level transformations are conducted on the raw data to produce the tidy data set.

1. The 'test' and 'train' data sets are merged into one result set
1. Only variables containing means and standard deviations of measurements are included.  All other measurements are excluded from the tidy data set
1. The 'SubjectId' (e.g. "3") and 'Activity' (e.g. "WALKING") are merged into the tidy data set.  For each observation, the 'SubjectId' identifies the person conducting the activity and the 'Activity' describes the subject's physical activity when the observation data was captured
1. Each variable is averaged (arithmetic mean) across all observations by SubjectId and Activity

See the `README.md` file for a detailed description of how to execute the tidying process and the operations executed by the R script on the raw data.  

#### Variables

Listed below are the variables generated during the tidy process and included in the tidy dataset.  This data file can be found in your R working directory after executing the `run_analysis.R` script.

* `tidy_output/HumanActivitySmartphonesDataSet_Average_TidyData.txt`

*NOTE*: See the "Human Activity Recognition Using Smartphones Data Set" `README.txt` file for more information on the data stored in these variables including units.

| Column # | Name                                      | Description                                                                    |
|----------|-------------------------------------------|--------------------------------------------------------------------------------|
| 1        | SubjectId                                 | "Number uniquely identifying the test subject (person acting with the device)" |
| 2        | Activity                                  | "Physical activity conducted by the test subject"                              |
| 3        | Avg: tBodyAcc-mean()-X                    | Arithmetic mean of variable tBodyAcc-mean()-X                                  |
| 4        | Avg: tBodyAcc-mean()-Y                    | Arithmetic mean of variable tBodyAcc-mean()-Y                                  |
| 5        | Avg: tBodyAcc-mean()-Z                    | Arithmetic mean of variable tBodyAcc-mean()-Z                                  |
| 6        | Avg: tBodyAcc-std()-X                     | Arithmetic mean of variable tBodyAcc-std()-X                                   |
| 7        | Avg: tBodyAcc-std()-Y                     | Arithmetic mean of variable tBodyAcc-std()-Y                                   |
| 8        | Avg: tBodyAcc-std()-Z                     | Arithmetic mean of variable tBodyAcc-std()-Z                                   |
| 9        | Avg: tGravityAcc-mean()-X                 | Arithmetic mean of variable tGravityAcc-mean()-X                               |
| 10       | Avg: tGravityAcc-mean()-Y                 | Arithmetic mean of variable tGravityAcc-mean()-Y                               |
| 11       | Avg: tGravityAcc-mean()-Z                 | Arithmetic mean of variable tGravityAcc-mean()-Z                               |
| 12       | Avg: tGravityAcc-std()-X                  | Arithmetic mean of variable tGravityAcc-std()-X                                |
| 13       | Avg: tGravityAcc-std()-Y                  | Arithmetic mean of variable tGravityAcc-std()-Y                                |
| 14       | Avg: tGravityAcc-std()-Z                  | Arithmetic mean of variable tGravityAcc-std()-Z                                |
| 15       | Avg: tBodyAccJerk-mean()-X                | Arithmetic mean of variable tBodyAccJerk-mean()-X                              |
| 16       | Avg: tBodyAccJerk-mean()-Y                | Arithmetic mean of variable tBodyAccJerk-mean()-Y                              |
| 17       | Avg: tBodyAccJerk-mean()-Z                | Arithmetic mean of variable tBodyAccJerk-mean()-Z                              |
| 18       | Avg: tBodyAccJerk-std()-X                 | Arithmetic mean of variable tBodyAccJerk-std()-X                               |
| 19       | Avg: tBodyAccJerk-std()-Y                 | Arithmetic mean of variable tBodyAccJerk-std()-Y                               |
| 20       | Avg: tBodyAccJerk-std()-Z                 | Arithmetic mean of variable tBodyAccJerk-std()-Z                               |
| 21       | Avg: tBodyGyro-mean()-X                   | Arithmetic mean of variable tBodyGyro-mean()-X                                 |
| 22       | Avg: tBodyGyro-mean()-Y                   | Arithmetic mean of variable tBodyGyro-mean()-Y                                 |
| 23       | Avg: tBodyGyro-mean()-Z                   | Arithmetic mean of variable tBodyGyro-mean()-Z                                 |
| 24       | Avg: tBodyGyro-std()-X                    | Arithmetic mean of variable tBodyGyro-std()-X                                  |
| 25       | Avg: tBodyGyro-std()-Y                    | Arithmetic mean of variable tBodyGyro-std()-Y                                  |
| 26       | Avg: tBodyGyro-std()-Z                    | Arithmetic mean of variable tBodyGyro-std()-Z                                  |
| 27       | Avg: tBodyGyroJerk-mean()-X               | Arithmetic mean of variable tBodyGyroJerk-mean()-X                             |
| 28       | Avg: tBodyGyroJerk-mean()-Y               | Arithmetic mean of variable tBodyGyroJerk-mean()-Y                             |
| 29       | Avg: tBodyGyroJerk-mean()-Z               | Arithmetic mean of variable tBodyGyroJerk-mean()-Z                             |
| 30       | Avg: tBodyGyroJerk-std()-X                | Arithmetic mean of variable tBodyGyroJerk-std()-X                              |
| 31       | Avg: tBodyGyroJerk-std()-Y                | Arithmetic mean of variable tBodyGyroJerk-std()-Y                              |
| 32       | Avg: tBodyGyroJerk-std()-Z                | Arithmetic mean of variable tBodyGyroJerk-std()-Z                              |
| 33       | Avg: tBodyAccMag-mean()                   | Arithmetic mean of variable tBodyAccMag-mean()                                 |
| 34       | Avg: tBodyAccMag-std()                    | Arithmetic mean of variable tBodyAccMag-std()                                  |
| 35       | Avg: tGravityAccMag-mean()                | Arithmetic mean of variable tGravityAccMag-mean()                              |
| 36       | Avg: tGravityAccMag-std()                 | Arithmetic mean of variable tGravityAccMag-std()                               |
| 37       | Avg: tBodyAccJerkMag-mean()               | Arithmetic mean of variable tBodyAccJerkMag-mean()                             |
| 38       | Avg: tBodyAccJerkMag-std()                | Arithmetic mean of variable tBodyAccJerkMag-std()                              |
| 39       | Avg: tBodyGyroMag-mean()                  | Arithmetic mean of variable tBodyGyroMag-mean()                                |
| 40       | Avg: tBodyGyroMag-std()                   | Arithmetic mean of variable tBodyGyroMag-std()                                 |
| 41       | Avg: tBodyGyroJerkMag-mean()              | Arithmetic mean of variable tBodyGyroJerkMag-mean()                            |
| 42       | Avg: tBodyGyroJerkMag-std()               | Arithmetic mean of variable tBodyGyroJerkMag-std()                             |
| 43       | Avg: fBodyAcc-mean()-X                    | Arithmetic mean of variable fBodyAcc-mean()-X                                  |
| 44       | Avg: fBodyAcc-mean()-Y                    | Arithmetic mean of variable fBodyAcc-mean()-Y                                  |
| 45       | Avg: fBodyAcc-mean()-Z                    | Arithmetic mean of variable fBodyAcc-mean()-Z                                  |
| 46       | Avg: fBodyAcc-std()-X                     | Arithmetic mean of variable fBodyAcc-std()-X                                   |
| 47       | Avg: fBodyAcc-std()-Y                     | Arithmetic mean of variable fBodyAcc-std()-Y                                   |
| 48       | Avg: fBodyAcc-std()-Z                     | Arithmetic mean of variable fBodyAcc-std()-Z                                   |
| 49       | Avg: fBodyAcc-meanFreq()-X                | Arithmetic mean of variable fBodyAcc-meanFreq()-X                              |
| 50       | Avg: fBodyAcc-meanFreq()-Y                | Arithmetic mean of variable fBodyAcc-meanFreq()-Y                              |
| 51       | Avg: fBodyAcc-meanFreq()-Z                | Arithmetic mean of variable fBodyAcc-meanFreq()-Z                              |
| 52       | Avg: fBodyAccJerk-mean()-X                | Arithmetic mean of variable fBodyAccJerk-mean()-X                              |
| 53       | Avg: fBodyAccJerk-mean()-Y                | Arithmetic mean of variable fBodyAccJerk-mean()-Y                              |
| 54       | Avg: fBodyAccJerk-mean()-Z                | Arithmetic mean of variable fBodyAccJerk-mean()-Z                              |
| 55       | Avg: fBodyAccJerk-std()-X                 | Arithmetic mean of variable fBodyAccJerk-std()-X                               |
| 56       | Avg: fBodyAccJerk-std()-Y                 | Arithmetic mean of variable fBodyAccJerk-std()-Y                               |
| 57       | Avg: fBodyAccJerk-std()-Z                 | Arithmetic mean of variable fBodyAccJerk-std()-Z                               |
| 58       | Avg: fBodyAccJerk-meanFreq()-X            | Arithmetic mean of variable fBodyAccJerk-meanFreq()-X                          |
| 59       | Avg: fBodyAccJerk-meanFreq()-Y            | Arithmetic mean of variable fBodyAccJerk-meanFreq()-Y                          |
| 60       | Avg: fBodyAccJerk-meanFreq()-Z            | Arithmetic mean of variable fBodyAccJerk-meanFreq()-Z                          |
| 61       | Avg: fBodyGyro-mean()-X                   | Arithmetic mean of variable fBodyGyro-mean()-X                                 |
| 62       | Avg: fBodyGyro-mean()-Y                   | Arithmetic mean of variable fBodyGyro-mean()-Y                                 |
| 63       | Avg: fBodyGyro-mean()-Z                   | Arithmetic mean of variable fBodyGyro-mean()-Z                                 |
| 64       | Avg: fBodyGyro-std()-X                    | Arithmetic mean of variable fBodyGyro-std()-X                                  |
| 65       | Avg: fBodyGyro-std()-Y                    | Arithmetic mean of variable fBodyGyro-std()-Y                                  |
| 66       | Avg: fBodyGyro-std()-Z                    | Arithmetic mean of variable fBodyGyro-std()-Z                                  |
| 67       | Avg: fBodyGyro-meanFreq()-X               | Arithmetic mean of variable fBodyGyro-meanFreq()-X                             |
| 68       | Avg: fBodyGyro-meanFreq()-Y               | Arithmetic mean of variable fBodyGyro-meanFreq()-Y                             |
| 69       | Avg: fBodyGyro-meanFreq()-Z               | Arithmetic mean of variable fBodyGyro-meanFreq()-Z                             |
| 70       | Avg: fBodyAccMag-mean()                   | Arithmetic mean of variable fBodyAccMag-mean()                                 |
| 71       | Avg: fBodyAccMag-std()                    | Arithmetic mean of variable fBodyAccMag-std()                                  |
| 72       | Avg: fBodyAccMag-meanFreq()               | Arithmetic mean of variable fBodyAccMag-meanFreq()                             |
| 73       | Avg: fBodyBodyAccJerkMag-mean()           | Arithmetic mean of variable fBodyBodyAccJerkMag-mean()                         |
| 74       | Avg: fBodyBodyAccJerkMag-std()            | Arithmetic mean of variable fBodyBodyAccJerkMag-std()                          |
| 75       | Avg: fBodyBodyAccJerkMag-meanFreq()       | Arithmetic mean of variable fBodyBodyAccJerkMag-meanFreq()                     |
| 76       | Avg: fBodyBodyGyroMag-mean()              | Arithmetic mean of variable fBodyBodyGyroMag-mean()                            |
| 77       | Avg: fBodyBodyGyroMag-std()               | Arithmetic mean of variable fBodyBodyGyroMag-std()                             |
| 78       | Avg: fBodyBodyGyroMag-meanFreq()          | Arithmetic mean of variable fBodyBodyGyroMag-meanFreq()                        |
| 79       | Avg: fBodyBodyGyroJerkMag-mean()          | Arithmetic mean of variable fBodyBodyGyroJerkMag-mean()                        |
| 80       | Avg: fBodyBodyGyroJerkMag-std()           | Arithmetic mean of variable fBodyBodyGyroJerkMag-std()                         |
| 81       | Avg: fBodyBodyGyroJerkMag-meanFreq()      | Arithmetic mean of variable fBodyBodyGyroJerkMag-meanFreq()                    |
| 82       | Avg: angle(tBodyAccMean,gravity)          | Arithmetic mean of variable angle(tBodyAccMean,gravity)                        |
| 83       | Avg: angle(tBodyAccJerkMean),gravityMean) | Arithmetic mean of variable angle(tBodyAccJerkMean),gravityMean)               |
| 84       | Avg: angle(tBodyGyroMean,gravityMean)     | Arithmetic mean of variable angle(tBodyGyroMean,gravityMean)                   |
| 85       | Avg: angle(tBodyGyroJerkMean,gravityMean) | Arithmetic mean of variable angle(tBodyGyroJerkMean,gravityMean)               |
| 86       | Avg: angle(X,gravityMean)                 | Arithmetic mean of variable angle(X,gravityMean)                               |
| 87       | Avg: angle(Y,gravityMean)                 | Arithmetic mean of variable angle(Y,gravityMean)                               |
| 88       | Avg: angle(Z,gravityMean)                 | Arithmetic mean of variable angle(Z,gravityMean)                               |


#### Appendix

##### "Human Activity Recognition Using Smartphones Data Set" README.TXT

Listed below is the "read me" file included in the raw data set for your convenience.


    ==================================================================
    Human Activity Recognition Using Smartphones Dataset
    Version 1.0
    ==================================================================
    Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.
    Smartlab - Non Linear Complex Systems Laboratory
    DITEN - Universit‡ degli Studi di Genova.
    Via Opera Pia 11A, I-16145, Genoa, Italy.
    activityrecognition@smartlab.ws
    www.smartlab.ws
    ==================================================================

    The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

    The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details.

    For each record it is provided:
    ======================================

    - Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
    - Triaxial Angular velocity from the gyroscope.
    - A 561-feature vector with time and frequency domain variables.
    - Its activity label.
    - An identifier of the subject who carried out the experiment.

    The dataset includes the following files:
    =========================================

    - 'README.txt'

    - 'features_info.txt': Shows information about the variables used on the feature vector.

    - 'features.txt': List of all features.

    - 'activity_labels.txt': Links the class labels with their activity name.

    - 'train/X_train.txt': Training set.

    - 'train/y_train.txt': Training labels.

    - 'test/X_test.txt': Test set.

    - 'test/y_test.txt': Test labels.

    The following files are available for the train and test data. Their descriptions are equivalent.

    - 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.

    - 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis.

    - 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration.

    - 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second.

    Notes:
    ======
    - Features are normalized and bounded within [-1,1].
    - Each feature vector is a row on the text file.

    For more information about this dataset contact: activityrecognition@smartlab.ws

    License:
    ========
    Use of this dataset in publications must be acknowledged by referencing the following publication [1]

    [1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

    This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.

    Jorge L. Reyes-Ortiz, Alessandro Ghio, Luca Oneto, Davide Anguita. November 2012.
