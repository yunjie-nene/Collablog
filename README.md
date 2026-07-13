# Collablog – Personal Blogging Platform

Collablog is a full-stack university group project. It consists of a Svelte web application for readers and authors, an Express/SQLite backend exposing a REST API, and a Java Swing desktop client used by administrators to manage user accounts.
Both the web frontend and the desktop admin client consume the same REST API.

## Features
### Web application

* User registration and login
* Blog post publishing and browsing
* Likes and comments, including nested comment threads
* Masonry-style homepage post display

### Admin desktop client

* Admin login with session-based authentication
* User list and user detail views
* Delete non-admin user accounts

## Tech Stack

* Frontend: Svelte
* Backend: Express / Node.js
* Database: SQLite
* Desktop client: Java (Swing), Jackson
* API Testing: Postman
* Collaboration: Git, GitHub Pull Requests, Google Sheets

## My Contributions

* Contributed mainly to backend API development and SQLite data handling.
* Supported selected frontend features, including nested comments and masonry-style homepage display.
* Created a Postman collection for API checking.
* Contributed to the Java Swing admin desktop client as part of the team.
* Set up a Google Sheet bug tracker before final delivery to record issues, owners, status, and fixes.
* Helped coordinate Git workflow through branches, pull requests, and code review.

## Architecture
The Express backend exposes a REST API consumed by two separate clients:

* The Svelte web app, used by regular users and authors
* The Java Swing desktop client, used by administrators for account management

The desktop client authenticates against the same login endpoint as the web app and reuses the session cookie for subsequent requests.

## Demo Accounts

Admin account:

* Username: `test01`
* Password: `Ab123456`

Regular user account:

* Username: `test03`
* Password: `Ab123456`

## Setup Notes

Initialise the database before running the project.

Backend formatting check:

```bash
npm run format
```

Frontend formatting check:

```bash
npm run format
```

The desktop client is an IntelliJ project under `desktop-client/`. Dependencies are in `desktop-client/lib/`. The backend must be running on `localhost:3000` before starting the client.

## Development Notes

This project was developed by a 4-person university team. We used feature branches and pull requests for collaboration, and issues found during final testing were tracked in a shared bug sheet.
