
# Soccer Team Management Service
![Logo](src/main/resources/static/logo.png)

This is a simple CRUD application for managing soccer teams.

## Running the Application
Run the application using Maven:
```
./mvnw spring-boot:run
```

## CRUD Operations

### Create a Team
To create a new team:
```
curl -X POST localhost:8080/teams -H "Content-type:application/json" -d "{ \"name\": \"Team Name\", \"history\": \"Team History\", \"id\": 1, \"pictures\": \"url\", \"logo\": \"url\", \"foundationDate\": \"YYYY-MM-DD\", \"description\": \"Description\" }"
```

### Read Team Information
To retrieve information about a specific team by ID:
```
curl localhost:8080/teams/1
```

To retrieve information about all teams:
```
curl localhost:8080/teams
```

### Update a Team
To update an existing team:
```
curl -X PUT localhost:8080/teams/1 -H "Content-type:application/json" -d "{ \"name\": \"New Team Name\", \"history\": \"New History\", \"id\": 1, \"pictures\": \"new_url\", \"logo\": \"new_url\", \"foundationDate\": \"YYYY-MM-DD\", \"description\": \"New Description\" }"
```

### Delete a Team
To delete a team:
```
curl -X DELETE localhost:8080/teams/1
```

### Find Teams (Assuming Find Functionality Exists)
To find teams based on certain criteria (e.g., name):
```
curl "localhost:8080/teams/search?name=Team+Name"

```
