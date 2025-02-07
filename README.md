# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the code attempts to parse a user ID from the request parameters as an integer without checking if the ID is actually a valid integer.  This can lead to unexpected behavior or crashes if the ID is not a number.

## Bug
The `bug.js` file contains the buggy code. The route handler attempts to parse the `id` parameter as an integer without any validation or error handling. If the `id` parameter is not a valid integer, `parseInt(userId)` will return `NaN`, causing the `find` method to fail silently or throw an error.

## Solution
The `bugSolution.js` file provides a corrected version of the code. It includes explicit error handling to check if `userId` is a valid integer and returns a proper error response if it's not.