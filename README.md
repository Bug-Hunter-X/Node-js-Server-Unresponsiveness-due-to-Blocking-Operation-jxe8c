# Node.js Server Unresponsiveness

This repository demonstrates a common Node.js issue: server unresponsiveness caused by a long-running synchronous operation blocking the event loop.

The `server.js` file contains a simple HTTP server with a request handler that performs a time-consuming operation. This operation prevents the server from responding to subsequent requests.

The `serverSolution.js` file demonstrates a solution using asynchronous operations to avoid blocking the event loop.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `node server.js`.
4. Open multiple browser tabs and try to access `http://localhost:3000`. You'll see that only the first request will be handled, and subsequent requests will hang.

## Solution

The solution involves using asynchronous operations to avoid blocking the event loop. This allows Node.js to efficiently handle concurrent requests.