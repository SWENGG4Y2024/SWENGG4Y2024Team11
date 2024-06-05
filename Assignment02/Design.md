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

<img height="500" width="500" alt="Healthsync" src="https://github.com/SWENGG4Y2024/SWENGG4Y2024Team10/blob/main/Assignment-2/UML%20Diagrams/HealthSync.png"> <img height="500" width="500" alt="Healthsync1" src="https://github.com/SWENGG4Y2024/SWENGG4Y2024Team10/blob/main/Assignment-2/UML%20Diagrams/Healthsync1.png">


Features of the HealthSync Application:

a) Footstep & Activity Tracker

b) Heart Monitoring

c) Water consumption & Sleep Tracker

d) BMI Calculator

e) Altimeter - for tracking stairs climbed

f) Online consultation with trainers

g) Diet Monitoring

h) AI-enabled workout schedule

### 2.3 **Software Design Methodology**
In developing the HealthSync Application, the development team adheres to the Agile Model. All achievable requirements are gathered, forming a plan for their realization within a defined timeframe. A model is created, broadening the planning flow and selecting technologies to construct the application. The application's basic layout is built from the chosen tech stack, and any new high-priority requirements introduced are accommodated within the same sprint. After each sprint, a retrospective is conducted to identify areas for improvement in upcoming development tasks, followed by planning for the next sprint.

### 2.4 **Principles of Software Design** 
The principles guiding the design of the HealthSync Application are:

1. Requirement Gathering: Understanding subscriber needs is paramount, with thorough documentation serving as a reference throughout the design process.

2. Iterative Design: Requirements are analyzed iteratively from various stakeholders to create a design reflecting the application upon release.

3. Technical Architecture: Defining the application's technical architecture includes determining necessary components and selecting tools and modules for development.

4. Prototyping: Developing Proof of Concepts (POCs) for essential features gathers feedback crucial for improving software functionality.

5. Design Review and Refinement: Stakeholder feedback informs implementation adjustments, ensuring the requirements and feedback gathered remain distinct.

6. High Performance: Achieving optimal speed, responsiveness, and efficiency is a critical goal in software design.

7. Data Privacy and Security: Member data is securely managed and not shared with third-party applications, with access limited to the application's admin.

8. Continuous Monitoring: Post-release monitoring is essential to track performance, user interactions, and identify and report any illicit activities involving the application by subscribers.

## 3 **Activity Diagram**
<img alt="Activity Diagram" src="https://github.com/SWENGG4Y2024/SWENGG4Y2024Team10/blob/main/Assignment-2/UML%20Diagrams/Activity Diagram-SE.png">



## 4 **Key Issues in Software Design**
### 4.1 Error and Exception Handling

1.	Scalability: The application should be built to support a large and growing user base. This involves designing the architecture, databases, and infrastructure to handle increasing volumes of data, user requests, and concurrent users efficiently.
   
2.	Performance: It is crucial for the Healthsync application to be responsive and perform optimally. This includes optimizing database queries, reducing network latency, and writing efficient code to provide a smooth user experience, particularly when processing real-time data from Healthsync devices.
   
3.	Integration with Healthsync devices: The application must seamlessly integrate with various Healthsync wearable devices. This involves ensuring reliable data synchronization, device pairing, and real-time data streaming. Compatibility with different Healthsync models is essential to provide a consistent user experience across devices.
   
4.	User Interface and User Experience: Creating an intuitive and user-friendly interface is vital. The application should allow users to easily navigate features, track their health data, set goals, and interact with the app. Emphasizing usability, visual appeal, and accessibility will help cater to a diverse user base.

5.	Data Management: A robust data management strategy is necessary for secure storage, backup, and recovery of user data. This includes adhering to data privacy regulations, implementing data anonymization techniques, and regularly performing data backups to prevent data loss.

### 4.2 Security Issues

Protecting user data is paramount in a health and fitness application. Implement strong authentication mechanisms, secure data transmission using encryption, enforce access control to prevent unauthorized access, and follow industry best practices for securing user information. 
Here is the list of security issues that needs to be taken care of while developing a Health and Fitness Application:

1. User Authentication: Implement a robust authentication mechanism to ensure that only authorized users can access their accounts. This includes enforcing password complexity rules and implementing protections against brute-force attacks.

2. Data Encryption: Encrypt sensitive data both at rest and in transit. This includes encrypting data stored on servers and data transmitted between the application and backend systems to protect against unauthorized access and data breaches.

3. Secure APIs: Ensure that APIs exposed for integration with third-party applications are secure and follow industry best practices. Implement strong authentication and authorization mechanisms, rate limiting, and input validation to prevent unauthorized access and API abuse.

4. Secure Data Storage: Employ robust security measures to protect user data stored on servers. This includes using strong encryption algorithms, implementing access controls and permissions, regularly patching and updating software, and conducting regular security audits and vulnerability assessments.

5. Privacy Settings: Provide users with granular privacy settings to control the sharing and visibility of their personal health data. Users should have the ability to choose what information is shared with others, including friends, groups, and social communities.

### 4.3 Concurrency Issues

Developing a health & Fitness Application involves addressing various concurrency issues to ensure smooth and reliable operation. Here are some common concurrency challenges that can be faced in software development:

1. Data Synchronization: Imagine a Healthsync app that syncs data from multiple sources, like Healthsync devices and user entries across various gadgets. It's crucial to handle concurrent data synchronization processes meticulously to avoid data inconsistencies or conflicts.

2. Database Concurrency: When multiple users access and update data simultaneously, it can lead to conflicts and data integrity problems. Implement appropriate concurrency control mechanisms, such as transactions, locks, or optimistic concurrency control, to manage concurrent database access and ensure data consistency.

3. Thread Safety: If your Healthsync app utilizes multiple threads or processes, thread safety is paramount. Make sure shared data structures or resources are accessed and modified securely to prevent data corruption or race conditions. Employ synchronization primitives, thread-safe data structures, or message passing mechanisms to orchestrate concurrent activities.

4. Asynchronous Operations: Healthsync apps often involve asynchronous operations like network requests, data processing, or background tasks. Proper handling of these operations is essential to avoid UI blocking and ensure smooth execution without conflicts or data inconsistencies.

## 5 Software Design Quality Analysis and Evaluation
### 5.1 Non Functional Requirements
Non-Functional Requirements, also referred to as Quality Attributes or System Qualities, delineate the desired characteristics or properties of a software system, defining its overall quality. Key non-functional requirements include:

1. Reliability: This pertains to the software system's capacity to execute its intended functions accurately and consistently over a specified duration. It encompasses attributes like fault tolerance, availability, recoverability, and error handling.

2. Performance: Performance concerns the system's responsiveness, efficiency, scalability, and resource utilization. It encompasses attributes such as response time, throughput, latency, and capacity. Establishing performance goals ensures that the system meets user expectations and can handle anticipated loads.

3. Maintainability: Maintainability concentrates on the ease with which the software can be altered, improved, and repaired throughout its lifecycle. It incorporates attributes such as modularity, readability, extensibility, reusability, and testability. A maintainable system reduces maintenance efforts, facilitates prompt bug fixes, and supports future enhancements.

4. Usability: Usability relates to the simplicity of use, learnability, and user satisfaction with the software system. It encompasses attributes such as user interface design, intuitiveness, consistency, accessibility, and documentation. A usable system ensures a positive user experience and minimizes user errors or frustrations.

5. Interoperability: Interoperability concerns the system's ability to interact and exchange data with other systems or components, typically within a heterogeneous environment. It includes attributes such as adherence to standards, support for protocols and data formats, and compatibility with external systems. Interoperability facilitates seamless integration and collaboration among different software components.

### 5.2 Software Design Quality Analysis and Evaluation Technique

Some quality analysis techniques used are:

1. Code Reviews: This involves manual examination of source code by peers or experts to identify defects, ensure compliance with coding standards, and enhance overall code quality. Code reviews foster collaboration, knowledge sharing, and early bug detection.

2. Static Code Analysis: Static code analysis tools automatically scrutinize source code without executing it, detecting potential coding issues such as syntax errors, code smells, security vulnerabilities, and adherence to coding standards. This technique aids in early defect detection and improvement of code quality.

3. Unit Testing: Unit testing entails crafting and executing small, targeted tests on individual code units, like functions or methods. It verifies the correctness of individual units and aids in early defect identification. Unit testing frameworks and methodologies, such as Test-Driven Development (TDD), are pivotal in ensuring software quality.

4. Security Testing: Security testing focuses on uncovering vulnerabilities and weaknesses in the software's security mechanisms. Techniques include vulnerability scanning, penetration testing, and code analysis to assess the software's resistance to attacks, data protection, and adherence to security standards.

5. Peer Reviews: Peer reviews involve informal discussions or inspections where team members review and provide feedback on artifacts such as requirements documents, designs, or test plans. This technique fosters knowledge sharing, identifies inconsistencies, and enhances overall quality through collaborative feedback.
