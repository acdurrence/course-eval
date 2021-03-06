# Course-Eval
Our evaluation project in course CSE442 Fall semester is to create a web page in a group format.  The members of our group are Timothy J Eilinger II, Min Bang, Seti Reid, Aaron Durrence and Linn Linn Htway. We received guidance from TA Michael Wehar. The link to our web pages is as follows: 

http://hulk.cse.buffalo.edu/Course_Eval/page_search.php

# Description

Our objective for the course evaluation website is to design a website that will be beneficial to the students of University of Buffalo. The students of UB can access the website by logging in using their student id. The result page will show Aggregate data and will help students in deciding which professor will best suite them and as well as what courses specific instructors teach. We created a rating scale for the students by the students that display a level of popularity with instructors and the courses they teach as well.

# User Interface

The web application is user friendly with concise simple tabs and icons to navigate through.  Students can utilize the website by using the Faculty name or course name of choice. First in the drop down menu students can choose either instructor or course. By choosing the instructor, the department name will be available and the names of all instructors in the department will be displayed. A course list will be displayed when a student chooses the course link. 

# Development

The website UI was made with html, css, javascript, bootstrap, jquery. Backend with Ubuntu, php, mysql. Data came from Thomas Slomka who is from the program accessment and data accessment reporting department of UB in csv files. In the future we have plan to add admin tools, user authentication and tracking, and make the layout more user friendly. 

# Overview of PHP Scripts 

- Filename: **page_search.php**

```
Description: Retrieves all available subjects for dropbown and generates a webpage.

Based on the user's selection from the dropdown, the page makes an AJAX request

to ajax.search.php to get all available courses.
```

- Filename: **ajax.search.php**

```
Description: Retrieves all of the available courses for a given subject.

Parameters: action, searchType, subject
```

- Filename: **page_course.php**

```
Description: Retrieves course data and displays it in a chart.

Parameters: id
```

- Filename: **data_accessor.php**

```
Description: A collection of php functions for retreiving course data from the database.
```
Additional php functions were made for retreiving instructor data.  However, this code is currently incomplete.

...

In folder **admin_tools** (designed to be used to house administrative tools, primarily for handling data). See the readme in the folder for further details.

- Filename: **general.php**

```
Description: Provides a class to control all general functions for classes in the admin_tools folder. Currently houses a $pdo variable which creates a limited connection to the DB. All classes in this folder should extend general.
```

- Filename: **merge_script.php**

```
Description: Simple script to import locally stored csv files into the DB using the merge_data script. Use this script as a template if the mergeTools class is used as the order these functions are called in is important (assuming you are importing the same files I did).
```

- Filename: **merge_data.php**

```
Description: Provides functions to import data from csv files corresponding to the data to be entered into the DB. Notice it extends general. These functions provide the backend of any kind of interface that might be created to import data into the database automatically. They will never delete data, only add new records when a previous one does not exist. The only parameter these functions require is a file path string.
```
