# Express.js Route Handler Error: Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  failure to handle invalid or unexpected input. Specifically, this example shows a route that fetches a user by ID, but lacks proper error handling if the provided ID is not a valid integer.

## Bug Description

The `bug.js` file contains an Express.js route that retrieves a user based on their ID.  However, it doesn't validate the ID before attempting to parse it as an integer. If a non-numeric ID is passed, the `parseInt()` function will return `NaN`, leading to a potential crash or unexpected behavior.

## Solution

The `bugSolution.js` file provides a corrected version of the route handler. It includes input validation to check if the ID is a valid integer before proceeding.  If the ID is invalid, an appropriate error response is returned.