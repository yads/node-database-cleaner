Node.js Database Cleaner
========================
The simplest way to clean your database. Removes all data. Starting only with mongodb, but will support mainstream databases.

Say you're doing test cases. How can you clean up your data after each
test run? With Database Cleaner you can simply do it with one line of code.

Supported Databases
-------------------
* MongoDB
* Redis
* CouchDB
* MySQL

Dependencies
------------

### Runtime
* Node 0.4.x+
* node-mongodb-native (a.k.a mongodb)
* redis
* cradle for couchdb (<http://cloudhead.io/cradle>)
* mysql server

### Development/Tests
* nodeunit
* hredis
* redis
* cradle
* mysql

Instalation
-----------
> npm install database-cleaner 

Usuage
------
> var DatabaseCleaner = require('database-cleaner');
> var databaseCleaner = new DatabaseCleaner(type); //type = 'mongodb|redis|couchdb'
>
> databaseCleaner.clean(database, callback);

### Examples
Take look at test folder to see how it works

A full example can be found at (<https://github.com/emerleite/node-rating/blob/master/test/hit.test.js>)

Running tests
-------------
There is some ways to run tests:

$ nodeunit test (you need nodeunit globaly installed. *npm install -g nodeunit*)
$ npm test
$ ./run-tests.js

> For tests you need each database running (mongodb, redis, couchdb, mysql)
> Or run once. Ex: nodeunit test/redis.test.js

To-Do
-----
* see (<https://github.com/emerleite/node-database-cleaner/issues>)

Author
------

* Emerson Macedo (<http://codificando.com/> and <http://nodecasts.org>)

License:
--------

(The MIT License)

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
