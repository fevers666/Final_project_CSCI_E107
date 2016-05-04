# Final_project_CSCI_E107
The repo contains the Rmarkdown, html and all assets required to run the program

There are 3 zip files in this repo. The zips named tests_ascii.zip and gemlich.zip contain ansi text files with the data used in the majority of the project. 
final.rmd has code on lines 53 and 54 as follows:
dataFiles <- file.path("E:","hal", "tests_ascii") ## update to reflect location..
gemlichFile <- file.path("E:","hal", "gemlich")

In order to run the program, the zip files mentioned above must be unzipped and these two lines changed to reflect the location of the files.
Note that the file.path() method in R creates a way to copy ALL files in a directory. 'test_ascii' contains several files, while 'gemlich' contains only 1. In the R application I deliberately separated these into 2 separate directories. Please do the same when you run the program.

Secondly, I have made use of teh R package 'Stylo' to run some clustering and classification methods on lines 357 ff in the Rmd. This package has particular requirements for the location of the data on which it operates. The 'stylo()' method call requires the following:
"The actual text files for your analyses must be placed in a subfolder in the working directory, named corpus (Note: all file names are case sensitive!). All functions in this tool suite expect to find at least two input texts for their analyses."
In my case, the zip named 'ml_main' contains a subdirectory and files whose names folow the conventions specified by Stylo. The 'ml_main.zip' must be extracted to your computer, and the working directory must be set to the top-level directory where 'corpus' is an immediate child. The 'classify() method in Stylo  requires another set of conventions. Both conventions will be met and data located by Stylo as long as the working directory is set to the place where you have unzipped 'ml_main'
