# twitter_nodejs

##Twitter Clone API

This project implements a simplified backend API for a Twitter-like application using Node.js and SQLite. It provides endpoints to handle user registration, authentication, tweet management, and social interactions.

## Features

- **User Management:**
  - Register new users
  - Authenticate users with JWT tokens
  - Fetch user details and manage followers

- **Tweet Management:**
  - Post tweets
  - Fetch tweets from users the logged-in user follows
  - Get details of a tweet, including likes and replies

## Project Structure

- **`app.js`:** Main entry point for the application.
- **`twitterClone.db`:** SQLite database file containing tables for users, tweets, followers, likes, and replies.
- **`routes/`:** Directory containing route handlers for different API endpoints.
- **`middlewares/`:** Middleware functions, including JWT authentication.
- **`models/`:** Database models using Sequelize for ORM operations.

## APIs Provided

1. Registration and Login
   - `/register/`: POST request to register a new user.
   - `/login/`: POST request to authenticate and receive a JWT token.

2. Tweet Operations
   - `/user/tweets/feed/`: GET request to fetch tweets from followed users.
   - `/user/tweets/`: GET and POST requests for managing user tweets.
   - `/tweets/:tweetId/`: GET and DELETE requests for specific tweet operations.

3. Social Interactions
   - `/user/following/`: GET request to fetch users followed by the logged-in user.
   - `/user/followers/`: GET request to fetch users following the logged-in user.
   - `/tweets/:tweetId/likes/`: GET request to fetch users who liked a tweet.
   - `/tweets/:tweetId/replies/`: GET request to fetch replies to a tweet.

## Installation

1. Clone the repository:
   ```
   git clone <repository_url>
   cd twitter-clone-api
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Start the server:
   ```
   npm start
   ```

## Usage

- Ensure the SQLite database `twitterClone.db` is properly set up and configured.
- Use tools like Postman or curl to interact with the API endpoints.

## Dependencies

- Express.js: Web framework for Node.js
- SQLite: Embedded SQL database engine
- Sequelize: ORM for Node.js, used for database operations

## License

This project is licensed under the MIT License - see the LICENSE file for details.
