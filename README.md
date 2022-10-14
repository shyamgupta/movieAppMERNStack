# Project Requirements

Containerize Movie Application which is based on MERN stack
Source code for the application is at this [link](https://github.com/samaronybarros/movies-app)
Deploy all containers (front end, server, mongodb) on a Ubuntu 20.04 EC Machine

# Steps Followed

1. Create an EC2 machine (Ubuntu:20.04) and open ports 3000, 8000, 27017 in Security Group.
2. Login to the EC2 machine
3. Execute `git clone https://github.com/samaronybarros/movies-app` to clone the repository
4. `cd movies-app`
5. In `client/src/api/index.js` file, replace 127.0.0.1 with EC2 Public IP in baseURL section
6. In `server/db/index/js` file, replace 127.0.0.1 with either EC2 Public IP or 'mongo'. I've used 'mongo'.
7. Create Dockerfile under `movies-app/client` for client component
8. Create Dockerfile under `movies-app/server` for server component
9. Create `docker-compose.yml` under `movies-app` directory
10. Execute `docker compose up -d` - this will run 3 containers in detahced mode.
11. Visit `EC2_IP_Address:8000` in your browser to view the application and perform CRUD operations.

