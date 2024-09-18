# FULLSTACK CONTAINERIZATION WITH TERRAFORM

## Introduction
This project is based on GitHub-repo:

https://github.com/dhomi/fullstack_conteinerized 

- A scenario:
-- As a DevOps specialist
-- I would like to use an IaC tool
-- In order to manage my complete fullstack container environment/infrastructure

## How-To
1) Install / start Docker Desktop
2) Install NodeJS
3) For local running the Act tool is very handy: <https://nektosact.com>
2) After docker-compose go to dashboard: http://localhost:4000/

## Start the container
```docker-compose up --build```
=> at the end of the build you will see the Local IP and the Network IP

### Monitoring
Grafana: http://localhost:4000

- Monitoring dashboard = 'TechLab backend monitor'
- Grafana fetches the data from InfluxDB:8086, and Influx receives the data every couple of seconds from the telegram scraper (from backend)

## Fetch Local IP address
ipconfig | grep IPv4 | awk 'END{print}'  


### View the front- en backend 
Frontend: http://localhost:3000/ 

- The frontend reveives the 'jokes' from the backend running on: http://localhost:8000/
- Stop the Docker container with command ```docker-compose down```

### E2E tests
Open a shell and go to folder "e2e" and run with "act" command

```cd e2e
act
```
### JMeter
Navigate to "jmeter" folder and start act 

```cd jmeter
act
```

## Testing CRUD operations

### Read (GET) all items, returns status: 200:
GET http://localhost:8000

### Read (GET) a specific item by ID, returns status: 200:
GET http://localhost:8000/6

### Create (POST) a new joke, returns status: 201:
POST http://localhost:8000
Body: {"item": "POST nieuwe mop" }

### Update (PUT) an item by ID, returns status: 200:
PUT http://localhost:8000/6
Body: { "item": "PUT update" }

### Delete (DELETE) an item by ID, returns status: 204:
DELETE http://localhost:8000/6


## TODO
- Chaos testing: https://github.com/chaos-mesh/chaos-mesh
- Design architecture blueprint to explain how it works