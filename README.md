# hw_full_stack_app_preparation

# Questions

1. What is responsible for defining the routes of the `games` resource?
2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?
3. What are the the responsibilities of server.js?
4. What are the responsibilities of the `gamesRouter`?
5. What process does the the client (front-end) use to communicate with the server?
6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs
7. Which of the games API routes does the front-end application consume (i.e. make requests to)?
8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?

# Answers

1. gamesRouter
2. client - front end / UI. server - back end / API / DB stuff
3. server.js is responsible for connecting to the MongoDB database (games_hub). Accessing the db and passing data (games) to router(gamesRouter/createRouter). Routing data (games) to the api path (api/games). Listening to requests made on ports (5000). -- also uses bodyParser to access data from requests + allows CORS requests.
4. As in Q1, games Router is responsible for defining the routes of the games resource. Also connecting/interacting with the db.  -- CRUD functionality from the DB games_hub
5. Sends fetch requests to the server on the routes set up in the router.  -- this is defined in a 'helper'/'services' file called GamesService.js
6. Get is the default type of fetch request, the optional second method is used when another type of request, such as Post or Delete are required.  -- a config object the things we will need: a method - (GET/PUT/POST), body - the payload, headers- an onject. we will need to specify the Content-Type as application/json
7. Get Post Delete. -- index create delete
8. MongoDB Driver lets us talk/connect to the DB (games_hub) from inside our app. -- to get collecion of games, all of this in server.js

# Extensions

1. Why do we need to use ObjectId from the MongoDB driver?

 Each entry in MongoDB has a unique identifier (key_id) if we use this as an ObjectId then when we try to query the db for an instance, we know that it will give us a unique entry, rather than searching for a piece of data that is stored as a string, which may have a match/partial match elsewhere in the db.


Diagram the dataflow for removing a game is available at - Homework-FullStackGamesHubApp_Answers.png
