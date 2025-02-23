# Express.js - Empty req.body despite using express.json()
This repository demonstrates a common issue in Express.js applications where `req.body` remains empty even after using `express.json()`. The bug and its solution are provided in separate `.js` files.

## Bug (`bug.js`)
The provided `bug.js` file shows an Express.js server that attempts to parse a JSON request body using `express.json()`.  However, due to a missing configuration, `req.body` is empty.

## Solution (`bugSolution.js`)
The `bugSolution.js` file demonstrates the corrected code. It includes the necessary middleware to correctly parse the JSON request body.

## How to reproduce the bug:
1. Clone this repository.
2. Navigate to the directory `cd <repo_name>`.
3. Run `node bug.js`. 
4. Send a POST request with a JSON body (e.g., using Postman or curl) to `http://localhost:3000/data`.  The server will log an empty `req.body`.

## How to test the solution:
1. Run `node bugSolution.js`. 
2. Repeat step 4 above.  The server will now log the correct JSON data.

## Contributing
Contributions are welcome! Feel free to open an issue or submit a pull request.