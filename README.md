# GettingAndCleaningDataCourseProject

## Contents
1. run_analysis.R - R script that transforms data from Samsung data to aggregated data of average for each mean() and std() for each measurement of data. Samsung data should be in subfolder "UCI HAR Dataset" in working directory.
2. Codebook.pdf - Codebook for resulting data

## Description of R script
* Read data from Samsung tables in txt format to dplyr package data frames
* Merge train and test data for variables
* Seek for variable names from features.txt containing mean() or std() and save resulting indicies
* Select only columns with indices got in previous step
* Merge IDs of subjects and activities to resulted set from previous step
* Join with table which connects activity ID with activity name
* Delete activity ID from resulting set
* Group by activity and subject and calculate mean for each other column
* Write the resulting set into result.txt file in working directory
