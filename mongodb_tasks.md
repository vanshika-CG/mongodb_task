## Task 1: Add more students to the students collection
```js
db.students.insertMany([
    {
     "name": "samiksha",
     "rollNumber":1,
     "department":"MBA",
     "year": "2",
     "subjectsEnrolled":"accountancy"
    },
     {
     "name": "rahul",
     "rollNumber":2,
     "department":"pharmacy",
     "year": "1",
     "subjectsEnrolled":"biology"
    },
     {
     "name": "heena",
     "rollNumber":3,
     "department":"photography",
     "year": "1",
     "subjectsEnrolled":"camera"
    },
     {
     "name": "pavan",
     "rollNumber":4,
     "department":"agricultural",
     "year": "2",
     "subjectsEnrolled":"agri-cultivate"
    },
     {
     "name": "priya",
     "rollNumber":5,
     "department":"cse",
     "year": "1",
     "subjectsEnrolled":"javascript"
    }
])
```
this will add more student data with unique data.

## Task 2: Insert a new course into the courses collection
```js
db.courses.insertMany([
    {
 "Course Code": "CS202",
"Name": "Data Structures",
"Credits": "3",
"Instructor": "Prof. Krishna"
    }
])
```
this will add new course to courses collection.

## Task 3: Fetch a specific student's record by roll number
```js
db.students.find({"rollNumber":12})
```
this will show the data of rollnuber 12.

## Task 4: Query all students who are enrolled in a particular course
```js
db.courses.find({"courseCode":"211"})
```
this will find data with 211 coursecode.

## Task 5: Update a student's courses

