# Express.js Route Parameter Handling and Error Handling

This repository demonstrates a common error in Express.js route parameter handling and provides a solution for more robust error management.

## Bug

The original code lacks proper error handling for cases where the requested user does not exist. It returns a simple 'User not found' message without providing any context or specific error codes.  This makes debugging and client-side error handling more difficult.

## Solution

The solution improves error handling by:

1.  Explicitly checking if the `userId` is a valid integer.
2.  Returning more informative error messages with appropriate HTTP status codes (400 for bad request, 404 for not found).
3.  Using try-catch to handle potential database errors.

## How to run

1.  Clone this repository.
2.  Run `npm install` to install dependencies.
3.  Run `node bug.js` to see the buggy code in action.
4.  Run `node bugSolution.js` to see the improved version.