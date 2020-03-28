Cook Book
---------

### 1) Download the given [dataset](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip), extract it and place it in the directory of your project.

### 2) Create variables to read in the following data items.

-   subject\_test &lt;- subject\_test.txt (testing data for subjects)
-   subject\_train &lt;- subject\_train.txt (training data for subjects)
-   X\_test &lt;- X\_test.txt (x testing data)
-   y\_test &lt;- y\_test.txt (y testing data)
-   y\_train &lt;- y\_train.txt (y training data)
-   X\_train &lt;- X\_train.txt (x training data)
-   features &lt;- features.txt (feature extration or the selected
    features from the data)
-   activity\_labels &lt;- activity\_labels.txt (activities performed)

### 3) Bind the training and testing data.

The rbind function binds or merges the following dataset together. -
X\_train and X\_test dataset. - y\_train and y\_test dataset. -
subject\_train and subject\_test dataset. The cbind() function merges
the subject, X and y dataset into binded\_data variable.

### 4) Extract only the measurements on the mean and standard deviation for each measurement.

the binded\_data is subsetted by selecting only columns: subject, code
and mean(mean) and standard deviation(std) measurements and stored in
tidy\_data.

### 5) Use discriptive activity names to name the activities in the dataset.

The activity names are taken from the activity\_labels dataset and
substituted into the code column of the tidy\_data.

### 6) Appropriately label the data set with descriptive variable names.

-   acc renamed to -&gt; Accelerometer
-   gyro renamed to -&gt; Gyroscope
-   mag renamed to -&gt; Magnitude
-   BodyBody renamed to -&gt; Body
-   Anything that starts T replaced by -&gt; Time
-   Anything that starts F replaced by -&gt; Frequency
-   gravity renamed to -&gt; Gravity
-   angle renamed to -&gt; Angle.

**7) From the dataset, create second, independent tidy dataset with
average of each variable for each activity and each subject.** - Take
the mean value of each variable for each activity and subject from
tidy\_data and store it in dataset. - Finally export the dataset into
tidy-data-final.txt file.
