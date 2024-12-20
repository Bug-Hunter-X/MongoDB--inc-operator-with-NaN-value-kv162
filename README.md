# MongoDB $inc Operator with NaN Value
This repository demonstrates an uncommon error related to using the `$inc` operator in MongoDB update operations with a `NaN` value.

## Bug Description
Attempting to increment a field using `$inc` with `NaN` results in unexpected behavior, preventing the field from being updated correctly and potentially throwing errors.

## Reproduction
1. Connect to a MongoDB database.
2. Create a collection with a numeric field (e.g., `counter`).
3. Execute the provided `bug.js` script to attempt to increment the field with `NaN`.
4. Observe that the field is not incremented as expected.

## Solution
The provided `bugSolution.js` script demonstrates the corrected approach by ensuring that the increment value is a valid number.  Error handling could also be added to gracefully handle potential cases where the field might not exist or contain non-numeric values.