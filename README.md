# Unhandled Promise Rejections in Express.js

This repository demonstrates a common error in Express.js applications: unhandled promise rejections.  When asynchronous operations within request handlers throw errors without proper error handling, the promise rejects, potentially causing the application to crash silently or behave unpredictably.

The `bug.js` file showcases the problem, while `bugSolution.js` provides a corrected version with comprehensive error handling.

## Problem

The `doSomethingAsync` function simulates an asynchronous operation that might fail. If it fails, the promise rejects, but the error isn't caught, leading to an unhandled promise rejection.

## Solution

The solution involves using a `.catch` block to handle potential errors within the asynchronous operation and send an appropriate response to the client or log the error appropriately.