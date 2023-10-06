# cleaningdata_final_assessment
Getting and Cleaning Data Final Assessment

=================================================================
Human Activity Recognition Using Smartphones Dataset
==================================================================
Coursera Week 4 Assessment. 

The data is provided as separate datasets of the human activity accelerometry measurements, there is a training and a test dataset, these have to be joined to form the
complete dataset. Furthere, identification of respective activity of the studied particants also is contained in
a separate file called "activity" as well as subject identifiers, they are located in the file "subject". All these
files have to be joined to build the tidy dataset needed for later calculations. 

The following files are needed:

- 'features.txt': List of all features.

- 'activity_labels.txt': Links the class labels with their activity name.

- 'train/X_train.txt': Training set.

- 'train/y_train.txt': Training labels.

- 'test/X_test.txt': Test set.

- 'test/y_test.txt': Test labels.

- 'train/subject_train.txt': subject identifiers.

- 'test/test/subject_test.txt': subject identifiers.

First, all the data of both test and training set are read into R (X_test, X_train, y_test, y_train). Then they are joined together 
with their respective variable names taken from features.txt and build the "data" dataset. Subject is used to identify the participants and is changed to 
build the column "ID" containing subject numbers from 1 to 30. 
Next, the activity labels are taken from "activity_labels.txt" and saved as "labels". These are then used to created a factor variable for the variable
"activity" in the dataset und to convert the numbers contained in this column to the right labels and correct names. 
This yields a correctly named dataset.

Next, columns that contain mean or sd are identified and the respective columns are saved in "columns_mean_sd", then
the data is subsetted so it contains only these columns. The columns "ID" and "activity" are added to the dataset. 

Finally, the tidy_data is created by grouping the subsetted dataset by ID and activity and calculating the mean for each of the before selected variables. 

