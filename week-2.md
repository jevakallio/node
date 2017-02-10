## WEEK 2 TUTORIAL WIP

Things to cover, from notes during the week:

### Repetition of the web backend use case: serving JSON and HTML
- This is important to keep in mind why we do node in the first place
- TASKS: (?)
- practical: make another app to serve JSON (and HTML)
- theoretical: stand up and explain some web backend concepts, eg
 - status codes
 - REST and routing
 - headers, query params, posting data
 - what's the difference bewteen sending JSON or HTML

- controller - some logic and some aync processes to run before sending JSON / HTML response

### Talk a bit more about the tooling use case of node (as scripts)
- There was some confusion I felt about using node/npm in tooling vs as servers

- TASK: write a little node script? how to fit this in with the rest of the session?

### Basics of Node programming
- what is sync vs async,
- what does it mean to “block” and why it is bad
- what are streams
- what is global state
- what is the request lifecycle (vs. statefulness)

- TASKS
 - practical: include async processes, blocking and non-blocking. (cf the node girls what is node)
 - practical: game!
 - theoretical: stand up and explain these fundamentals
 - practical and theoretical: the node girls what is node document

### ideas for the steps in the tutorial

#### Set up

1.
   - set up a new project and install express - or should we havr a blank project to fork?
   - remember how to do this? npm init -y; npm i -S express;

2.
   - download the provided /data directory to your root directory (have a look at them) JSON files for the resources we are going to add to our app ('/code GET', '/code POST' OR '/method GET', '/method POST')

3.
   - download postman

#### Build a json api

1.
   - write a server.js file
   - create a route to serve the / (base) JSON (read the file path and send the response as json)
   - run on port 8080
   - node server.js

2.
   - create a GET /code route to serve the /code json
   - get it in your browser (check out the json formatter)

3.
   - create a GET /code/:id route to serve an individual code
   - if there is no code, send a 404 back

4.
   - create a POST /code/:id route. this should save the post data to a file on your machine
   - using postman, post the supplied json to your localhost:8080/api/:code
   - try to get it in your browser

#### MVC (advanced / extra)

1.
   - set up a templating engine? or static files? the different use cases. add an api source and add stuff into the view.
   - store the HTML in a views directory
   - could render the JSON data into a view

### homework

- practical project
 - maybe add to the app from the session - 3, setting up views for the data?
 - add more routes for the HTTP / REST verbs / methods
- "koans"
 - supertest unit tests to isolate concepts
 - run tests in CI when PRs submitted
