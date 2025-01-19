# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input. Specifically, the provided code attempts to parse a user ID from the request parameters as an integer without verifying if the input is a valid number.  This can lead to unexpected errors and application crashes.

The `bug.js` file contains the buggy code, while `bugSolution.js` provides a corrected version with robust error handling.

## Bug
The primary issue lies in the lack of input validation.  If a non-numeric value is passed as a user ID, `parseInt()` will return `NaN`, causing the `find()` method to fail silently or generate an error depending on the implementation details of the `users` array.