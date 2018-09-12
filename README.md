# Pictures-Sorting

Overview: 

mkpics - generates an html file to display a table of photos
filepics - organizes the photos into directories by the date that they were created
mkpics2 - extends mkpics to handle the directories created by filepics

Details: 

mkpics:

Writes to standard output valid html that will display a table of photos. The first command line argument to mkpics is the number of columns in the table, and the remaining arguments are the files to be displayed.

- If there are not enough pictures to fill all of the rows, then the incomplete row may be the first row or the last row.
- Include the height=100 attribute in each img tag in your table so that the page will be displayed reasonably.
- It should only include jpeg pictures in the table. It should verify that a file is a picture by checking the file type using the file program.
- It should handle 0 or more pictures.
- If mkpics is run with an argument (other than the first one) that is not a jpeg picture, it should report this to standard error with an appropriate message and continue creating the table using the valid filenames. If none of the arguments are valid filenames your program should create and write an empty table to standard output.


filepics:

- will take an existing directory as an argument. For each picture in that directory, filepics will use exiftime to get the time that the picture was generated. It will move the pictures to directories by year, and within year by month. The year directories will be subdirectories of the directory from which the script was run.
- Any non-picture files in the original directory should be ignored.
