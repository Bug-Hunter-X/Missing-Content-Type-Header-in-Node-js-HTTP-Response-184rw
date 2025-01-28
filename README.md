# Missing Content-Type Header in Node.js HTTP Response

This repository demonstrates a common but easily overlooked error in Node.js HTTP servers: omitting the `Content-Type` header in the response.  This can lead to unpredictable client-side behavior.

## Bug

The `bug.js` file shows a simple HTTP server that omits the `Content-Type` header.  This can cause issues depending on the client's expectations.

## Solution

The `bugSolution.js` file corrects the issue by including the `Content-Type` header.  This ensures that the client correctly interprets the response.

## How to Reproduce

1. Clone this repository.
2. Run `node bug.js`.
3. Make a request to `http://localhost:3000` using a tool like `curl` or a browser.  Observe that the client may not correctly handle the response.
4. Run `node bugSolution.js`.
5. Make a request to `http://localhost:3000`.  Observe that the response is now handled correctly.
