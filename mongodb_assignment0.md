## Task 1: Create a "CodingGita Students" database

```
use CodingGita
```
this command is used to create database

``` 
db.students.insertMany([
    {
        name :"vanshika",
        rollNumber: "51",
        department: "cse",
        year: "1",
        coursesEnrolled: "datascience"
    },
      {
        name :"yashvi",
        rollNumber: "60",
        department: "IT",
        year: "1",
        coursesEnrolled: "AI/ML"
    },
      {
        name :"priyasha",
        rollNumber: "56",
        department: "cse",
        year: "1",
        coursesEnrolled: "software"
    }
]);
```
create students collection and add data.

```
db.courses.insertMany([
    {
        courseCode: "108",
        name: "introduction to javascript",
        credits: "5",
        instructor: "Mr. Neel Patel"
    },
     {
        courseCode: "106",
        name: "introduction to C++",
        credits: "4",
        instructor: "Ms. Akruti Patel"
    },
 {
        courseCode: "111",
        name: "introduction to python",
        credits: "4",
        instructor: "Mr. Neel Patel"
    }
])
```
this will create a courses collection and add data into it.


## Task 2: Perform CRUD operations

```
db.students.insertMany([
    {
        name: "kanishka",
        rollNumber: "30",
        department: "cse",
        year: "2",
    corsesEnrolled: "datastructure"
    },
     {
        name: "khushi",
        rollNumber: "400",
        department: "cse",
        year: "3",
    corsesEnrolled: "machine learning"
    }
])
```
this will add more data in students collection.
```
db.courses.insertMany([
     {
        courseCode: "222",
        name: "introduction to C language",
        credits: "3",
        instructor: "Mr. Neel Patel"
    },
     {
        courseCode: "211",
        name: "Figma",
        credits: "5",
        instructor: "Mr. Rushil patel"
    }
])
```
this will more data in courses collection.

```
db.students.find({"department":"cse"});
```
this will find all the student with cse department.

```
db.students.find({"year":"1"});
```
this will find all the student with 1st year student.
```
db.students.find({"coursesEnrollred": "software"});
```
this will find all software course enrolled.

```
db.students.updateOne(
    {"name":"kanishka"},
    
)
