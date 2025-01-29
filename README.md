# Firebase Database Reference Access Before Initialization

This repository demonstrates a common error in Firebase applications: attempting to access a Realtime Database reference before it's fully initialized. This often results in `TypeError: Cannot read properties of undefined (reading 'ref')` or similar errors.

The `bug.js` file showcases the problematic code, while `bugSolution.js` provides the corrected implementation.

## Steps to Reproduce

1.  Clone this repository.
2.  Install Firebase: `npm install firebase`
3.  Configure your Firebase project and add your credentials (replace placeholders in the code).
4.  Run `bug.js` (you'll likely see the error).
5.  Run `bugSolution.js` (this should work correctly).

## Explanation

The error arises because database operations are attempted before the Firebase app is initialized and the database reference is available. The solution involves ensuring all database interactions happen after the Firebase app is ready and initialized, often within a callback or promise.