# Knowledge Base for Software Engineer GPT

## Requirements Engineering

Requirements engineering is a coordinated set of activities for exploring, evaluating, documenting, consolidating, revising, and adapting the objectives, capabilities, qualities, constraints, and assumptions that the system-to-be should meet based on problems raised by the system-as-is and opportunities provided by new technologies.
## Business Analyst
A business analyst has the primary responsibility for the requirements engineering activities. A business analyst is the point person who has to forge this customer-dev collaborative partnership. The skilled analyst is patient and well organized, has effective interpersonal, communication and facilitation skills, with technical and business domain knowledge, and the right personality. The business analyst is usually a project role, not necessarily a job title. A software team may have a dedicated specialist as a business analyst, or in most cases, a team member who also performs other project functions. A business analyst is also known as requirements analyst, system analyst, requirements engineer, requirements manager, application analyst, business system analyst, IT business analyst, analyst, product manager, or product owner.
## Requirements
What are requirements in software engineering? Requirements are a specification of what should be implemented. They are descriptions of how the system should behave, or of a system property or attribute. They may be a constraint on the development process of the system. This definition acknowledges that diverse types of information that collectively are referred to as “the requirements”.

Here are various types of requirements for a software project:

- Business requirements
- Features
- User requirements
- Functional requirements
- Quality attributes, also known as non-functional requirements
- Business rules
- External interface requirements
- Constraints
- Data requirements

The requirements in the above list are not on the same abstraction level. Requirements like business requirements and features are intentionally abstract, while user requirements and functional requirements are concrete and detailed. With that understanding, a business analyst needs to organize the business requirements, features, user requirements, functional requirements, and quality attributes in a requirements hierarchy where requirements at a lower-level add more details or elaborate a higher-level requirement.

Business requirements are located at the top level of this hierarchy. They can be refined or elaborated by a set of features. The features support the business requirements. Each feature can then be refined into a set of user requirements if the system-to-be has a lot of user interactions. Finally, each user requirement is refined into a set of detailed and testable functional requirements and quality attributes. This refinement approach is very similar to the top-down design in programming.

This requirements hierarchy provides useful context for both the customers and the development team at appropriate levels of abstraction and helps properly structure and trace requirements.

### User Requirements

User requirements describe goals or tasks the users must be able to perform with the system-to-be that will provide value to some stakeholders. User requirements are also known as user needs, user goals, tasks need to be done with the system-to-be. This is a user-centric and usage-centric requirements engineering approach. User requirements are usually elicited by business analysts and user representatives or a product manager depending on the type of the software (Software for internal corporate use or Software for commercial sale). They must align with the context and objectives that the business requirements and features establish.

User requirements are most typically represented as use cases, scenarios, or user stories.

The name of a use case corresponds to an important feature of the system-to-be. A use case describes this feature by a series of user (the primary actor) and system interactions that help users accomplish something that brings value to them. Stated differently, a use case describes how users and the system work together to realize the identified feature.

Use cases are popular and efficient in user requirements specification largely because they tell stories about how the system will behave in use. They primarily capture the functional requirements of the system-to-be. So, use cases can be used to derive functional requirements, test cases, analysis models, and data requirements.

What is the format of a use case? A use case has the following elements:

- Use Case ID and Name: Give each use case a unique integer sequence number identifier. State a concise name for the use case that indicates the value the use case would provide to some user. Begin with an action verb, followed by an object. For example, UC-1: enroll in a course.
- Author and Date Created: Enter the name of the person who initially wrote this use case and the date it was written.
- Primary and Secondary Actors: An actor is a person or other entity external to the software system being specified who interacts with the system and performs use cases to accomplish tasks. Different actors often correspond to different user classes or roles, identified from the customer community that will use the system-to-be. Name the primary actor that will be initiating this use case and any other secondary actors who will participate in completing execution of the use case.
- Trigger: Identify the business event, system event, or user action that initiates the use case. This trigger alerts the system that it should begin testing the preconditions for the use case so it can judge whether to proceed with execution.
- Description: Provide a brief description of the reason for and outcome of this use case, or a high-level description of the sequence of actions and the outcome of executing the use case.
- Preconditions: List any activities that must take place, or any conditions that must be true before the use case can be started. The system must be able to test each precondition. Label each postcondition in the form PRE-X, where X is a sequence number. Example: PRE-1: User’s identity has been authenticated.
- Postconditions: Describe the state of the system at the successful conclusion of the use case execution. Label each postcondition in the form POST-X, where X is a sequence number. Example: POST-1: Price of item in the database has been updated with the new value.
- Main Success Scenario/Normal Flow: Provide a description of the user actions and corresponding system responses that will take place during execution of the use case under normal, expected conditions. This dialog sequence will ultimately lead to accomplishing the goal stated in the use case name and description. Show a numbered list of action steps performed by the actor, alternating with responses provided by the system. An action step is either an interaction between two actors (“The Customer enters address info into the system.”) or a validation step to protect interest of a stakeholder (“The System validates the PIN code.”) or an internal change to satisfy a stakeholder (“The System deducts amount from balance.”).
- Extensions: Extensions work this way. Each action step in the main success scenario may branch because of a particular condition. The condition can be either an alternative success scenario or an exception. Write down the condition and then write the action steps that handle it. The condition and its handling steps are called an extension. It is possible that an action step in the main success scenario may have multiple extensions.
  - Alternative Success Scenarios: Document other successful usage scenarios that can take place within this use case. State the alternative success scenario as the condition. Number each alternative success scenario in the form “XY”, where “X” is a number that references an action step in the main success scenario and “Y” is a letter that identifies an alternative success scenario for that action step. For example, “5b” would indicate the second alternative success scenario for action step 5.
  - Exceptions: Describe any anticipated error conditions that could occur during execution of the use case and how the system responds to those conditions. Number each exception handling flow in the form “XY”, where “X” is a number that references an action step in the main success scenario and “Y” is a letter that identifies an exception for that action step. For example, “5b” would indicate the second exception for action step 5.
- Priority: Indicate the relative priority of implementing the functionality required to allow this use case to be executed. Use the same priority scheme as that used for the functional requirements.
- Frequency of Use: Estimate the number of times this use case will be performed per some appropriate unit of time. This gives an early indicator of throughput, concurrent usage loads, and transaction capacity.
- Business Rules: List any business rules that influence this use case. Don’t include the business rule text here, just its identifier so the reader can find it in another repository when needed.
- Associated Information: Identify any additional requirements, such as quality attributes, for the use case that may need to be addressed during design or implementation. Also list any associated functional requirements that aren’t a direct part of the use case flows but which a developer needs to know about. Describe what should happen if the use case execution fails for some unanticipated or systemic reason (e.g., loss of network connectivity, timeout). If the use case results in a durable state change in a database or the outside world, state whether the change is rolled back, completed correctly, partially completed with a known state, or left in an undetermined state as a result of the exception.
- Assumptions: List any assumptions that were made regarding this use case or how it might execute.

### Functional Requirements

The use case describes the system’s behavior under various conditions as it responds to a request from the user. However, software developers don’t implement user requirements. They implement functional requirements. Functional requirements are the software capabilities that must be implemented by the developers for the user to carry out a feature’s service or to perform a use case. Functional requirements often are written from the perspective of the system-to-be and in the form of the traditional “The system shall” statements. A business analyst documents these functional requirements in the Software Requirements Specification (SRS). Then how does a business analyst write functional requirements?

Use cases describe tasks that users will need to perform with the system, or user-system interactions that will result in a valuable outcome for some stakeholder. That understanding leads the business analyst to derive the necessary functional requirements that must be implemented to enable each use case. Developers might implement an entire use case in a single release or iteration. Alternatively, they might implement just a portion of a particular use case initially, either for size or priority reasons, and then implement additional parts in future releases.

A business analyst needs to examine each element of a given use case (main success scenarios, extensions, preconditions, postconditions) to look for pertinent functional and non-functional requirements and to derive test cases. This helps the business analyst avoid overlooking any requirements that developers must implement to let users perform the use case.

A business analyst starts with examining each action step in the main success scenario and the extensions. The action steps taken by the system based on user action steps can be converted into traditional functional requirement statements about what functionality the system shall support. To accomplish this, each action step of a use case should be considered to see if there are any system functions necessary to support executing that action step. If there are, those are functional requirements. In other words, for each action step, a business analyst needs to think/specify/elaborate  enough details (e.g., data requirements, business rules, non-functional requirements) so that the developers know how to implement each action step and the testers know how to derive test cases. Many functional requirements fall right out of the dialog steps between the actor and the system. Such as, “The system shall assign a unique sequence number to each request.” Other functional requirements don’t appear in the use case description. Such as what the system shall do if a precondition is not satisfied.

A business analyst needs to use the name of each use case as a feature name, and organize  functional requirements derived in this use case under this feature. The problem is the exact text from the scenarios doesn’t stand on its own very well as an itemized functional requirement. Even though the text is copied from the scenarios, a business analyst would constantly reword a little, or add some context around it.

Preconditions and postconditions are also important sources of functional requirements. Preconditions define prerequisites that must be met before the system can begin executing the use case. The system should be able to test all preconditions to see if it’s possible to proceed with the use case. Postconditions describe the state of the system after the use case is executed successfully. Postconditions can describe:

- Something observable to the user (“The system displays an account balance.”)
- Physical outcomes (“The ATM has dispensed money and printed a receipt.”)
- Internal system state changes (“The account has been debited by the amount of a cash withdrawal, plus any transaction fees.”)

Many postconditions are evident to the user, because they reflect the outcome that delivers user value, for example “I’ve got my cash from the ATM.” However, no user will ever tell a business analyst that the system should reduce its record of the amount of cash remaining in the ATM by the amount the user just withdrew. Users neither know nor care about such internal housekeeping details. But developers and testers need to know about them, which means that the business analyst needs to discover those, perhaps by working with a subject matter expert, and record them as additional postconditions.

Some error conditions could affect multiple use cases or multiple steps in a use case’s normal flow. Examples are a loss of network connectivity, a database failure partway through an operation, or a physical device failure such as a paper jam. Treat these as additional functional requirements to be implemented, instead of repeating them as exceptions for all the potentially affected use cases. The goal is not to force-fit all known functionality into a use case. You’re employing usage-centric elicitation to try to discover as much of the essential system functionality as you can.

Granularity of functional requirements. Write individually testable functional requirements. If you can think of a small number of related test cases to verify that a requirement was correctly implemented, it is probably at an appropriate granularity. If you envision numerous and diverse tests, perhaps several requirements are combined and ought to be separated.

## Requirements Document Templates

Project glossary document template: https://docs.google.com/document/d/1yqUkax6duHvEfFCP50IP16yoxQGyDaMHBT-CxUA73zk/edit?usp=sharing

Vision and scope document template: https://docs.google.com/document/d/1h7Bho4auvUAE5zuPNh4Jkk0TBSNfom8P8F_e11kugqY/edit?usp=sharing

Use case document template: https://docs.google.com/document/d/1vaoprKQn58N4uE5gLaqLFLWtvsBYralnNWP_7rj4vJY/edit?usp=sharing

## Software Development Process

You need to follow an opinionated light-weight development process that incorporates software requirements analysis, object-oriented design, and testing.

You start the development journey by understanding the provided glossary document, the business requirements in a vision and scope document, and the user requirements in use case format. After getting familiar with the project and requirements, you are asked to refine user requirements into detailed functional and non-functional requirements. Those requirements are critical for software design. Then, you are asked to design one or more UML sequence diagrams for each use case. The purpose of the design is to discover key objects, assign responsibilities to them, and model their interactions so that the objects can carry out the functional requirements of the use case. Finally, based on the functional requirements and sequence diagrams produced in the previous steps, you are asked to design test cases based on the test-driven development (TDD) approach.

## Software Architecture

In this design, we adopt a simplified Clean Architecture. The entire application is divided into layers such as controllers layer, services layer, and domain objects layer.

The controllers layer converts data from the format most convenient for the services layer and domain objects layer, to the format most convenient for some external agency such as the Web, and vice versa. Objects in this layer correspond to the design classes discussed later on in the “Object-Oriented Design (OOD) Guidelines” section. Frameworks like Spring Boot have direct support to the controllers using the @Controller or @RestController annotation.

Services layer: The software in this layer contains application specific business logics. It encapsulates and implements all of the use cases of the system. These services orchestrate the flow of data to and from the domain objects and direct those objects to use their enterprise-wide business logics to achieve the goals of the service (use case). Objects in this layer correspond to the design classes discussed later on in the “Object-Oriented Design (OOD) Guidelines” section. Frameworks like Spring Boot have direct support to the services using the @Service annotation.

Domain objects layer is also known as entities layer. This layer contains the core business objects of the application or the problem domain. Objects in this layer correspond to the analysis classes discussed later on in the “Object-Oriented Design (OOD) Guidelines” section.

## Object-Oriented Design (OOD) Guidelines

You now have a list of functional requirements for object-oriented design. During object-oriented design, you need to:

- identify key classes that users use to describe the problem domain and implementers use to describe the solution domain,
- assign responsibilities to each class,
- provide properties and operations to each class that are needed to carry out these responsibilities,
- come up with an object collaboration so that the objects of the classes can collaborate to carry out the functional requirements of a use case.

You will use classes to model abstractions that are drawn from the problem you are trying to solve or from the technology you are using to implement a solution to that problem. Each of these abstractions is a part of the vocabulary of the system, meaning that, together, they represent the things that are important to users and to implementers. For users, most abstractions are not that hard to identify because they are drawn from the things that users already use to describe their systems. For implementers, these abstractions are typically just the things in the technology that are parts of the solution.

There are two broad categories of classes you need to find: analysis classes and design classes.

An analysis class describes a data abstraction directly drawn from the model of the problem domain. For example, “Plane” in a traffic control system, “Paragraph” in a document processing system, “Part” in an inventory control system. Analysis classes belong to the problem domain or problem space.

A design class describes a software architectural choice. Design classes represent architectural abstractions that help produce elegant, extensible, and maintainable software structures. Those classes can come from various design patterns. Examples include “command” classes in the command pattern, “state” classes in the state pattern, “controller” classes in the MVC pattern, “repository” classes and “service” classes in domain-driven design (DDD), “factory” classes in the factory pattern, “client” classes used to interact with external libraries or API, “adapter” classes in the adapter pattern and so on. Design classes belong to the solution domain or solution space.

### Heuristics for finding the analysis classes

Analysis classes can be found based on the important concepts from the problem domain of the system-to-be. A problem domain is the area of application that needs to be examined to solve a problem. People use software system to obtain answers to certain questions about this problem domain (as in a program that computes the solution to a specific problem), to interact with things in this problem domain (as in a process control system), or to add things to the problem domain (as in a text processing system). From the requirements document, you should pay attention to:

- Terms that occur frequently.
- Terms to which the text devotes explicit definitions.
- Terms that are not defined precisely but taken for granted throughout the document.
- Important abstractions of the problem domain.
- Specific jargon of the problem domain.

You must also note that classes can represent conceptual or intangible things as well as material or tangible or physical things in the problem domain.

When you are assessing whether a certain notion should yield a class or not, here is the right criterion: do the objects of the system under discussion exhibit enough specific operations and properties of their own, relevant to the system and not covered by existing classes? If all of the operations and properties that you can identify for a type of objects are irrelevant in this sense or are already covered by the operations and properties of a previously identified class, the conclusion is that the class itself is irrelevant: it must not yield a class. For example, an elevator control system might not include “Floor” as a class because from the point of view of the elevator system, floors have no relevant properties other than those of the associated integer numbers, whereas a Computer Aided Design system designed for architects will have a “Floor” class - since in that case the floor has several specific properties and operations.

It is easy to find tangible objects in a domain like persons, equipment, sensors, devices, airplanes, employees, paychecks, books, products, tax returns, cars, paragraphs, integrable functions. If you are new to a domain, talk to the Subject Matter Expert (SME) to understand some jargon, terminology, you can find some objects that are not obvious. Another good place to start is the glossary document or wiki of this project.

Some objects in the domain may not be tangible. They can be quite abstract. For example, job satisfaction of employees. What counts is how important the concepts are to the enterprise, and what you can do with them. Here are some examples, “Seniority Rule” for a U.S. congress voting system and “Market Tendency” for a trading system.

Whether material or abstract, classes represent the abstractions that specialists of the domain, be they aerospace engineers, accountants, or mathematicians, constantly use to think and talk about their domain. There is always a good chance - although not a certainty - that such an object type will yield a useful class, because typically the domain experts will have associated significant operations and properties with it.

The provided requirements document is useful for finding classes. However, when faced with a new software project, you should not accept the requirements document as the alpha and omega of wisdom about the problem but should combine it with knowledge about previous developments and available software libraries. The corresponding abstractions are most likely to be found in similar existing software. Try to reuse classes useful for other existing software.

### Heuristics for finding the design classes

When developing a software system, besides all the things that simulate concepts in the problem domain, you need to come up with some utility classes to model the design abstractions, such as “controller” classes, “service” classes, “repository” classes, “client” classes and so on. They corresponds to the objects in the controllers layer and services layer in the clean architecture. Basically, they are utility classes responsible for interacting with databases, IO, external API, devices, UI, network, libraries, and infrastructures. The Domain-Driven Development (DDD) and the clean architecture are good approaches to follow.

A few guidelines are worth noting:

- Many design classes have been devised by others before. By reading books and articles that describe precise solutions to design problems, you will gain many fruitful ideas. You should consult articles written by the lead designers of various industrial projects who describe their architectural solutions in detail, providing precious guidance to others faced with similar problems in telecommunications, real-time systems, web projects, mobile projects, Computer-Aided Design, artificial intelligence, and other application areas.
- The book on “design patterns” by Gamma et al. has started an effort of capturing proven design solutions and is now being followed by several others.
- Reuse is preferable to invention. You can hope that many of the “patterns” currently being studied will soon cease to be mere ideas, yielding instead directly usable library classes.

### Criteria for rejecting candidate classes

Just as you need criteria for finding classes, you need criteria for rejecting candidate classes - concepts which initially appear promising but end up not justifying a class of their own.

In this section, you will see a few signs that usually indicate a bad choice of class. Because design is not a completely formalized discipline, you should not treat these signs as proof of a bad class design; in each case one can think of some circumstances that may make the original decision legitimate. So, what you will see is not “absolute negatives” (sure-fire rules for rejecting a design) but “advisory negatives”: danger signals that alert you to the presence of a suspicious pattern and should prompt you to investigate further.

This table shows the “Danger signal” and “Why suspicious”:

| Danger signal                                                | Why suspicious                                               |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Class with verbal name (infinitive or imperative)            | May be a simple subroutine, not a class.                     |
| Fully effective class with only one exported routine         | May be a simple subroutine, not a class.                     |
| Class described as “performing” something                    | May not be a proper data abstraction.                        |
| Class with no routine                                        | May be an opaque piece of information, not an ADT. Or may be an ADT, the routines having just been missed. |
| Class introducing no or very few features (but inherits features from parents) | May be a case of “taxomania”.                                |
| Class covering several abstractions                          | Should be split into several classes, one per abstraction.   |

The last signal “Class covering several abstract” is a typical imperfect design: A class whose features relate to more than one abstraction. Meilir Page-Jones uses the term connascence (defined in dictionaries as the property of being born and having grown together) to describe the relation that exists between two features when they are closely connected, based on a criterion of simultaneous change: a change to one will imply a change to the other. As he points out, you should minimize connascence across class libraries; but features that appear within a given class should all be related to the same clearly identified abstraction.

All the features of a class must pertain to a single, well-identified abstraction. Here is an example: In an early release of the NeXT library, the text class also provided full visual text editing capabilities. Users complained that the class, although useful, was too big. Large class size was the symptom; the true problem was the merging of two abstractions (character  string, and interactively editable text); the solution was to separate the two abstractions, with a class NSAttributedString defining the basic string handling mechanism and various others, such as NSTextView, taking care of the user interface aspects.

### Typical properties of the ideal classes

Here are some of the typical properties of the ideal classes:

- The class provides a crisp abstraction of something drawn from the vocabulary of the problem domain or the solution domain.
- The class name is a noun or adjective, adequately characterizing the abstraction.
- Embodies a small, well-defined set of responsibilities and carries them all out very well.
- The class represents a set of possible run-time objects, its instances. (Some classes are meant to have only one instance during an execution; that is acceptable too.) 
- Several queries are available to find out properties of an instance. 
- Several commands are available to change the state of an instance. (In some cases, there are no commands but instead functions producing other objects of the same type, as with the operations on integers; that is acceptable too.)
- Is understandable and simple, yet extensible and adaptable.

This list describes a set of informal goals, not a strict rule. A legitimate class may have only some of the properties listed.

The classes derived from the functional requirements shall conform to the SOLID design principles: Single Responsibility Principle (SRP), Open/Close Principle (OCP), Liskov Substitution Principle (LSP), Dependency Inversion Principle (DIP).

## Test-driven Development (TDD)

With a good understanding of the use case requirements, a set of finer-grained functional requirements, class model, and objects interaction model, a developer finally can start the test-driven development.

To develop a feature, test-driven development or TDD asks a developer to write a test first for this feature, before writing any implementation code. This test will fail once being executed since there is no implementation. The developer then writes just enough implementation code to make the test pass. From there, the developer will need to come up with more tests for this feature and refactor the code to make it maintainable.

In the first part, the developer shall demonstrate TDD on the requirement in the Domain Objects layer of the Clean Architecture.

Then, in the second part, the developer shall work outward, and unit test the Services layer object.

Finally, in the third part, the developer shall move further outward, and work on an integration test for the entire requirement at the REST Controllers layer.