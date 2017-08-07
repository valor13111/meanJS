#meanJS

Understanding MEAN Stack.

Taking M101x, which goes through MongoDB using MEAN Stack.<br>
Will add more info as I am going through the course.

Mongo   - NoSQL DB, will store data with collections and documents, using JSON for example.<br>
Angular - extends HTML for application.<br>
Express - flexible web app framework, for building single and multi-page web apps.<br>
NodeJS  - server built with JS runtime for scalable apps.<br>

### Mongo

- need a path called '/data/db' needs to exist before starting mongo.<br>
- 'mongo --dbpath ~/data/db' will set where data path is<br>
- uses collections<br>
- ex. <i>db.movies.find({ leadActor: 'Arnold Schwarzenegger' })</i> will find all documents in movie collection where leadActor key equals 'Arnold Schwarzenegger'

### NodeJS

- need a package.JSON file for npm<br>
- <i>npm install</i> command downloads npm modules in './node_modules'
- I created a file caalled 'mongo_samples.js' in main directory, and in order to run mongo through node,
you use command <i>'node mongo_sample.js'</i><br>

### Callback Function
- a callback function tells nodeJS what to do once operation is complete, 
if it is successful, callback gets null as first argument, and result of operation as second.<br>
- ex. <i>'mongodb.MongoClient.connect(uri, function(error, db))'</i><br>
- error is first argument, which is returned if connection is unsuccessful, but you can use <i>db</i> handle
if it is successful to do things like inserting or querying the database.<br>

### Concurrency
- uses event loop<br>
- single-threaded<br>
- nodeJS uses callbacks, which is asynchronous, making it highly concurrent<br>

### Require Function
- in nodeJS this mechanism is for breaking up large projects into smaller files<br>
- when somebody uses <i>module.exports = function()...</i> this is return value they get when calling 
require on this file

### Mocha Testing
- most popular testing framework for nodeJS
- <i>npm install mocha -g</i> globally installs mocha, but is better to do locally in case other projects can't
use updated version of Mocha.<br>
- in package.json, can add a script to test files<br>
- ex. under scripts, use <i>"test": "mocha -R nyan test.js"</i>, which you can now run <i>npm test</i>
which runs the script from node package manager.

### Example codes and What they do
- <i>db.collection('test').find().toArray(console.log);</i>  Prints out all documents in the 'test' collection

