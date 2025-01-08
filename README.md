# Unresponsive Node.js Server

This repository demonstrates a common Node.js issue: an unresponsive server caused by a long-running synchronous operation that blocks the event loop.  The `bug.js` file contains code that simulates this problem.  The `bugSolution.js` file provides a solution using asynchronous operations.

## Problem

Node.js is single-threaded, meaning it handles all requests within a single thread.  A long-running synchronous operation in the request handler blocks this thread, preventing the server from responding to other requests. This leads to an unresponsive server. 

## Solution

The solution involves refactoring the code to use asynchronous operations.  This prevents blocking the event loop and ensures the server remains responsive.