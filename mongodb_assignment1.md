## Task 1: Add multiple students

```js
db.students.insertMany([
    {
     "name": "dhruvesh",
     "rollNumber":12,
     "department":"MBA",
     "year": "2",
     "subjectsEnrolled":"accountancy"
    },
     {
     "name": "krish",
     "rollNumber":68,
     "department":"pharmacy",
     "year": "1",
     "subjectsEnrolled":"biology"
    },
     {
     "name": "arjun",
     "rollNumber":23,
     "department":"photography",
     "year": "1",
     "subjectsEnrolled":"camera"
    },
     {
     "name": "dhruvil",
     "rollNumber":50,
     "department":"agricultural",
     "year": "2",
     "subjectsEnrolled":"agri-cultivate"
    },
     {
     "name": "priy",
     "rollNumber":44,
     "department":"cse",
     "year": "1",
     "subjectsEnrolled":"javascript"
    }
])
```
this will add more student data with unique data.

## Task 2: Add multiple subjects

```js
db.subjects.insertMany([
    {
        subject: "physics",
        topics : ["rotational-motion","modern--physics","newtonslaw","electrodynamics","electric-current"]
    },
     {
        subject: "chemistry",
        topics : ["organic","inorganic","physical","electrocell","compound-color"]
    },
     {
        subject: "mathematics",
        topics : ["calculus","probability","matrices","vector","logarithm"]
    },
     {
        subject: "biology",
        topics : ["plant-life","animal-life","human-anatomy","cells","plasma"]
    },
 {
        subject: "physical Education",
        topics : ["hockey","cricket","football","volleyball","badminton"]
    },
    {
        subject: "IT",
        topics : ["javascript","python","c language","c++","react"]
    }
])
```
this will create subjects collection and add data init.

## Task 3: Query students based on subject enrollment
```js
db.students.find({subjectsEnrolled:"javascript"});
```
this will find all javascrript enrolled sunject students.

## Task 4: Add a new topic to a subject
```js
db.subjects.updateOne(
    {subject:"IT"},
    {$push:{topics:"node.js"}}
)
```
this will push node.js topic in the array.

## Task 5: Query subjects with multiple topics
```js
db.subjects.find({
    $expr:{
        $gte:[{$size:"$topics"},4]
    }
})
```
this will show the data if topics are more than 4 and equql to 4.

## Task 6: Update student enrollment
```js
db.students.insertOne({
    name: "Jenil",
    rollNumber: 30,
    department: "IT",
    year: "1",
    subjectsEnrolled: []
});
```
this will add jenil data in students collection.

```js
db.students.updateOne(
    {name:"Jenil"},
    {$push:{subjectsEnrolled:"react native"}}
)
```
this will add react native topic in jenil data.

## Task 7: Query all students
```js
db.students.find({},{name:1,subjectsEnrolled:1,_id:0,coursesEnrolled:1})
```
this will show only name , subjectsEnrolled and coursesEnrolled data from the studennt collection.

## Task 8: Update multiple students' year
```js
db.students.updateMany(
    {department:"cse"},
    {$set:{year:"3"}}
)
```
this will update the data of cse department.

## Task 9: Add new topics to multiple subjects
```js
db.subjects.insertMany([
    {subject:"react",
    topic:["usestate"]},

    {subject:"nodejs",
    topic:["node"]},

    {subject:"mongodb",
    topic:["indexing"]},
])
```
this will add more data in subjects.

```js
db.subjects.updateOne(
    {subject:"react"},
    {$push:{ topic: "useeffect"}}
);
db.subjects.updateOne(
    { subject: "nodejs" },
    { $push: { topic: "express" }} 
);
db.subjects.updateOne(
    {subject: "mongodb"}, 
    {$push: {topic: "sharding"}} 
);
```
this will add more topics init.

## Task 10: Remove a topic from a subject
```js
db.subjects.updateOne(
    {subject:"nodejs"},
    {$pull:{topic:"express"}}
)
```
this will remove topic from nodejs .

## Task 11: Query all students in a specific year
```js
db.students.find(
    {$or:[{year:"2"},{year:"3"}]}
)
```
this will show data of year 2 or 3.

## Task 12: Delete a student by roll number
```js
db.students.deleteOne(
    {rollNumber:50}
)
```
this will delete the data of rollnumber 50.

## Task 13: Delete all students from a department
```js
db.students.deleteMany(
    {department:"electrical engineering"}
)
```
this will delete all electrical engineering student data.

## Task 14: Retrieve all topics for a subject
```js
db.subjects.find(
    {},
    {subject:1, topics:1,_id:0}
)
```
this will show subject and topics only no id .

## Task 15: Count the number of subjects in which a student is enrolled

