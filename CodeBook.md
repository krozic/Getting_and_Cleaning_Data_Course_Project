# **Code Book**

*This document describes the files used, what they contain, and where they were sourced from. It also describes the operations that are performed to tidy and subset the data and produce the final data set of average values.*

### **Data Source**

***

[.zip](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) file was provided by "Getting and Cleaning Data" instructors through cloudfront.net.

Original [description of full data set](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) by UCI.

### **Data Description**

***

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.[^1]

### **Files**

***

- 'data/UCI_HAR.zip': Contains the files required to build the tidy data and final data set.
- 'test/X_test.txt': Table of gyroscope and observation values for test data. Each row provides sensor values corresponding to a 'subject' performing a single 'activity'.
- 'test/y_test.txt': Activity numbers to go with the 'X_test.txt' table.
- 'test/subject_test.txt': Subject number labels to go with the 'X_Test.txt' table.
- 'train/X_train.txt': Table of gyroscope and observation values for training data. Each row provides sensor values corresponding to a 'subject' performing a single 'activity'.
- 'train/y_train.txt': Activity numbers to go with the 'X_train.txt' table.
- 'train/subject_train.txt': Subject number labels to go with the 'X_train.txt' table.
- 'features.txt': A table containing the variable names for every sensor value obtained.
- 'activity_labels.txt': Descriptive titles for the activities that subjects were asked to perform.

### **Included Variables**

***

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals TimeAccelerometer-XYZ and TimeGyroscope-XYZ. 

#### **Variables beginning with "Time":**

*Time domain signals captured at a constant rate of 50 Hz. Signals were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise.*

#### "Body" and "Gravity" Signals:

*The acceleration signal was separated into body and gravity acceleration signals using another low pass Butterworth filter with a corner frequency of 0.3 Hz.*

- TimeBodyAccelerometer...-XYZ 
- TiemGravityAccelerometer...-XYZ

#### "Jerk" Signals:

*The body linear acceleration and angular velocity were derived in time to obtain Jerk signals.* 

- TimeBodyAccelerometerJerk...-XYZ 
- TimeBodyGyroscopeJerk-XYZ 

#### "Magnitude" Signals:

*The "Euclidean norm" was used to calculate the magnitude of these three-dimensional signals.*

- TimeBodyAccelerometerMagnitude
- TimeGravityAccelerometerMagnitude
- TimeBodyAccelerometerJerkMagnitude
- TimeBodyGyroscopeMagnitude
- TimeBodyGyroscopeJerkMagnitude 

#### **Variables beginning with "Frequency":**

*Indicates frequency domain signals obtained by applying a Fast Fourier Transform (FFT) to some of the signals described earlier.*

- FrequencyBodyAccelerometer-XYZ
- FrequencyBodyAccelerometerJerk-XYZ
- FrequencyBodyGyroscope-XYZ
- FrequencyBodyAccelerometerJerkMagnitude
- FrequencyBodyGyroscopeMagnitude
- FrequencyBodyGyroscopeJerkMagnitude 

#### **Variables beginning with "Angle":**

*Additional vectors obtained by averaging the signals in a signal window sample.*

- Angle(TimeBodyAccelerometerMean_Gravity)            
- Angle(TimeBodyAccelerometerJerkMean_GravityMean)    
- Angle(TimeBodyGyroscopeMean_GravityMean)            
- Angle(TimeBodyGyroscopeJerkMean_GravityMean)        
- Angle(X_GravityMean)                                
- Angle(Y_GravityMean)                                
- Angle(Z_GravityMean) 

\*\*\***'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.*****

\*\*\***Of the data described above, only the 'Mean' and "Standard Deviation" values were used.*****

#### **Full List of Variables:**

 [1] "subject"                                             
 [2] "activity"                                            
 [3] "TimeBodyAccelerometerMean-X"                         
 [4] "TimeBodyAccelerometerMean-Y"                         
 [5] "TimeBodyAccelerometerMean-Z"                         
 [6] "TimeBodyAccelerometerSTD-X"                          
 [7] "TimeBodyAccelerometerSTD-Y"                          
 [8] "TimeBodyAccelerometerSTD-Z"                          
 [9] "TimeGravityAccelerometerMean-X"                      
[10] "TimeGravityAccelerometerMean-Y"                      
[11] "TimeGravityAccelerometerMean-Z"                      
[12] "TimeGravityAccelerometerSTD-X"                       
[13] "TimeGravityAccelerometerSTD-Y"                       
[14] "TimeGravityAccelerometerSTD-Z"                       
[15] "TimeBodyAccelerometerJerkMean-X"                     
[16] "TimeBodyAccelerometerJerkMean-Y"                     
[17] "TimeBodyAccelerometerJerkMean-Z"                     
[18] "TimeBodyAccelerometerJerkSTD-X"                      
[19] "TimeBodyAccelerometerJerkSTD-Y"                      
[20] "TimeBodyAccelerometerJerkSTD-Z"                      
[21] "TimeBodyGyroscopeMean-X"                             
[22] "TimeBodyGyroscopeMean-Y"                             
[23] "TimeBodyGyroscopeMean-Z"                             
[24] "TimeBodyGyroscopeSTD-X"                              
[25] "TimeBodyGyroscopeSTD-Y"                              
[26] "TimeBodyGyroscopeSTD-Z"                              
[27] "TimeBodyGyroscopeJerkMean-X"                         
[28] "TimeBodyGyroscopeJerkMean-Y"                         
[29] "TimeBodyGyroscopeJerkMean-Z"                         
[30] "TimeBodyGyroscopeJerkSTD-X"                          
[31] "TimeBodyGyroscopeJerkSTD-Y"                          
[32] "TimeBodyGyroscopeJerkSTD-Z"                          
[33] "TimeBodyAccelerometerMagnitudeMean"                  
[34] "TimeBodyAccelerometerMagnitudeSTD"                   
[35] "TimeGravityAccelerometerMagnitudeMean"               
[36] "TimeGravityAccelerometerMagnitudeSTD"                
[37] "TimeBodyAccelerometerJerkMagnitudeMean"              
[38] "TimeBodyAccelerometerJerkMagnitudeSTD"               
[39] "TimeBodyGyroscopeMagnitudeMean"                      
[40] "TimeBodyGyroscopeMagnitudeSTD"                       
[41] "TimeBodyGyroscopeJerkMagnitudeMean"                  
[42] "TimeBodyGyroscopeJerkMagnitudeSTD"                   
[43] "FrequencyBodyAccelerometerMean-X"                    
[44] "FrequencyBodyAccelerometerMean-Y"                    
[45] "FrequencyBodyAccelerometerMean-Z"                    
[46] "FrequencyBodyAccelerometerSTD-X"                     
[47] "FrequencyBodyAccelerometerSTD-Y"                     
[48] "FrequencyBodyAccelerometerSTD-Z"                     
[49] "FrequencyBodyAccelerometerMeanFrequency-X"           
[50] "FrequencyBodyAccelerometerMeanFrequency-Y"           
[51] "FrequencyBodyAccelerometerMeanFrequency-Z"           
[52] "FrequencyBodyAccelerometerJerkMean-X"                
[53] "FrequencyBodyAccelerometerJerkMean-Y"                
[54] "FrequencyBodyAccelerometerJerkMean-Z"                
[55] "FrequencyBodyAccelerometerJerkSTD-X"                 
[56] "FrequencyBodyAccelerometerJerkSTD-Y"                 
[57] "FrequencyBodyAccelerometerJerkSTD-Z"                 
[58] "FrequencyBodyAccelerometerJerkMeanFrequency-X"       
[59] "FrequencyBodyAccelerometerJerkMeanFrequency-Y"       
[60] "FrequencyBodyAccelerometerJerkMeanFrequency-Z"       
[61] "FrequencyBodyGyroscopeMean-X"                        
[62] "FrequencyBodyGyroscopeMean-Y"                        
[63] "FrequencyBodyGyroscopeMean-Z"                        
[64] "FrequencyBodyGyroscopeSTD-X"                         
[65] "FrequencyBodyGyroscopeSTD-Y"                         
[66] "FrequencyBodyGyroscopeSTD-Z"                         
[67] "FrequencyBodyGyroscopeMeanFrequency-X"               
[68] "FrequencyBodyGyroscopeMeanFrequency-Y"               
[69] "FrequencyBodyGyroscopeMeanFrequency-Z"               
[70] "FrequencyBodyAccelerometerMagnitudeMean"             
[71] "FrequencyBodyAccelerometerMagnitudeSTD"              
[72] "FrequencyBodyAccelerometerMagnitudeMeanFrequency"    
[73] "FrequencyBodyAccelerometerJerkMagnitudeMean"         
[74] "FrequencyBodyAccelerometerJerkMagnitudeSTD"          
[75] "FrequencyBodyAccelerometerJerkMagnitudeMeanFrequency"  
[76] "FrequencyBodyGyroscopeMagnitudeMean"                 
[77] "FrequencyBodyGyroscopeMagnitudeSTD"                  
[78] "FrequencyBodyGyroscopeMagnitudeMeanFrequency"        
[79] "FrequencyBodyGyroscopeJerkMagnitudeMean"             
[80] "FrequencyBodyGyroscopeJerkMagnitudeSTD"              
[81] "FrequencyBodyGyroscopeJerkMagnitudeMeanFrequency"    
[82] "Angle(TimeBodyAccelerometerMean_Gravity)"            
[83] "Angle(TimeBodyAccelerometerJerkMean_GravityMean)"    
[84] "Angle(TimeBodyGyroscopeMean_GravityMean)"            
[85] "Angle(TimeBodyGyroscopeJerkMean_GravityMean)"        
[86] "Angle(X_GravityMean)"                                
[87] "Angle(Y_GravityMean)"                                
[88] "Angle(Z_GravityMean)" 

### **Operations**

***

1. Check if directory/file exists then create the required directories and download the files with `if(!file.exists()){}`:

```{r}
if(!file.exists("./data")){dir.create("./data")}
fileUrl <- "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"
if(!file.exists("./data/UCI_HAR.zip")){download.file(fileUrl, "./data/UCI_HAR.zip", method = "curl")}
if(!file.exists("./UCI HAR Dataset/")){unzip("./data/UCI_HAR.zip", exdir = ".")}
```
2. Read the files described above into R with `read.table()`:

```{r}
testX <- read.table("./UCI HAR Dataset/test/X_test.txt")
testy <- read.table("./UCI HAR Dataset/test/y_test.txt")
subjectTest <- read.table("./UCI HAR Dataset/test/subject_test.txt")
trainX <- read.table("./UCI HAR Dataset/train/X_train.txt")
trainy <- read.table("./UCI HAR Dataset/train/y_train.txt")
subjectTrain <- read.table("./UCI HAR Dataset/train/subject_train.txt")
features <- read.table("./UCI HAR Dataset/features.txt")
activityLabels <- read.table("./UCI HAR Dataset/activity_labels.txt")
```

3. Label the columns of '...X' with 'features' data and the columns of '...y' and 'subject...' with 'activity' and 'subject' respectively:

```{r}
names(testX) <- features$V2
names(trainX) <- features$V2
names(testy) <- "activity"
names(trainy) <- "activity"
names(subjectTest) <- "subject"
names(subjectTrain) <- "subject"
```

4. Merge the 'subject...', '...y', and '...X' data with `cbind()` and the 'testset' to the 'trainset' with `rbind()` (This accomplishes request:

```{r}
testset <- cbind(subjectTest, testy, testX)
trainset <- cbind(subjectTrain, trainy, trainX)
fullset <- rbind(testset, trainset)
```

5. Use a 'for loop' to substitute numeric references to activity types with descriptive labels:

```{r}
for (i in 1:6) {
        fullset$activity <- gsub(i, activityLabels$V2[i], fullset$activity)
}
```
6. Using regex and `grep()`, find and subset all variables describing a 'Mean' or 'Standard Deviation':

```{r}
meanindeces <- grep("[Mm][Ee][Aa][Nn]", names(fullset))
stdindeces <- grep("[Ss][Tt][Dd]", names(fullset))
indeces <- sort(c(1:2, meanindeces, stdindeces))
tidyset <- fullset[, indeces]
```
7. Using regex and `gsub()`, rephrase variable titles to be intuitive and informative at a glance:

```{r}
names(tidyset) <- gsub("^t", "Time", names(tidyset))
names(tidyset) <- gsub("^f", "Frequency", names(tidyset))
names(tidyset) <- gsub("Acc", "Accelerometer", names(tidyset))
names(tidyset) <- gsub("Gyro", "Gyroscope", names(tidyset))
names(tidyset) <- gsub("Mag", "Magnitude", names(tidyset))
names(tidyset) <- gsub("BodyBody", "Body", names(tidyset))
names(tidyset) <- gsub("-mean", "Mean", names(tidyset))
names(tidyset) <- gsub("-std", "STD", names(tidyset))
names(tidyset) <- gsub("Freq\\(\\)", "Frequency", names(tidyset))
names(tidyset) <- gsub("\\(\\)", "", names(tidyset))
names(tidyset) <- gsub("gravity", "Gravity", names(tidyset))
names(tidyset) <- gsub("angle", "Angle", names(tidyset))
names(tidyset) <- gsub("\\(t", "(Time", names(tidyset))
names(tidyset) <- gsub("\\),|,", "_", names(tidyset))
```
8. Group the table 'tidyset' by 'subject' then by 'activity' with `group_by()` and calculate the mean for each 'activity' for each 'subject' using `summarise_all()`: 

```{r}
tidysetMeans <- tidyset %>% group_by(subject, activity) %>% summarise_all(list(mean))
```
9. Finally, write this final 'tidysetMeans' table to the file 'FinalDataset.txt' with `write.table()`:

```{r}
write.table(tidysetMeans, "FinalDataset.txt", row.name = FALSE)
```

References:

[^1]: [UCI Description](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones).