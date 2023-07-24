1. What is responsible for defining the routes of the games resource?

The createRouter function defines the generic routes, and server.js uses this template
to define specific routes for the games resource

2. What do you notice about the folder structure? Whats the client responsible for? Whats the server responsible for?

The server is responsible for back end operations, such as connecting to the database, routing,
responding to client requests.
The client is responsible for the front end, such as making fetch requests and rendering responses.
The app is split into these two folders as they are effectively two apps which are run separately.

3. What are the the responsibilities of server.js?

Connecting to the games database, creating games routes, and utilising express to listen for changes on the
port (and restarting when necessary).

4. What are the responsibilities of the gamesRouter?

It calls the createRouter function defined in helpers/create_router.js to create a copy of a router which
can then be used by express.

5. What process does the the client (front-end) use to communicate with the server?

It uses HTTP in the form of fetch requests.

6. What optional second argument does the fetch method take? And what is it used for in this application? Hint: See Using Fetch on the MDN docs

It is used to send requests to the server. By default these are GET requests, but the method can be changed
using the optional second argument. In this app it can request to view, post, or delete games data.

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?

GET, POST, and DELETE.

8. What are we using the MongoDB Driver for?

To connect to and interact with the MongoDB database.

EXTENSION

Why do we need to use ObjectId from the MongoDB driver?

It generates MongoDB document IDs in a default format.