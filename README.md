# Devops-Day2
follow Uli Exercise
<h1>MongoDB – Getting Started </h1>
You Need:
Linux or Mac machine
Docker installed & running
Terminal Application
Or simply use the Google Cloud Shell (free!)
<br>
1 – Run MongoDB with Interactive Shell

git clone https://github.com/u1i/mongodb-getting-started

cd mongodb-getting-started

./run-mongo.sh
<br>
2 – Databases
Which DB am I using? <br>
db

test

Which databases exist?
show databases

admin 0.000GB
config 0.000GB
local 0.000GB

Switch to (or create) DB
use class01

switched to db class01

<br>
3 – Create a Collection & Add Data <br>
db.students.insert({"name": "Sally", "email": "sallyml91@yahoo.com"})

db.students.insert({"name": "Jack", "email": "jack@gmail.com"})
<br>
4 – Query Data
Get All Data in a Collection
db.students.find()

{ "_id" : ObjectId("5f5c85f67eaad73223e85fc3"), "name" : "Sally", "email" : "sallyml91@yahoo.com" }
{ "_id" : ObjectId("5f5c85f87eaad73223e85fc4"), "name" : "Jack", "email" : "jack@gmail.com" }

<br>
db.students.find().pretty()



Find All Students with the name 'Jack'
db.students.find({"name": "Jack"})

{ "_id" : ObjectId("5f5c85f87eaad73223e85fc4"), "name" : "Jack", "email" : "jack@gmail.com" }

<br>
5 – Deleting Stuff
Delete a Document
db.students.remove({"name": "Jack"})

Delete a Collection
db.students.remove({})
