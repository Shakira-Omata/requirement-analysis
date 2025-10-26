# Requirement Analysis in Software Development 📝

This Project focuses on crafting a comprehensive blueprint for a **Booking Management System**.

The purpose of this project is to simulate a real-world scenario by systematically documenting, analyzing, and structuring all necessary software requirements. This process is crucial in the Software Development Lifecycle (SDLC) for setting a clear, precise, and actionable stage for successful development and execution.


## Project Objectives

* Master the principles and methodologies of Requirement Analysis.
* Efficiently translate project needs into structured documentation.
* Identify and categorize functional and non-functional requirements.
* Leverage visual tools (like Draw.io) for system diagramming.
* Establish clear acceptance criteria for project success.


## Repository Structure (Planned)

As the project progresses, the following files and directories will be added:

* **`README.md`**: Project overview and objectives.
* **`Requirements/`**: Detailed documentation for functional and non-functional requirements.
* **`Diagrams/`**: Visual models (e.g., Use Case Diagram, Activity Diagrams).
* **`Acceptance_Criteria.md`**: Specific criteria for feature validation.



## Why is Requirement Analysis Important?

**Requirement Analysis** is a fundamental and critical stage in the Software Development Lifecycle (SDLC). It is the process of defining, documenting, and maintaining the requirements for a system.

### Key Activities

This process involves several key activities:

* **Requirement Elicitation/Gathering:** Working with stakeholders (users, clients, domain experts) to discover their needs and constraints.
* **Analysis and Negotiation:** Examining the gathered requirements for clarity, completeness, consistency, and feasibility. Conflicts or ambiguities are resolved and negotiated with stakeholders.
* **Documentation:** Formalizing the requirements into structured documents, such as a **Software Requirements Specification (SRS)**, which includes functional and non-functional requirements.
* **Validation:** Reviewing the documentation with stakeholders to ensure the documented requirements accurately reflect their needs and business objectives.

### Importance in the SDLC

Requirement Analysis is the **cornerstone of successful software development** because it transforms abstract business goals into concrete, verifiable specifications.

* **Minimizes Scope Creep:** By clearly defining the boundaries and features of the system early on, it helps prevent uncontrolled changes later in the project.
* **Reduces Development Errors:** A well-defined requirement acts as a precise target. Without it, development teams might build the wrong product, leading to costly rework.
* **Facilitates Accurate Planning:** It provides the necessary input for project managers to create reliable estimates for cost, time, and resources.
* **Establishes Acceptance Criteria:** The documented requirements form the basis for testing and quality assurance, ensuring the final product meets the client's expectations.

## Key Activities in Requirement Analysis

Requirement Analysis is not a single action but a structured process involving several interdependent activities to ensure a clear and complete understanding of the system's needs.

1.**Requirement Gathering:**
This initial, broad phase involves identifying all stakeholders and determining the overall high-level scope and goals of the project. It focuses on the 'Why' and 'What' of the project from a business perspective.

2.**Requirement Elicitation:**
This is the targeted act of drawing out detailed, specific requirements from stakeholders using various techniques. Methods include interviews, workshops (JAD sessions), surveys, prototyping, and observation of current processes. This phase is crucial for bridging the gap between a user's abstract need and a system's tangible specification.

3.**Requirement Documentation:**
This phase involves formally recording all confirmed and analyzed requirements in a structured format, typically resulting in a Software Requirements Specification (SRS) document. Documentation ensures that requirements are stored, managed, and accessible, acting as the single source of truth for the project team.

4.**Requirement Analysis and Modeling:**
Once documented, requirements are systematically analyzed for conflicts, ambiguities, completeness, and feasibility. Modeling uses visual techniques—such as Use Case Diagrams, Class Diagrams, or Activity Diagrams—to represent the system's structure and behavior, ensuring a shared, unambiguous understanding among technical and non-technical team members.

5.**Requirement Validation:**
The final critical step is to verify the documented requirements against the original business objectives. This is done through reviews, inspections, and walk-throughs with stakeholders to ensure the requirements are correct, testable, and truly solve the identified business problem. This activity prevents building the "wrong" system.

## Types of Requirements 

Requirements are broadly classified into two categories, reflecting the "what" (functionality) and the "how" (quality) of the system.

## Functional Requirements (FRs)

Functional Requirements define the specific functions or services the system must perform. They describe the behavior of the system, often in terms of inputs, process, and outputs. They are generally actionable and directly map to user stories.

Examples for the Booking Management System:

**User Authentication:** The system must allow a user to register, log in, and log out securely.

**Search Availability:** The system must allow a user to search for bookable resources (e.g., meeting rooms, appointments, vehicles) based on date, time, and type.

**Booking Creation:** The system must allow a logged-in user to select an available slot and confirm a booking after providing necessary details (e.g., purpose, attendees).

**Confirmation and Notification:** The system must automatically send an email confirmation to the user and the resource provider upon successful booking.

**Cancellation Logic:** The system must allow a user to cancel a booking up to 24 hours before the scheduled time, automatically freeing up the resource.

**Admin Management:** The system must allow an administrator to add, edit, or remove bookable resources and manage user roles.

Non-functional Requirements (NFRs)

Non-functional Requirements define the quality attributes or constraints that the system must satisfy. They specify how well the system performs its functions, often covering aspects like performance, security, reliability, and usability. They are generally measurable.

Examples for the Booking Management System:

**Performance (Response Time):** The search results page must display within 1.5 seconds under normal load conditions.
**Security (Data Protection):** All personally identifiable information (PII) and payment details must be encrypted both in transit (using HTTPS) and at rest (in the database).

**Scalability:** The system must be able to process 5,000 concurrent booking requests during peak hours (e.g., first day of the month) without degradation of service.

**Usability (Accessibility):** The booking interface must conform to WCAG 2.1 AA accessibility standards.

**Reliability (Uptime):** The system must maintain 99.9% uptime, excluding scheduled maintenance windows.

**Maintainability:** New resource types or pricing models must be configurable by administrators without requiring code changes or system downtime.




## Acceptance Criteria

Acceptance Criteria (AC) are a set of predefined conditions that a software feature or functional requirement must satisfy to be accepted as complete by the customer or stakeholder. They are formal, testable statements that define the "done" state of a feature.

Importance in Requirement Analysis

Defines "Done": ACs eliminate ambiguity by providing a clear, objective, and binary (pass/fail) definition of when a requirement is considered complete and functional, moving beyond subjective interpretation.

**Aligns Stakeholders:** They ensure that the development team, QA team, and business stakeholders all share the exact same understanding of the expected outcome and boundaries of the feature.

**Drives Testing:** They are the primary input for quality assurance (QA). Every Acceptance Criterion must be testable, directly forming the basis for test cases.

**Prevents Scope Creep:** By specifying what is included, ACs also help clarify what is not included in the feature, managing expectations and preventing scope drift.

Example for the Checkout Feature

Acceptance criteria are often written using the Gherkin syntax (Given-When-Then), which describes the scenario, the action, and the result.

Feature: Booking Checkout and Payment (FR3)

Scenario

Given (Initial Context)

When (Action Performed)

Then (Expected Result)

Successful Payment

The user is on the checkout page with a reserved slot and provides valid payment details

The user clicks the "Confirm Booking and Pay" button

The system processes the payment, displays a "Booking Confirmed" message, and sends an immediate email confirmation to the user.

Insufficient Funds

The user provides payment details associated with insufficient funds

The payment gateway returns an 'Insufficient Funds' error

The system displays a transactional error message: "Payment Failed: Insufficient Funds. Please try another method." and keeps the resource reserved for 10 minutes.

Simultaneous Booking Failure

The user clicks "Pay" for a slot that was just booked by another user

The system attempts to process the booking and detects the resource lock

The system cancels the transaction and displays a message: "Error: This resource is no longer available. Please select a different time."

