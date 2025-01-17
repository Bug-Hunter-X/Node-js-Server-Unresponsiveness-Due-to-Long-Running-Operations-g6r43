# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js servers: unresponsiveness due to long-running operations within the request handler.  The `server.js` file contains a server that simulates a long-running task, causing it to hang and not respond to further requests.  The solution is provided in `serverSolution.js`.

## Problem

Node.js is single-threaded.  If a request handler performs a lengthy operation, it blocks the event loop, preventing other requests from being processed. This leads to a unresponsive server. 

## Solution

The solution involves offloading long-running tasks to worker threads or using asynchronous operations to avoid blocking the main thread. The `serverSolution.js` example showcases this using asynchronous operations.