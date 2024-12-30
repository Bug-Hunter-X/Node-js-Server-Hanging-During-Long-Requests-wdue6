# Node.js Server Hanging During Long Requests

This repository demonstrates a common issue in Node.js where a server hangs during long-running requests if asynchronous operations aren't handled correctly.  The `server.js` file shows the problematic code, while `serverSolution.js` provides a solution.

## Problem

The provided `server.js` simulates a long-running task within the request handler.  Because Node.js is single-threaded, this blocks the event loop, preventing it from processing other requests or events.  The server effectively becomes unresponsive.

## Solution

The `serverSolution.js` demonstrates how to use asynchronous operations, such as timers or worker threads, to handle long-running tasks without blocking the event loop. This ensures the server remains responsive even under heavy load.

## How to Run

1. Clone the repository.
2. Navigate to the repository's directory.
3. Run `node server.js` to experience the hanging server.
4. Run `node serverSolution.js` to see the improved, responsive server.