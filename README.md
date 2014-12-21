#### Description

This document describes the steps to take to produce a tidy set based on the "Human Activity Recognition Using Smartphones Data Set".  See the `CodeBook.md` file for detailed information on the tidy data set and the raw source data.

#### Assumptions & Prerequisites

Please note these assumptions when inspecting the tidy dataset and executing the R programming language script that generates the tidy dataset.

* The R tidying script (`run_analysis.R`) was developed and tested in this technical environment:
* R version 3.1.1 (2014-07-10)
* Mac OS X version 10.9.5
* The script loads and uses the **plyr** package.  If the **plyr** package is not installed, the script will generate an error message and stop processing
* The script creates two directories to store interim working files (`tidy_work/...`) and final tidy datasets (`tidy_output/...`)
* To minimize memory usage, the script executes in steps and writes and reads interim data files.  These data files are saved to the working folder (`tidy_work/...`)
* NOTE: The script can be run repeatedly.  Interim data files will be created if they don't exist and overwritten if they are present.  These files can be deleted after the process is complete.
* Two tidy data sets are produced and saved to the output directory (`tidy_output/...`)
* The output datasets are:
* `HumanActivitySmartphonesDataSet_Average_TidyData.txt`
* `HumanActivitySmartphonesDataSet_TidyData.txt`

#### Executing the Tidying Script

Use these steps to execute the R script to generate the tidy data set

1. From this Github repository download the raw data housed in the compressed file: `getdata-projectfiles-UCI HAR Dataset.zip`, download directly from the UCI Machine Learning Repository website, or clone this repo in it's entirety.  See the **CodeBood.md** file for more information
1. If not already installed, install the `plyr` R package into your local R implementation.  The `plyr` package is a prerequisite to execute tidying script
1. Extract the compressed files into a directory of your choice
1. Download the tidying script (`run_analysis.R`) to the folder containing the uncompressed data files (e.g. `...\UCI HAR Dataset`)
1. Open the data folder in a terminal emulator (e.g. Terminal on Mac OS, command prompt on Windows)
1. With the R script (`run_analysis.R`) in the folder containing the uncompressed data files (`...\UCI HAR Dataset`), run the R script using the command (`Rscript run_analysis.R`)
1. Inspect the script output
1. Inspect the output files located in: `...\UCI HAR Dataset\tidy_output`
1. View the tidy dataset:
* `...\UCI HAR Dataset\tidy_output\HumanActivitySmartphonesDataSet_Average_TidyData.txt`
