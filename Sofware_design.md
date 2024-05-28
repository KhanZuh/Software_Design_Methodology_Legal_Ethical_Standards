# Software Design and Methodology

## What do we mean by coupling and cohesion when discussing structured design?

**Coupling** refers to the degree of interdependence between software modules. In a highly coupled system, changes in one module can heavily impact others, making the system more complex and harder to maintain. The goal is to minimize coupling, achieving low coupling, where modules interact with each other through well-defined interfaces and have minimal dependencies. This makes the system more modular and easier to manage and evolve.

> "Software modules are distinct and self-contained units of code that represent a specific functionality within a software system. Each module is designed to perform a particular task or set of tasks and can be developed, tested, and maintained independently of other modules. Modules often encapsulate a specific aspect of the system's functionality, providing a clear separation of concerns."

**Cohesion** describes how closely related and focused the responsibilities of a single module are. A highly cohesive module performs a single task or a group of related tasks - promoting clarity and ease of maintenance. High cohesion within a module means that its components are strongly related and work together to achieve a specific function, which enhances the module's reusability and robustness.

**In practice - combining low coupling and high cohesion allows for a more modular, maintainable, and scalable system grounded in improved readability, testability, and adaptability.**

## Top-down & Bottom design

Top-down and bottom-up design approaches offer distinct methodologies for system development, both with unique advantages and disadvantages. 

The **top-down** design begins with the overall system and progressively breaks it down into more detailed components. This ensures a cohesive vision but sometimes misses the lower-level details. **Bottom-up** design starts with the most basic elements, gradually integrating them into subsystems and ultimately forming the complete system - which allows for flexibility and adjustments but can risk missing the overarching system cohesion.

**Function-oriented** design aligns more closely with the top-down approach because it begins by defining the system's major functions and incrementally decomposing them into smaller sub-functions, emphasizing processes and high-level decomposition over data structures.

## Class Diagrams

A class diagram would be most useful in the object-oriented design (OOD) methodology. Object-oriented design focuses on structuring a software system as a collection of interacting objects, each representing an instance of a class. These classes encapsulate data and behavior, modeling real-world entities and their relationships.
Class diagrams are a fundamental tool in OOD as they visually represent the classes within a system, along with their attributes, methods, and the relationships between them.
This visualization aids in comprehending the system's architecture, identifying class dependencies, and ensuring adherence to key object-oriented principles like inheritance, encapsulation, and polymorphism. By clearly outlining the system's structural blueprint, class diagrams enhance communication among team members and stakeholders and provide a solid foundation for implementation.

## The Four Pillars of Object-Oriented Programming

- **Encapsulation**: Encapsulation is the bundling of data and methods that operate on the data into a single unit, typically called a class. It restricts access to some of the object's components, usually to hide the internal state of an object and to prevent unauthorized access.

- **Inheritance**: Inheritance is the mechanism in which one class acquires the properties and behaviors of another class. It promotes code reusability and allows the creation of a new class based on an existing class, inheriting its attributes and methods.

- **Polymorphism**: Polymorphism allows objects of different classes to be treated as objects of a common superclass. It enables methods to be written to operate on objects of a base class and then reused for objects of a derived class, providing flexibility and extensibility in the code.

- **Abstraction**: Abstraction refers to the process of hiding the complex implementation details and showing only the necessary features of an object. It focuses on what an object does rather than how it does it, simplifying the programming interface and reducing complexity for the user.

## Strategy Pattern

The Strategy Pattern is a behavioral design pattern that enables defining a family of algorithms, encapsulating each one, and making them interchangeable. This pattern allows the algorithm to vary independently from clients that use it.

In a **functional system**, the Strategy Pattern is typically implemented using higher-order functions or function objects. Here, different strategies are represented as functions, which can be passed around as arguments or stored in data structures.
In contrast, in an **object-oriented system**, the Strategy Pattern involves defining a family of algorithms as separate classes, each implementing a common interface. Clients can then switch between these algorithms by using polymorphism, i.e., by interacting with the common interface rather than the concrete implementations directly.

With these implementations - the difference lies in how the strategies are represented and invoked: functional systems rely on functions or function objects, while object-oriented systems use classes and interfaces.

## Design Methodology for a New Online Payment System

**Decision Matrix**

Structured Design, rooted in a top-down approach, emphasizes the hierarchical decomposition of a system into smaller, manageable modules. While this methodology offers clarity in system organization and facilitates systematic development, it falls short in accommodating the dynamic and evolving nature of the online payment system. The rigidity inherent in structured design may hinder the system's ability to adapt to diverse sectors' unique requirements and may impede scalability and maintainability in the long run.

Function-Oriented Design, characterized by its focus on functions or procedures and their interactions, emphasizes procedural decomposition and emphasizes code reusability. 
This approach may offer some advantages in terms of modularization and code reuse, it lacks the inherent encapsulation and abstraction mechanisms provided by OOD. In the context of an online payment system requiring seamless integration across various sectors, function-oriented design may lead to code redundancy, increased coupling, and decreased maintainability.

Object-Oriented Design (OOD), offers a comprehensive and flexible approach to system design that aligns well with the objectives of the online payment system. At the core of OOD lies the concept of encapsulation, which enables the bundling of data and related functionality into cohesive units known as objects. This encapsulation fosters modularity and information hiding, allowing for the development of reusable and interoperable components. OOD promotes inheritance and polymorphism, facilitating code reuse and extensibility. In the context of the online payment system, inheritance can be leveraged to create specialized payment methods tailored to specific sectors while maintaining a common interface. Polymorphism enables the system to handle diverse transaction types and payment processes seamlessly, enhancing its versatility and adaptability.OOD promotes the development of robust and maintainable systems through the use of design patterns. Design patterns, such as the Factory Method pattern or the Strategy pattern, provide standardized solutions to common design problems, promoting code clarity and consistency across the system. This standardized approach simplifies system maintenance and enhances collaboration among development teams.

Additionally, OOD aligns well with industry best practices and frameworks, ensuring compatibility and interoperability with existing systems and technologies. This compatibility is essential for maximizing market reach and ensuring seamless integration with various platforms and services.

Object-Oriented Design emerges as the preferred methodology for developing the online payment system due to its inherent flexibility, modularity, extensibility, and compatibility with industry standards. While Structured Design and Function-Oriented Design offer certain advantages, they are inherently limited in their ability to accommodate the dynamic and evolving nature of the online payment system and may impede scalability and maintainability in the long run.
