# Express.js JSON Body Parsing Issue

This repository demonstrates a common error encountered when working with JSON request bodies in Express.js applications.  The issue arises when body-parser (or a similar middleware) isn't correctly configured or when there is a conflict in middleware order.

## Bug Description

The provided `bug.js` file shows an Express.js server that attempts to handle POST requests containing JSON data. However, due to a setup problem (explained in the solution), the server fails to parse the JSON data correctly; `req.body` remains empty, causing unexpected behavior.

## Solution

The `bugSolution.js` file provides a corrected version of the server.  The solution addresses the parsing issue, ensuring that `req.body` contains the parsed JSON data correctly.

## How to reproduce the bug

1. Clone this repository.
2. Navigate to the root directory.
3. Run `npm install express`.
4. Run `node bug.js`.
5. Send a POST request to `http://localhost:3000/data` with a JSON payload in the request body (e.g., using curl or Postman).
6. Observe that the server receives an empty `req.body`, which means the JSON wasn't parsed successfully.
7. Now repeat steps 3-6 using `bugSolution.js` to see the difference.
