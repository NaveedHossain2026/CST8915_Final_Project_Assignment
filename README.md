# CST8915 Final Project: Cloud-Native App for Best Buy

## Application Overview


This project is a cloud-native, microservices-based retail application that resembles Best Buy’s website. The application allows customers to browse products and place orders, while employees can manage products and monitor operations from the admin interface.

The architecture is made up of five different microservices: The Store Front and Store Admin microservices handle the user interface; Product Service manages product data; Order Service handles customer orders; and Makeline Service handles asynchronous order processing in the background. All microservices have been containerized and deployed within Azure Kubernetes Service for scalability and reliability.

The database utilized for storing the products and orders is a MongoDB database that provides persistent and flexible data management. Kubernetes functionalities like ConfigMaps and Secrets are utilized for secure configuration and sensitive data handling.

Additionally, the software makes use of a CI/CD pipeline that uses GitHub Actions to automate the building, testing, and deployment processes for each microservice.

Overall, the application demonstrates modern cloud-native design principles, including microservices architecture, containerization, and automated deployment.
