# Decagon SSO - System Analysis & Design

**Samson Okemakinde
(Engineering Manager)**

## Overview
DecagonSSO is a SAAS providing single sign on services to customers. It allows customers to add authentication and authorization functions to their applications with just a few clicks.
Single sign-on (SSO) is an authentication method that enables users to securely authenticate with multiple applications and websites by using just one set of credentials.

## Architecture
The application will be designed as a loosely coupled system using **Microservices** architecture to deliver a highly maintainable system, with components that can be independently deployed. This architecture will allow each system component to be:

 - Highly maintainable and testable
 - Loosely coupled
 - Developed and maintained by a small team
 - Focused on a single capability/function

Loose coupling of components will ensure that the system will be adaptable, efficient, flexible and scalable.


**![](https://lh4.googleusercontent.com/SNCKv2dSoSiLB6LakiyFfupoDqWfg1sPzZ3L13I0fQKflJTqXpTZkn00jb2XQwUWK0C1pIO0Tj2YCvjA5gPIPsHjdAN0jr-d3FSFNGhxhnPb3DjkRdcEDNGg1pgZ6s9td19j8FGsUxdT50-sf7fpVho9X9rtyc3ZzF4DkYqtwQF1fVCPeKvwih8_8w00ZA)***Microservices Architecture Diagram***

The SSO microservices architecture will be designed as a loosely coupled system with Object Oriented Programming. An optimal approach to Object Oriented Programming is the SOLID paradigm.
 SOLID stands for:

 - **S-** Single responsbility principle (A class will have only one job)
 - **O-** Open-closed principle (Object should be open for extension but
   closed for modification)
 - **L-** Liskov substitution principle (Every subclass should be
   substitutable for their base class)
 - **I-** Interface Segregration Principle (Clients should not depend on
   methods they don't use)
 - **D-** Dependency inversion principle (Entities must depend on
   abstractions)

 

## Components
**![](https://lh4.googleusercontent.com/B4N20tQo1d0EqNIajBsb5y5E0QsSDwNklycVBevtBTKHy-XdLX3nVieK6GRA8CnDy48flhf7t2HyabpjMwwL8yP4lJAj6idM-O3IFz7iIpkwzDFBDfzryuuwtzcYNPeUTHvoBAOImm_r2O8YXrvIFcO_iLaObMtWAmqdj37K5JdAW8W-WOJ5BwT0yeYVcA)**
***Component Diagram***
 - **Web User Interface :** Provides the login interface to vendor's users.
   It also provides an admin panel for vendors to manage their users and
   other settings.
 - **Web Service / API :** Provides a communication layer between vendors
   and the SSO
  - **Administration Module:** This allows system admins to manage vendors
   and their access for web services, etc.
 - **SSO Database :** The SSO Database is necessary for all the functions of Single Sign-On. The database holds the critical information about the common logins, vendor information, control for consuming the web services.
   **![](https://lh4.googleusercontent.com/yi9Vz9SYFd7_bv78ec2wcQr1uJIy6B_7q7jYASlD5CNB-0SjoaCb3bfLOGmUksfp1Of5iW958E_Ku-Az5oTlLLkLqc-7YOcIa9mA-Q1_qlA4eMX9grrddd0Qhk3OZ4zrtWX4uqlb6XYjV1WQZpi91u2ghaWJAqPe4YVT_7wjh4iS6EilEHUAzHF1CFyMRw)**
   ***Database Design Diagram***


## Technology
 -   **Backend - SpringBoot Framework(Java):** Java is the optimal language for  reliability & high performance systems. SpringBoot is a Java based framework with out-of-the-box support for building service oriented architectures and mitigating the challenges associated with micro-services.
 - **Frontend - ReactJS :** React is a view focused javascript framework that is effective for building API driven web application frontends. React is lightweight, and its component based architecture will enable us to optimize for performance, code reusability and a pleasing user experience. ReactJS is very popular among frontend developers, hence, developers will be readily available to build and maintain the project.**
 - **Database - SQL :** SQL is an industry standard database with optimal support for advanced analytics & complex queries as required by this application.

## Methodology

  **Agile Methodology-:** This will allow us to have small teams working on each microservices in sprints. Features are broken down to tasks which are then structured into a series of 2-week sprints. The Web interface module & Admin Module will have 2 backend and 1 frontend Engineers each. The client-facing API module will have 1 backend engineer.
  
###Team breakdown (9 Engineers)
-   Backend Engineers (SpringBoot) - 5    
-   Frontend Engineers(React + TailwindCSS) - 2
-   QA Engineer (Manual & Automated Testing)  - 1
-   DevOps Engineer - 1


## Deployment
Microservices will be deployed to cloud providers of choice with multiple instances of each service deployed across different regions to ensure high availability.
To ensure that software releases are done properly, each release will pass through the following five stages:
-   Planning : This kicks off the release management process and involves liaising with all the stakeholders involved, getting the proper sign offs and lay out the release process.
-   Building : The software update is prepared for deployment to the staging server. Code cleanup and compiling/building executables ( if required) is done at this stage.
-   Testing : Testing is important to ensure that the software / update is working effectively and is ready for launch. Testing is performed after deployment to the staging server.
-   Preparation : The software is given a final review after testing and is signed off for deployment.
-   Deployment : The software is deployed and tested in a production environment with defined metrics being taken into consideration.

To ensure an hitch free release process, the following notes should be taken:
 -   Automation : All deployments must be as automated as possible to prevent repetition and ensure consistency in processes.
 -   Clear requirements: Acceptance requirements are clearly defined and objective with key release metrics that can be easily measured and checked off.
 -   Staging Environment must be as close to the production environment as possible. This will ensure that successful tests on the staging server will most likely translate to successful production tests too.
 - Minimize User impact : With each release, it is very important to ensure that downtime & negative impact on users is highly minimized. Proactive testing, active monitoring, and real-time alerting will be used to promptly identify and resolve any incidents during a release.

**Containerization**
Microservices will deployed with Kubernetes, guaranteeing the following:
-   AutoScaling - With Horizontal and Vertical pod autoscaling, it will be ensured that the system can scale up / or down by changing the number of pods & resources (CPU & Memory) based on usage.
-   Multiple Regions - Microservice instances will be portable and can be deployed across multiple regions ensuring resiliency.
-   Load Balancing - Load balancer will distribute traffic across available pods ensuring the system is resilient and can withstand high volume of concurrent requests.

![](https://lh5.googleusercontent.com/YYDlT6YgClfTE92ck_7byuCDgcQ0K-CsESNyndHvCCuLN-qDQ3SmII3dKFp1_4zqmiZECQoV_CwAN630y24JWU7t2Bo9dRsdzi9b84RbMi0mh9TRIbVluBRHIfl60EQM0iTmWMFqScxZ_jIVTKAKKG2DvY45c1ulzyTZDjzUBEr83kYWuNB34DSTJBbalQ)
    
**Continuous Integration & Deployment**
**CircleCI :** CircleCI ensures that deployment is automated, and engineers can focus solely on development. Quality assurance ( unit tests, integration tests & static analysis) is automated with the deployment process and a threshold is defined for passing the tests. Deployment to the staging & production servers will be test driven to ensure minimal disruption in operations.

 **Security** 

 - Server Hardening - All deployment servers will be secured following the NIST 800 technical security standards. Effectively blocking intruders, monitoring & eliminating security threats to the system.
       
 -   API Gateway - Microservices will not be available over the internet. All requests will be processed by the API gateway which then communicates securely to the required microservice. Communication between microservices will be through internal VPNs and the API Gateway will be accessed through a Web Application Firewall.
        
 - Web Application Firewall - Web application firewall will ensure that only authorized traffic is permitted to access the system.
