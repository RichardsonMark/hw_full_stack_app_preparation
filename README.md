# hw_full_stack_app_preparation

Questions
1. gamesRouter
2.  server.js is responsible for connecting to the MongoDB database (games_hub). Accessing the db and passing data (games) to router(gamesRouter/createRouter). Routing data (games) to the api path (api/games). Listening to requests made on ports (5000).
3. As in Q1, games Router is responsible for defining the routes of the games resource. Also connecting/interacting with the db.
4. Sends fetch requests to the server on the routes set up in the router.
5. Get is the default type of fetch request, the optional second method is used when another type of request, such as Post or Delete are required.
6. Get Post Delete.

Extensions
1. MongoDB Driver lets us talk/connect to the DB from inside our app.
2. Each entry in MongoDB has a unique identifier (key_id) if we use this as an ObjectId then when we try to query the db for an instance, we know that it will give us a unique entry, rather than searching for a piece of data that is stored as a string, which may have a match/partial match elsewhere in the db.
