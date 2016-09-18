#**Introduction**

Run_analysis.R - 5 steps described in the course project's definition.

* All the similar data is merged using the rbind() function. These files having the same number of columns and referring to the same entities.
* Only those columns with the mean and standard deviation measures are taken from the whole dataset. After extracting these columns, they are given the correct names, taken from features.txt.
* As activity data is addressed with values 1:6, we take the activity names and IDs from activity_labels.txt and they are substituted in the dataset.
* Correct those columns with vague column names.
* Generate a new dataset with all the average measures for each subject and activity type.  The output file is called tidy_data.txt and upladed to this repo.

#**Variables**

* x_train, y_train, x_test, y_test, subject_train and subject_test contain the data from the downloaded files.
* x_data, y_data and subject_data merge the previous datasets to further analysis.
* features contains the correct names for the x_data set, which are applied to the column names stored in mean_and_std_features.
* A same approach for activity names through the activities variable.
* all_data combines x_data, y_data and subject_data.
* tidy_data contains the relevant averages which is stored in tidy_data.txt file.  ddply() and the plyr package i use to apply colMeans(). 