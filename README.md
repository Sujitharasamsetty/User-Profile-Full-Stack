# User-Profile-Full-Stack

## When it comes to managing user data, we need a way to create a user profile store and session and associate other documents with them. Let’s define some rules around this user profile store concept:

Store account data like username and password in a profile document.

Pass sensitive user data with each user action request.
Use a session that expires after a set amount of time.
Stored session documents with an expiry limit.
We can manage all of this with the following API endpoints:

POST /account – Create a new user profile with account information
POST /login – Validate account information
GET /account – Get account information
POST /blog – Create a new blog entry associated to a user
GET /blogs – Get all blog entries for a particular user

## Creating the API with Node and Express

This creates a working directory for our project and initializes a new Node project. Our dependencies include the Node.js SDK for Couchbase and Express Framework and other utility libraries like body-parser to accept JSON data via POST requests, uuid for generating unique keys and bcryptjs to hash our passwords to deter malicious users.

### the account documents could represent a form of login credentials where you could have a document for basic authentication (Facebook authentication, etc.) referring to the same profile document. Instead of using a UUID for the session, a JSON Web Token (JWT) or maybe something more secure could be used.
