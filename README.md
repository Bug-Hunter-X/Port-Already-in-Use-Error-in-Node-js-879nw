# Node.js Port Already in Use Error

This repository demonstrates a common error in Node.js: the 'port already in use' error.  The `bug.js` file contains code that attempts to start an HTTP server on port 8080. If this port is already in use by another process, the server will fail to start. The `bugSolution.js` file provides a solution to gracefully handle this scenario.

## Reproducing the Bug

1.  Run `bug.js`.
2.  If successful (unlikely), stop the server (e.g., Ctrl+C).
3.  Run `bug.js` again. You might encounter an error that suggests that the port is already in use, depending on whether the previous process released the port or not.

## Solution

The `bugSolution.js` file demonstrates how to handle this situation more gracefully. Instead of immediately failing, the server now attempts to listen to the port. If unsuccessful, it handles the error and displays a message indicating the issue and exit code.