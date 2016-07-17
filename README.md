# Week4GettingAndCleaningData
Project to demonstrate collect and clean data sets using R
The project starts with the download of a zip file available at ""https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip". This is raw data sets collected in two folders, one called "Training" and the other "Test" available in "UCI HAR Datasets" folder
The training dataset "trainingData" is creatd by binding the subject, lables and the raw data for train (Train.X, Train.Y and train.subject)
Similarly, the "testData" is created by binding the subject, lables and raw data for test (Test.X, Test.Y and test.subject)
The test data and training data are combined (row bind) to create all data that contains all the rows of test and training data
Finaldata is created by combining only the "mean" and "standard deviations" features with all the rows of "allData" 
