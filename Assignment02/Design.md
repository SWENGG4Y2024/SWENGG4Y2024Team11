# Software Design Document

## Table of Contents
- [1. Project Details](#1-project-information)
- [2. Software Design Fundamentals](#2-software-design-fundamentals)
   -  [2.1 Context of Software Design](#21-context-of-software-design)
   -  [2.2 High Level Application Design](#22-high-level-application-design)
   -  [2.3 Software Design Model](#23-software-design-model)
   -  [2.4 Software Design Principles](#24-software-design-principles)
-  [3. Key Issues in Software Design](#4-key-issues-in-software-design)
   -  [4.1 Error and Exception Handling](#41-error-and-exception-handling)
   -  [4.2 Security Issues](#42-security-issues)
   -  [4.3 Concurrency Issues](#43-concurrency-issues)
-  [4. Activity Diagram](#3-activity-diagram)
-  [5. Software Design Quality Analysis and Evaluation](#5-software-design-quality-analysis-and-evaluation)
   -  [5.1 Non Functional Requirements](#51-non-functional-requirements)
   -  [5.2 Software Design Quality Analysis and Evaluation Technique](#52-software-design-quality-analysis-and-evaluation-technique)

## 1 **Project Information**
The Personal Health and Wellness Assistant is an application designed to help users manage their health and wellness. It provides features such as tracking physical activity, monitoring dietary intake, managing sleep patterns, and offering personalized health recommendations. The goal is to enhance the user's overall well-being through data-driven insights and recommendations.


## 2 **Software Design Fundamentals**
### 2.1 **Contextual Overview of Software Design**
The Personal Health and Wellness Assistant operates within the broader context of health and fitness applications. It interacts with various sensors (like fitness trackers and smartwatches), external APIs (for weather, nutrition information, etc.), and databases to store and process user data.

### 2.2 **High Level Application Design**
The application comprises the following high-level components:

User Interface (UI): The frontend that users interact with, including dashboards and data entry forms.
Backend Server: Handles business logic, data processing, and interactions with the database.
Database: Stores user data, preferences, and historical health information.
Third-party Integrations: Interfaces with external services for additional data (e.g., weather, nutritional databases).

<img height="500" width="500" alt="Nutrition" src="https://github.com/SWENGG4Y2024/SWENGG4Y2024Team11/blob/main/Assignment02/target.webp"> 


Features of the Personal Health and Wellness Assistant Application:

a. User Registration and Authentication

b. Personalized health tracking

c. Goal and monitoring

d. Activity Tracking and Workouts

e. Nutrition Tracking and Meal Planning

### 2.3 **Software Design Model**
Personal Health and Wellness Assistant Application, the development team adheres to the Agile Model.A desired plan was made of how these requirements can achieved in a stipulated amount of time. Creation of model was done where the planning flow was broadened up and a set of technologies were decided to construct the application, from the decided tech-stack the basic layout of application was built and if a new high priority requirement was introduced, was entertained in the same sprint. After the completion of sprint, retrospective is conducted to know what can be improved in upcoming development tasks. After the completion of retrospective, planning for next sprint starts.

### 2.4 **Principles of Software Design** 
The principles guiding the design of the HealthSync Application are:

1. Gather Requirements: It is crucial to understand the application's needs from a subscribed member's perspective. Documenting these requirements serves as a reference throughout the design process.

2. Designing the Model in Iterations: Analyze the gathered requirements from various stakeholders and create an iterative design of how the application should look upon release.

3. Creating Technical Architecture: Define the overall architecture of the application, including all the necessary technical components and the tools and modules to be used during development.

4. Prototyping a Feature: Develop a Proof of Concept (POC) focusing on the most important and basic features required by subscribed members. Gather feedback to improve the software's functionality.

5. Design Review and Refinement: After collecting feedback from stakeholders, implement the necessary changes and refine the model and architecture. Ensure that the requirements and feedback gathered are not repetitive.

6. High Performance: Aim for high performance to ensure the application operates with optimal speed, responsiveness, and efficiency.

7. Data Privacy and Security: Ensure that subscribed members' data is used securely and is not shared with third-party software. Access to member data should be restricted to the application admin only.

8. Continuous Monitoring: Monitor the application post-release to assess its performance and user interactions. Ensure the application is monitored to detect and report any illegal activities conducted by subscribed members.

## 3 **Activity Diagram**
<img alt="Activity Diagram" src="https://github.com/SWENGG4Y2024/SWENGG4Y2024Team11/blob/main/Assignment02/Activity Diagram-SE.png">



## 4 **Key Issues in Software Design**
### 4.1 Error and Exception Handling

1.	Scalability: The application should be built to support a large and growing user base. This involves designing the architecture, databases, and infrastructure to handle increasing volumes of data, user requests, and concurrent users efficiently.
   
2.	Performance: It is crucial for the Healthsync application to be responsive and perform optimally. This includes optimizing database queries, reducing network latency, and writing efficient code to provide a smooth user experience, particularly when processing real-time data from Healthsync devices.
   
3.	User Interface : Creating an intuitive and user-friendly interface is vital. The application should allow users to easily navigate features, track their health data, set goals, and interact with the app. Emphasizing usability, visual appeal, and accessibility will help cater to a diverse user base.

4.	Data Management: A robust data management strategy is necessary for secure storage, backup, and recovery of user data. This includes adhering to data privacy regulations, implementing data anonymization techniques, and regularly performing data backups to prevent data loss.

5.	Validation: Ensure all user inputs are validated before processing.

### 4.2 Security Issues

Protecting user data is paramount in a health and fitness application. Implement strong authentication mechanisms, secure data transmission using encryption, enforce access control to prevent unauthorized access, and follow industry best practices for securing user information. 
Here is the list of security issues that needs to be taken care of while developing a Health and Fitness Application:

1. User Login: Implement a robust authentication mechanism to ensure that only authorized users can access their accounts. This includes enforcing password complexity rules and implementing protections against brute-force attacks.

2. Data Safety: Encrypt sensitive data both at rest and in transit. This includes encrypting data stored on servers and data transmitted between the application and backend systems to protect against unauthorized access and data breaches.

3. Privacy : Provide users with granular privacy settings to control the sharing and visibility of their personal health data. Users should have the ability to choose what information is shared with others, including friends, groups, and social communities.

4. Secure APIs: Ensure that APIs exposed for integration with third-party applications are secure and follow industry best practices. Implement strong authentication and authorization mechanisms, rate limiting, and input validation to prevent unauthorized access and API abuse.

5. Secure Data Storage/Disaster management: Employ robust security measures to protect user data stored on servers. This includes using strong encryption algorithms, implementing access controls and permissions, regularly patching and updating software, and conducting regular security audits and vulnerability assessments.



### 4.3 Concurrency Issues

Developing a health & Fitness Application involves addressing various concurrency issues to ensure smooth and reliable operation. Here are some common concurrency challenges that can be faced in software development:

1. Data Synchronization: Imagine a Healthsync app that syncs data from multiple sources, like Healthsync devices and user entries across various gadgets. It's crucial to handle concurrent data synchronization processes meticulously to avoid data inconsistencies or conflicts.

2. Database Concurrency: When multiple users access and update data simultaneously, it can lead to conflicts and data integrity problems. Implement appropriate concurrency control mechanisms, such as transactions, locks, or optimistic concurrency control, to manage concurrent database access and ensure data consistency.

3. Asynchronous Operations: Healthsync apps often involve asynchronous operations like network requests, data processing, or background tasks. Proper handling of these operations is essential to avoid UI blocking and ensure smooth execution without conflicts or data inconsistencies.

4. Thread Management: If your Healthsync app utilizes multiple threads or processes, thread safety is paramount. Make sure shared data structures or resources are accessed and modified securely to prevent data corruption or race conditions. Employ synchronization primitives, thread-safe data structures, or message passing mechanisms to orchestrate concurrent activities.



## 5 Software Design Quality Analysis and Evaluation
### 5.1 Non Functional Requirements
Non-Functional Requirements, also referred to as Quality Attributes or System Qualities, delineate the desired characteristics or properties of a software system, defining its overall quality. Key non-functional requirements include:

1. Usability
The application should have a user-friendly interface that is easy to navigate and intuitive to use.Usability relates to the ease of use, learnability, and user satisfaction with the software system. 

2. Performance
 The application should perform efficiently, with minimal lag or downtime, even during peak usage periods.Performance relates to the system's responsiveness, efficiency, scalability, and resource utilization. It encompasses attributes like response time, throughput, latency, and capacity. 

3. Security
User data should be securely stored and protected from unauthorized access or breaches.


4. Compatibility
The application should be compatible with various devices and operating systems to ensure accessibility for users across different platforms.

5. Maintainability: Maintainability focuses on the ease with which the software can be modified, enhanced, and repaired over its lifecycle. It includes attributes such as modularity, readability, extensibility, reusability, and testability. A maintainable system reduces maintenance efforts, enables quick bug fixes, and supports future enhancements.


### 5.2 Software Design Quality Analysis and Evaluation Technique

Some quality analysis techniques used are:

1. Code Reviews: This involves manual examination of source code by peers or experts to identify defects, ensure compliance with coding standards, and enhance overall code quality. Code reviews foster collaboration, knowledge sharing, and early bug detection.

2. Static Code Analysis: Static code analysis tools automatically scrutinize source code without executing it, detecting potential coding issues such as syntax errors, code smells, security vulnerabilities, and adherence to coding standards. This technique aids in early defect detection and improvement of code quality.

3. Unit Testing: Unit testing entails crafting and executing small, targeted tests on individual code units, like functions or methods. It verifies the correctness of individual units and aids in early defect identification. Unit testing frameworks and methodologies, such as Test-Driven Development (TDD), are pivotal in ensuring software quality.

4. Automated Testing: Implement unit tests, integration tests, and end-to-end tests to validate functionality.

5. Performance Testing: Conduct load testing and stress testing to ensure the system meets performance requirements.

6. User Testing: Gather feedback from real users to assess usability and make improvements.

7. Security Testing: Perform penetration testing and vulnerability scanning to identify and mitigate security risks.
