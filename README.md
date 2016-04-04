Getting and Cleaning Data Project
====================================
Author: Hilary Condon  (https://github.com/hilarycondon/Getting-and-Cleaning-Data.git)
***
Date: 2016-04-03
***

##Contents
* Introduction
* Instructions to Reproduce This Project
* run_analysis.R Script Overview
* Output Overview
* Acknowledgements

### Introduction

As stated in the course project description, "one of the most exciting areas in all of data science right now is wearable computing - see for example [this article."](http://www.insideactivitytracking.com/data-science-activity-tracking-and-the-battle-for-the-worlds-top-sports-brand/)<sup>1</sup> This project analyzes data collected from the accelerometers of Samsung Galaxy S smartphones and demonstrates the ability to collect, work with, and clean a data set. The resulting output is a tidy data set that can be used in subsequent analysis.

A full description of the original data set, as well as the data itself, are available at the [UCI Machine Learning Repository Center for Machine Learning and Intelligent Systems.](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)<sup>2</sup>

The initial Dataset, [UCI HAR Data](http://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip), is provided as zipped file.<sup>1</sup>



### Intstructions to Reproduce This Project

To reproduce this project, run the R script run_analysis.R that is saved in this directory. 
You will also need to store the makeCodebook.Rmd file stored in this directory, as it is called in the run_analysis.R file.

Note: This will create a data directory, or add data to a pre-existing data directory, and output files in your
current working directory. Save and run the script in a working directory where you are comfortable with activity.

To read the output text file into R and View it, Open RStudio and: 
> SET CURRENT WORKING DIRECTORY TO DIRECTORY WHERE R SCRIPT RAN AND TIDY.TXT FILE OUTPUT
> data <- read.table("tidy.txt", header = TRUE) 
> View(data) # This will not work in console, but only in RStudio

### run_analysis.R Script Overview

This script does the following, each of which is blocked out in the code of the run_analysis.R file. 
***
**1. Merges the training and the test sets to create one data set.**
  
**2. Extracts only the measurements on the mean and standard deviation for each measurement.**
  
**3. Uses descriptive activity names to name the activities in the data set.**
  
**4. Appropriately labels the data set with descriptive activity names.**
  
**5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.**
  + Per Wickham <sup>3<sup> this data set is tidy because:
    * Each variable forms a column - Subject, Activity, Variables Being Measured
    * Each observation forms a row - Average Measurement for each Variable Being Measured by Subject + Activity.
    * Each type of observational unit forms a table - One table of Average Measurements for each variable by Subjects + Activity

### Output Overview
  * This script will output a tidy dataset file as described in step 5 (Tab-deliminated text)
  * In addition, this script will create or modify the codebook.md file (Markdown) 
    + a HTML version is also created by the current script.  
    + Variable Lists, Data Structures, and Information on the Output Data is Stored in the Codebook.
    + As noted in the Codebook, ore explicit documentation of transformations to the data to arrive at the dataset are noted in the comments of the run_analysis.R file. 

### Acknowledgements
1. This project is a part as of the [Getting and Cleaning Data Course,](https://www.coursera.org/learn/data-cleaning/) which is offered by Johns Hopkins University on Coursera, with Jeff Leek, PhD, Roger Peng, PhD, and Brian Caffo, PhD instructing.
  + This course is a part of the [Data Science Specialization.](http://www.coursera.org/specializations/jhu-data-science)
2. Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. A Public Domain Dataset for Human Activity Recognition Using Smartphones. 21th European Symposium on Artificial Neural Networks, Computational Intelligence and Machine Learning, ESANN 2013. Bruges, Belgium 24-26 April 2013. 
  + Reference for Study and Original Data: [UCI Machine Learning Repository Center for Machine Learning and Intelligent Systems.](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)
3. Wickham, H. (2014). Tidy Data. *Journal of Statistical Software*, 59(10), 1 - 23. doi:http://dx.doi.org/10.18637/jss.v059.i10

  
