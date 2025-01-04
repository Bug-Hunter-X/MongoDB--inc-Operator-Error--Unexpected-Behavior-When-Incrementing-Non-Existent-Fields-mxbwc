# MongoDB $inc Operator Error
This example demonstrates a common error when using the `$inc` operator in MongoDB. Specifically, it illustrates the issues arising from incrementing a non-existent field and potential type mismatch issues.

The `bug.js` file shows the incorrect code that leads to the error. The `bugSolution.js` file presents a corrected version that handles these potential issues gracefully.

## How to reproduce the bug:
1. Ensure you have a MongoDB instance running.
2. Create a collection (e.g., `users`) with documents that may or may not contain an 'age' field.
3. Execute the code in `bug.js`. Observe the results, which may be unexpected if the `age` field is not present in all documents.

## How to solve the bug:
Use the corrected code in `bugSolution.js`.  This version includes a check for the field and uses the `$setOnInsert` operator to handle cases where the field is missing.

This example highlights the importance of careful data validation and handling potential edge cases when working with MongoDB.