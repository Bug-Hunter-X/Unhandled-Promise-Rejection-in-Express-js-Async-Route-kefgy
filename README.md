# Unhandled Promise Rejection in Express.js Async Route

This repository demonstrates a common error in Express.js applications: improper error handling within asynchronous route handlers.  Failure to properly catch and handle promise rejections can lead to unexpected crashes and prevent graceful error reporting to clients.

## Problem

The provided `bug.js` file includes an Express.js route that performs an asynchronous operation. However, if the asynchronous operation fails, the error is only logged to the console; the Express.js application does not send an appropriate error response to the client and could crash unexpectedly. 

## Solution

The solution, shown in `bugSolution.js`, demonstrates the correct way to handle errors in asynchronous routes.  It uses `try...catch` to handle synchronous errors and `.catch()` to handle asynchronous errors. This approach ensures that appropriate HTTP error responses are sent back to the client, preventing crashes and providing better user experience.