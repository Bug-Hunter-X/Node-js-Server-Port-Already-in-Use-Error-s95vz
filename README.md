# Node.js Server Port Already in Use

This repository demonstrates a common Node.js error: failing to start a server because the specified port is already in use.  The `bug.js` file contains the problematic code, while `bugSolution.js` offers a robust solution.

## Problem

The `bug.js` file attempts to start an HTTP server on port 8080. If another process (e.g., another Node.js server or a different application) is already using that port, the server will fail to start and throw an error.

## Solution

The `bugSolution.js` file provides a more robust solution by handling the `EADDRINUSE` error gracefully. It attempts to start the server on the specified port, and if it fails due to the port being in use, it waits a short period before attempting again. This approach is more resilient and prevents the application from crashing.