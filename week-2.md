# Node II

### It's our second week of Node.js! The plan is as follows:

## 10:30 AM - Homework review

## 11:00 AM - Scrum session with Kram

## 1:00 PM - Node session

This is going to be a mixture of instructor-led parts to recap the fundamentals of Node.js, and practical pair-programming parts to get more experience with building Node.js apps.

### Node.js Fundamentals Recap

[Link](/node-recap.md)

### Practical exercises: The Status Code API and The Status Code Website.

First up, we are going to build a Node.js API to provide JSON data containing information about all the different [HTTP Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status).

The API is an Express app, just like the one you built last week. It has a server.js file but no routes... yet. You need to add them.

To guide you, the app has a test suite which you can run with `npm test`. There should be a single failing test. The failing test should say something like `Error: expected 200 "OK", got 404 "Not Found"`. 

You need to identify what request the test is expecting your app to handle, and then you must add the correct route to your server.js file. Once you've done that, the test will pass!

If you look at the test itself, you will see that it is doing the equivalent of running your app and then calling 'http://localhost:8080/code/200'. Then it is expecting to receive a HTTP response containing JSON data about the status code `200 "OK"`.

This should give you an idea of the work you and your pair now need to do. Why would your app respond with a `404 "Not Found"` when it gets a request for `/code/200`? 

Hint: you want to allow someone to make a GET request to `/code/200` or `/code/301` or `/code/503`. The number after the `/code/` part should not be hardcoded in the route - it should be what's called a Route Parameter or URL Parameter. You need to use this parameter to get the right data out of the statusCode object in your server.js, and then return it as a JSON response.

