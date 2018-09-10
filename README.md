# Pictures-Sorting

In short: 

mkpics - generates an html file to display a table of photos
filepics - organizes the photos into directories by the date that they were created
mkpics2 - extends mkpics to handle the directories created by filepics

More details: 

mkpics:

Writes to standard output valid html that will display a table of photos. The first command line argument to mkpics is the number of columns in the table, and the remaining arguments are the files to be displayed.

- If there are not enough pictures to fill all of the rows, then the incomplete row may be the first row or the last row.
- Include the height=100 attribute in each img tag in your table so that the page will be displayed reasonably.
- It should only include jpeg pictures in the table. It should verify that a file is a picture by checking the file type using the file program.
- It should handle 0 or more pictures.
- If mkpics is run with an argument (other than the first one) that is not a jpeg picture, it should report this to standard error with an appropriate message and continue creating the table using the valid filenames. If none of the arguments are valid filenames your program should create and write an empty table to standard output.

An example HTML file:

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">
<html>
  <head>
    <title>Pictures</title>
  </head>

  <body>
    <h1>Pictures</h1>

    <table>
      <tr> 
        <td><img src="pictures/IMG1.jpg" height=100></td> 
        <td><img src="pictures/IMG2.jpg" height=100></td> 
        <td><img src="pictures/IMG3.jpg" height=100></td> 
      </tr> 
      <tr> 
        <td><img src="pictures/IMG4.jpg" height=100></td> 
        <td><img src="pictures/IMG5.jpg" height=100></td> 
        <td><img src="pictures/IMG6.jpg" height=100></td> 
      </tr> 
    </table>
  </body> 
</html> 
