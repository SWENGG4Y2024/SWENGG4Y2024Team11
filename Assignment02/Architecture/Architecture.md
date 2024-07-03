# The C4 model for visualising software architecture
The C4 model is a set of visual notations and diagrams that help in visualizing the architecture of software systems. It provides a structured approach to representing different levels of abstraction, from high-level system context diagrams to low-level component diagrams.
The C4 model promotes simplicity and clarity in architectural diagrams. It emphasizes the use of a consistent set of symbols and conventions, making it easier for both technical and non-technical stakeholders to understand the software architecture.
# Context Diagram (Level 1): 
This is the highest level of abstraction, representing the system as a whole and showing its external dependencies and interactions.

<img width="721" alt="context" src="https://github.com/SWENGG4Y2024/SWENGG4Y2024Team11/assets/106813243/7387f827-562f-41aa-a189-6a01934bcb42">

# Container Diagram (Level 2): 
This level zooms in on the system and shows the major containers or subsystems that make up the system. A container is a runtime instance, such as a web server, a database, or a desktop application.

<img width="425" alt="container" src="https://github.com/SWENGG4Y2024/SWENGG4Y2024Team11/assets/106813243/e4146ba2-af91-4e82-ba0f-1891188e9ee3">


Sure! Let's dive deeper into Component Diagrams (Level 3) and Code Diagrams (Level 4).

# Component Diagram (Level 3):

**Purpose**:  
A Component Diagram focuses on the internal structure of a container, such as an application or a microservice. It helps in understanding the high-level organization of a system by showing how different parts of the system interact with each other.

**Key Elements**:
1. **Components**: These represent major parts of the system that encapsulate related functionality. Each component typically corresponds to a set of classes or modules that work together to provide a cohesive service or feature.
2. **Interfaces**: These define the points of interaction between components. An interface specifies what services a component provides or consumes without detailing how they are implemented.
3. **Relationships**: The connections between components, which often indicate dependency or communication. This can include usage relationships (one component uses another) or dependency relationships (one component depends on another).

**Benefits**:
- **Modularity**: Helps in understanding the modular structure of a system, making it easier to manage complexity.
- **Maintenance**: Provides a clear picture of the internal workings of a container, facilitating easier maintenance and upgrades.
- **Communication**: Serves as a communication tool among team members, ensuring everyone has a shared understanding of the system architecture.

**Example**:
Imagine an e-commerce application. A component diagram might include components such as:
- **User Management**: Handles user authentication and profile management.
- **Product Catalog**: Manages product listings and details.
- **Order Processing**: Takes care of order creation, payment processing, and order tracking.
- **Notification Service**: Sends email or SMS notifications to users.

# Code Diagram (Level 4):

**Purpose**:  
A Code Diagram provides a detailed view of the code structure within a component. This level of abstraction is crucial for developers who need to understand the nitty-gritty details of how a system is implemented.

**Key Elements**:
1. **Classes**: Represent the main building blocks of the code, typically corresponding to objects in object-oriented programming. Each class contains attributes (data) and methods (behavior).
2. **Interfaces**: Define contracts that classes can implement. An interface specifies methods that a class must implement, ensuring a certain level of functionality.
3. **Modules**: Higher-level groupings of related classes and interfaces. In some programming languages, modules can also encapsulate data and functions.
4. **Relationships**: 
   - **Inheritance**: Shows how classes inherit from one another, sharing common behavior or attributes.
   - **Associations**: Indicate how classes interact or depend on each other.
   - **Dependencies**: Highlight how one class relies on another for its functionality.

**Benefits**:
- **Detailed Understanding**: Provides a thorough understanding of the codebase, making it easier for developers to navigate and modify the code.
- **Implementation Insight**: Helps in identifying potential issues such as tight coupling or poor separation of concerns.
- **Refactoring**: Aids in the process of code refactoring by clearly showing the existing structure and dependencies.

**Example**:
Continuing with the e-commerce application, a code diagram for the **Order Processing** component might include:
- **Order** class: Represents an order, containing attributes like order ID, customer details, and order items.
- **PaymentService** interface: Defines methods for processing payments.
- **CreditCardPayment** class: Implements the PaymentService interface for handling credit card payments.
- **OrderRepository** class: Manages data storage and retrieval for orders.

By understanding both Component Diagrams (Level 3) and Code Diagrams (Level 4), architects and developers can ensure a well-structured, maintainable, and scalable system.


