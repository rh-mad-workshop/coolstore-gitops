# MAD Roadshow Dev Track - Outerloop Labs

This is a hands-on lab experience for building new cloud native applications using Red Hat OpenShift Application Runtimes (Quarkus, Spring Boot, Eclipse Vert.x and Node.js) utilizing a microservices architecture.

## CoolStore Online Store App

CoolStore is an online store web application built using Quarkus, Spring Boot, .Net, AngularJS adopting the microservices architecture.

* **Web**: Angular front-end
* **API Gateway**: Aggregates API calls to back-end services and provides a condenses REST API for front-end
* **Catalog**: a REST API for the product catalog and product information
* **Inventory**: a REST API for product's inventory status

```
                    +-------------+
                    |             |
                    |     Web     |
                    |             |
                    |  AngularJS  |
                    |             |
                    +------+------+
                          |
                          v
                    +------+------+
                    |             |
                    | API Gateway |
                    |             |
                    |    .NET     |
                    |             |
                    +------+------+
                          |
                +---------+---------+
                v                   v
          +------+------+     +------+------+
          |             |     |             |
          |   Catalog   |     |  Inventory  |
          |             |     |             |
          | Spring Boot |     |   Quarkus   |
          |             |     |             |
          +-------------+     +-------------+
```

## OpenShift Pipeline and GitOps

OpenShift Pipeline and GitOps are two complementary tools within the Red Hat OpenShift platform that work together to streamline the process of building, deploying, and managing containerized applications. Here's a breakdown of each and how they interact:

* **Pipeline Integration**: OpenShift Pipelines can be integrated with GitOps workflows. Pipelines can be triggered by changes in your Git repository, allowing for automated builds and deployments whenever code updates are pushed.
* **Delivery Automation**: Once your pipeline builds your application images, OpenShift Pipelines can interact with Argo CD to deploy the updated image to your OpenShift cluster. This creates a seamless CI/CD pipeline where code changes automatically trigger builds, deployments, and configuration updates in your cluster.

