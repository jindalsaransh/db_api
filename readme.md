### API
The API has been built using node.js and express.js and functions by fetching data from a mongo.db database.

Ensure that you have a functioning mongo.db database setup before running the API on postman.

Navigate to the `db_api` directory and install the required modules using npm:

`npm install express node body-parser mongoose nodemon`

First start the database server using - 

`mongod`

To import the csv database into mongo.db, run the following command -

`mongoimport --type csv-d record_db -c records --headerline --drop final_db.csv`

Then make sure you are in `db_api/` and run the command - 

`npm run start`

Now the setup is running and you can use `postman` to test your API. The parameters need to be passed using `x-www-form-urlencode` to the `Body`.

The API will be hosted on `http://localhost:3000/`

To get all records, use -  `http://localhost:3000/records`

To get details of a single person, use - 

`http://localhost:3000/findrecord`  and pass parameter `name` as explained above and in the accompanying video.
