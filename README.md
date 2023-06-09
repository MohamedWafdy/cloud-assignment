# SIM Cloud Computing Project
This project is a Docker-based RESTful API for managing people. It provides functionality to create, retrieve, update, and delete person documents.

## Docker Image
You can find the Docker image for this project on Docker Hub at the following link: https://hub.docker.com/r/mohamedwafdy/cloud-project-2

## How to run
To run the project, follow these steps:
1. Clone the complete project from GitHub:
```code 
git clone https://github.com/MohamedWafdy/cloud-assignment.git
```
2. Start the application using the docker-compose.yml file:
```code
docker compose up
```
That's it! The application should now be running on http://localhost:4000

## Running the Docker Application on a Different Port
By default, the Docker application runs on port 8080. If this port does not work for you, update the port mapping in the docker-compose.yml file to the desired port.

## Preview
To edit a field in the table, simply click on it and press enter to submit the changes.

Please note that every field is validated, and the changes you make must meet the validation criteria. For example, the "gender" section can be changed to "female" or "male" only. If you try to enter any other value, the change will not be registered.

By following the validation criteria, you can ensure that the data in the application remains accurate and consistent.


![alt text](https://cdn.discordapp.com/attachments/1010542840226517083/1106626826886975689/image.png)

## API endpoints
To test the API in Visual Studio Code, you can use the ***REST Client*** extension. To do this, follow these steps:

1. Install the REST Client extension in Visual Studio Code.
2. Create a new file in your project called "client.rest".
3. In the "client.rest" file, write the commands to test the API using the ***REST Client*** syntax.
4. Save the "client.rest" file.
5. Run the commands in the "client.rest" file using the REST Client extension.

Note: Replace {person-id} with the actual ID of the person you want to delete or update.

### Get All Persons
```client.REST
GET http://localhost:8080/persons
```
### Get Person
```client.REST
GET http://localhost:8080/persons/{person-id}
```
### Delete Person

```client.REST
DELETE http://localhost:8080/persons/{person-id}
```
### Create New Person
```client.REST
POST http://localhost:8080/persons
content-type: application/json

{
"name": "Mohamed",
"age": 21,
"gender": "male",
"email": "mohamedsaeed204@gmail.com"
}
```
### Update Person
```client.REST
PUT http://localhost:8080/persons/{person-id}
content-type: application/json

{
   "email": "example@gmail.com"
}
```

## Technologies used
The following technologies were used in the project:
- Node.js: a JavaScript runtime environment
- MongoDB: a NoSQL database
- Docker: a containerization platform
- React: a JavaScript library for building user interfaces
- Chakra UI: a modular and accessible component library for building React applications with a focus on design system and developer experience

## Credits
This project was created by Mohamed Ibrahim Wafdy.
