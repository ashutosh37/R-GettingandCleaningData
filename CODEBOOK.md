---
title: "CODEBOOK"
output: html_document
---


## Problem

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. 

For the current problem , we need to need to merge the training and test dataset and extract out the required columns and then calculate the mean for the all the measurment types.

##Columns/Features/Measurments extraxted:
[1] "body-acceleration-mean-x-time"                  
 [2] "body-acceleration-mean-y-time"                  
 [3] "body-acceleration-mean-z-time"                  
 [4] "body-acceleration-std-x-time"                   
 [5] "body-acceleration-std-y-time"                   
 [6] "body-acceleration-std-z-time"                   
 [7] "gravity-acceleration-mean-x-time"               
 [8] "gravity-acceleration-mean-y-time"               
 [9] "gravity-acceleration-mean-z-time"               
[10] "gravity-acceleration-std-x-time"                
[11] "gravity-acceleration-std-y-time"                
[12] "gravity-acceleration-std-z-time"                
[13] "body-acceleration-jerk-mean-x-time"             
[14] "body-acceleration-jerk-mean-y-time"             
[15] "body-acceleration-jerk-mean-z-time"             
[16] "body-acceleration-jerk-std-x-time"              
[17] "body-acceleration-jerk-std-y-time"              
[18] "body-acceleration-jerk-std-z-time"              
[19] "body-gyro-mean-x-time"                          
[20] "body-gyro-mean-y-time"                          
[21] "body-gyro-mean-z-time"                          
[22] "body-gyro-std-x-time"                           
[23] "body-gyro-std-y-time"                           
[24] "body-gyro-std-z-time"                           
[25] "body-gyro-jerk-mean-x-time"                     
[26] "body-gyro-jerk-mean-y-time"                     
[27] "body-gyro-jerk-mean-z-time"                     
[28] "body-gyro-jerk-std-x-time"                      
[29] "body-gyro-jerk-std-y-time"                      
[30] "body-gyro-jerk-std-z-time"                      
[31] "body-acceleration-magnitude-mean-time"          
[32] "body-acceleration-magnitude-std-time"           
[33] "gravity-acceleration-magnitude-mean-time"       
[34] "gravity-acceleration-magnitude-std-time"        
[35] "body-acceleration-jerk-magnitude-mean-time"     
[36] "body-acceleration-jerk-magnitude-std-time"      
[37] "body-gyro-magnitude-mean-time"                  
[38] "body-gyro-magnitude-std-time"                   
[39] "body-gyro-jerk-magnitude-mean-time"             
[40] "body-gyro-jerk-magnitude-std-time"              
[41] "body-acceleration-mean-x-frequency"             
[42] "body-acceleration-mean-y-frequency"             
[43] "body-acceleration-mean-z-frequency"             
[44] "body-acceleration-std-x-frequency"              
[45] "body-acceleration-std-y-frequency"              
[46] "body-acceleration-std-z-frequency"              
[47] "body-acceleration-jerk-mean-x-frequency"        
[48] "body-acceleration-jerk-mean-y-frequency"        
[49] "body-acceleration-jerk-mean-z-frequency"        
[50] "body-acceleration-jerk-std-x-frequency"         
[51] "body-acceleration-jerk-std-y-frequency"         
[52] "body-acceleration-jerk-std-z-frequency"         
[53] "body-gyro-mean-x-frequency"                     
[54] "body-gyro-mean-y-frequency"                     
[55] "body-gyro-mean-z-frequency"                     
[56] "body-gyro-std-x-frequency"                      
[57] "body-gyro-std-y-frequency"                      
[58] "body-gyro-std-z-frequency"                      
[59] "body-acceleration-magnitude-mean-frequency"     
[60] "body-acceleration-magnitude-std-frequency"      
[61] "body-acceleration-jerk-magnitude-mean-frequency"
[62] "body-acceleration-jerk-magnitude-std-frequency" 
[63] "body-gyro-magnitude-mean-frequency"             
[64] "body-gyro-magnitude-std-frequency"              
[65] "body-gyro-jerk-magnitude-mean-frequency"        
[66] "body-gyro-jerk-magnitude-std-frequency"         
[67] "subject"                                        
[68] "activity"  


##These column names are different than the ones provided in the text files as they have been formatted using :
filtered_feature_names <- gsub("\\(\\)", "", filtered_feature_names)
filtered_feature_names <- gsub("Acc", "-acceleration", filtered_feature_names)
filtered_feature_names <- gsub("Mag", "-Magnitude", filtered_feature_names)
filtered_feature_names <- gsub("^t(.*)$", "\\1-time", filtered_feature_names)
filtered_feature_names <- gsub("^f(.*)$", "\\1-frequency", filtered_feature_names)
filtered_feature_names <- gsub("(Jerk|Gyro)", "-\\1", filtered_feature_names)
filtered_feature_names <- gsub("BodyBody", "Body", filtered_feature_names)


##Subject Columns :
Identifies a subject based on ID

##Activity Column:
  id               name
1  1            WALKING
2  2   WALKING_UPSTAIRS
3  3 WALKING_DOWNSTAIRS
4  4            SITTING
5  5           STANDING
6  6             LAYING

##Mean:

Mean of the measurement for a combination of subject and activity



