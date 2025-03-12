# Dockorized MERN stack application 

### Create a network for the docker containers
![415943810-a3b7a9ac-401c-4dd1-9846-a6cf252e5f70](https://github.com/user-attachments/assets/0446560b-d542-4e17-a443-73d1de1b5d91)
ITI Supervisor: https://github.com/Ranaahmedit


`docker network create demo`

### Build the client 

```sh
cd mern/frontend
docker build -t mern-frontend .
```

### Run the client

`docker run --name=frontend --network=demo -d -p 5173:5173 mern-frontend`

### Verify the client is running

Open your browser and type `http://localhost:5173`

### Run the mongodb container

`docker run --network=demo --name mongodb -d -p 27017:27017 -v ~/opt/data:/data/db mongodb:latest`

### Build the server

```sh
cd mern/backend
docker build -t mern-backend .
```

### Run the server

`docker run --name=backend --network=demo -d -p 5050:5050 mern-backend`

## Using Docker Compose

`docker compose up -d`
![Capture](https://github.com/user-attachments/assets/eb3c871f-a606-432d-ad49-965e1f475ed5)

## Docker hub 


