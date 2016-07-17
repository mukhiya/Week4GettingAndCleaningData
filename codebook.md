Code Book
This document describes the code run_analysis.R.
The code is segmented by comment lines (Stages) that explain at a broad level what is the objective. Each stage is broken into logical steps indicating the data transformation steps.

Downloading and loading data
1.	train.x <- read.table("./data/UCI HAR Dataset/train/X_train.txt")
2.	train.y <- read.table("./data/UCI HAR Dataset/train/y_train.txt")
3.	train.subject <- read.table("./data/UCI HAR Dataset/train/subject_train.txt")
4.	test.x <- read.table("./data/UCI HAR Dataset/test/X_test.txt")
5.	test.y <- read.table("./data/UCI HAR Dataset/test/y_test.txt")
6.	test.subject <- read.table("./data/UCI HAR Dataset/test/subject_test.txt")
7.	features <- read.table("./data/UCI HAR Dataset/features.txt", stringsAsFactors = FALSE)[,2]

Manipulating data
•	Merges test data and training data to allData
•	Extract mean and standard deviation of each measurements,  Subject, Activity and Features to finalData
•	Replace cryptic column names with more descriptive labels such as Mean,Freq, Time and Std etc
•	Group finaldata on subject and activity column to groupData
•	Create a new tidy data file from groupData

Variables used
Index	Variable Name	Contains
1	fileUrl	URL of the raw zip file to download
2	train.x	Training set  in raw form
3	Train.y	Lables for raw training data 
4	test.x	Test set in raw form
5	test.y	Lables for test set
6. 	Training data	Combination of raw training data and the labels
7	Test data	Combination of raw test data and lables
8	Alldata	Combination of training and test data
9	Features	List of features (attributes) in the file
10	FeatureIndex	Contains the index of feature with mean or standard deviation in the name
11	FinalData	Contains subject, activity, features 
12	Groupdata	Final data grouped on subject, activity with mean of each feature

Writing final data to CSV
Creates the output file "tidyaverageData.txt" in the current working directory

