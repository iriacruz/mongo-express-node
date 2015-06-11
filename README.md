# mongo-express-node

## Dependencies
npm install/n

npm install --save package

##Running 
node app.js

###Mongo commands
mongoimport --db databaseName --collection collectionName --file documentName.json

mongo

show dbs

use databaseName

db.collectionName.find().pretty()

###Mongo tricks
####Use variable as a field
var query = {_id: doc._id};
var scoreString = {};
scoreString['scores.' + lowestIndex] = 1
var operator = { '$unset' : scoreString };

students.update(query, operator, callback);

####Delete element from an array
var query = {_id: doc._id};
var operator = { '$unset' : {score.index :1};

students.update(query, operator, callback);

var query = {_id: doc._id};
var operator = { '$pull' : { scores : null } };

students.update(query, operator, callback);

