# Microservice Transaction :smiley:

The project focuses on managing financial transactions through microservices. We have designed two main microservices using Node.js and TypeScript. The first one acts as a REST API responsible for creating new transactions, while the second specializes in validating these transactions, ensuring that the amount does not exceed a predetermined limit, in our case, 1000 PEN (chosen currency).

# Technologies Used

<ol>
  <ul><strong>Node.js y TypeScript</strong>: Node.js provides a server-side JavaScript runtime, while TypeScript adds static typing for safer and more maintainable development.</ul>
  <ul><strong>MongoDB</strong>: We use MongoDB as our database to store transactions. Its flexibility and scalability make it an ideal choice for modern applications.</ul>
  <ul><strong>Kafka</strong>: We implement Kafka as a messaging system for communication between our microservices. This technology allows us to build a robust and fault-tolerant event architecture.</ul>
  <ul><strong>Docker Compose</strong>: To facilitate the deployment and management of our development environment on different systems, we use Docker Compose. This tool allows us to define and run multiple containers efficiently.</ul>
</ol>





# Application Diagram

![Diagrama de Aplicaciones](https://github.com/MyPortfolio-Cesar/microservices-kafka/blob/master/assets/Diagrama%20de%20aplicaciones.png)


# Prerequisites:

In order to run and view the project logs, I recommend downloading **Docker Desktop** to have a more intuitive graphical interface of how the containers are being managed and to view the system logs.

Link to the official Docker Desktop page to download it: https://www.docker.com/products/docker-desktop/

Don't forget to have ports **3001** and **3002** free to be able to run the microservices.

# Installation and execution

To run the application, you must locate the root path of the project and run the following command in the console: `docker-compose up -d`. This will start the containers defined in the **docker-compose.yml** file in the background.

![Docker containers](https://github.com/MyPortfolio-Cesar/microservices-kafka/blob/master/assets/Docker%20containers.png)

![Microservicio Api](https://github.com/MyPortfolio-Cesar/microservices-kafka/blob/master/assets/Microservice%20API.png)

![Microservicio Validator](https://github.com/MyPortfolio-Cesar/microservices-kafka/blob/master/assets/Microservice%20Validator.png)



**NOTE:** To be able to enter as a client, Swagger is used where the REST API is documented and thus transactions can be created manually.

Swagger is located at `http://localhost:3001/documentation/`.

![Swagger](https://github.com/MyPortfolio-Cesar/microservices-kafka/blob/master/assets/Swagger%20API%20REST.png)

# Observations

- I chose to use Mongoose over TypeORM primarily due to my familiarity and prior experience with the MongoDB and Node.js ecosystem. Mongoose provides me with an intuitive, object-oriented interface to interact with MongoDB, which I find comfortable and efficient. Although I am also familiar with TypeORM and know its advantages, such as its support for multiple relational databases, I decided to use Mongoose for my project.






