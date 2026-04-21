# Hidden Thoughts App

A full-stack web application that allows users to anonymously share confessions. The app includes secure user authentication using both local login and Google OAuth via Passport.js.

Users can now submit a secret, they would be authenticated before adding or displaying their secret

##  Features
* User registration & login (local strategy)
* Google authentication (OAuth 2.0)
* Secure session management with Passport.js
* Anonymous confession sharing
* Dynamic UI with EJS templates

## Tech Stack

* **Backend:** Node.js, Express.js
* **Authentication:** Passport.js (Local + Google OAuth 2.0)
* **Frontend:** EJS, Bootstrap
* **Database:** PostgreSQL

##  Authentication Flow (Google OAuth)

* Users can sign in using their Google account.
* Passport.js handles OAuth authentication using the Google Strategy.
* On successful login:

  * User profile is retrieved from Google
  * User is created or found in the database
  * A session is established
* Users remain authenticated via session cookies.

## Setup

1. Install dependencies:

bash
npm install


2. Create a `.env` file:

- CLIENT_ID=your_google_client_id
- CLIENT_SECRET=your_google_client_secret
- SESSION_SECRET=your_session_secret


3. Run the app:

bash
node index.js

4. Visit:
http://localhost:3000


## Notes

* Google OAuth requires credentials from Google Cloud Console
* Make sure your callback URL matches:


http://localhost:3000/auth/google/callback


##  Author

Martin O
