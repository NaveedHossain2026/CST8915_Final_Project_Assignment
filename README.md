# CST8915 Final Project: Cloud-Native App for Best Buy

Student Name: Naveed Hossain   

Student ID: 041081882

## Video Demonstration

https://youtu.be/d9siFVTye4U


## Application Overview

![image alt](https://github.com/NaveedHossain2026/rideau-canal-monitoring/blob/41bc77b6cee391f5d69f767bd3286089e089c81a/screenshots/08-dashboard-azure.png)


This project is a cloud-native, microservices-based retail application that resembles Best Buy’s website. The application allows customers to browse products and place orders, while employees can manage products and monitor operations from the admin interface.

The architecture is made up of five different microservices: The Store Front and Store Admin microservices handle the user interface; Product Service manages product data; Order Service handles customer orders; and Makeline Service handles asynchronous order processing in the background. All microservices have been containerized and deployed within Azure Kubernetes Service for scalability and reliability.

The database utilized for storing the products and orders is a MongoDB database that provides persistent and flexible data management. Kubernetes functionalities like ConfigMaps and Secrets are utilized for secure configuration and sensitive data handling.

Additionally, the software makes use of a CI/CD pipeline that uses GitHub Actions to automate the building, testing, and deployment processes for each microservice.

Overall, the application demonstrates modern cloud-native design principles, including microservices architecture, containerization, and automated deployment.

## Deployment Instructions


### Deployment Steps
1.  **Prepare the Kubernetes YAML manifest:** Use the `aps-all-in-one.yaml` file, which contains the configurations for all services, statefulsets, and configmaps.
2.  **Apply the Kubernetes YAML manifest:**
    ```powershell
    kubectl apply -f aps-all-in-one.yaml
    ```
3.  **Verify Pod Status:**
    Ensure all pods, especially infrastructure pods like `mongodb-0` and `rabbitmq-0`, are healthy:
    ```powershell
    kubectl get pods
    ```
4.  **Access the Application:**
    Retrieve the External IPs for the frontend services:
    ```powershell
    kubectl get svc
    ```

---

## Resource Links Table

| Service Name | GitHub Repository | Docker Hub Image Link |
| :--- | :--- | :--- |
| **Store Front** | [store-front](https://github.com/NaveedHossain2026/store-front-L8) | https://hub.docker.com/r/naveedhossain/store-front |
| **Store Admin** | [store-admin](https://github.com/NaveedHossain2026/store-admin-L8) |https://hub.docker.com/r/naveedhossain/store-admin|
| **Order Service** | [order-service-L8](https://github.com/NaveedHossain2026/order-service-L8) |https://hub.docker.com/r/naveedhossain/order-service |
| **Product Service** | [product-service](https://github.com/NaveedHossain2026/product-service-L8) |https://hub.docker.com/r/naveedhossain/product-service |
| **Makeline Service** | [makeline-service](https://github.com/NaveedHossain2026/makeline-service-L8) |https://hub.docker.com/r/naveedhossain/makeline-service |

---
