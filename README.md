# Pinsight Task

## Overview

The task is to create a simple Dockerized user management CRUD REST API with JWT Authentication, RBAC, and billing plan based rate limiting.

## CRUD

The CRUD operations are:
- List Users
- View a user
- Create a user
- Edit a user
- Delete a user

## Data Models

Every user should at least have these fields:
- Username
- Email
- Full Name
- Password
- Billing Plan
- Roles

There should be 3 billing plans, where each one has:
- A name
- A price
- Rate limits for each CRUD operation count per hour

There should be permissions for every CRUD operation and 3 roles: 
- Admin can do everything
- Maintainer can list, add and edit users
- Viewer can list and view users

The Admin user, the permissions and the roles should be seeded into the DB at the API startup

## Rate limiting

Rate limiting should be based around operation count per hour. The operation count should be configured for each CRUD operation and should be based on the billing plan of the user.

## Authentication

The password should be encrypted in the database using the bcrypt algorithm. The authentication should be done with an endpoint accepting the username and the password of the user. In response that endpoint should return a symmetrically signed JWT token containing all the standard JWT claims.

## Docker

The API should be dockerized and also a docker-compose file should be written with the api and the mongodb containers

## Tech Stack

You should use:
- NodeJS
- TypeScript
- ExpressJS / Koa / NestJS
- MongoDB & Mongoose
- Docker & Docker Compose

## Evaluation criteria:
- Task completion level
- Code quality
- Git commits frequency and messages
- Project setup instructions (README)

## Timing

The time to complete the task is 1 week. \
In case of any questions please feel free to contact us anytime, good luck!
