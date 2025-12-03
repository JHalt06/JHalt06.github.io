---
layout: page
title: Books for the Future
description: Class group project for SWEN-261.
img: assets/img/12.jpg
importance: 1
category: work
related_publications: false
---

**Books for the Future** is a semester-long group software engineering project for a fictional non-for-profit we created.
My team designed and implemented a platform that helps users search, browse, and manage school supplies needs with an intuitive interface and a clean architecture focused on reliability, maintainability, and future extensibility.

The project showcases our work across the full development cycle inluding requirements gathering, design modeling, iterative implementation, and sprint-based development practices. Below is an overview of the system and a visual highlight of our process.

- A searchable and filterable catalog of books  
- Category-based browsing  
- User-focused interface design  
- A scalable multi-tier architecture following established design principles
- Comprehensive developer documentation and diagrams


This platform was developed collaboratively using Agile methods, including sprint planning, backlog management, version control with Git, and continuous team coordination.
---
<!-- <div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div> -->
<!-- <div class="caption">
    Import design documents from the project: 
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Our sprint board helped with sprint planning, tracking progress, assigning tasks, and evolving project requirements.
</div> -->

Between development milestones, we documented decisions, analyzed code impacts, and applied object-oriented software engineering principles such as the Single Responsibility Principle, Open/Close principle, Low Coupling, and Information Expert.

1. Information Expert
  - Responsibility is assigned to the class that has the necessary information to complete fulfill it.
  - The Need class, for example, is responsible for maintaining its own quantity, fund status, and metadata rather than having another class track it.
  - Another example is the DashboardStats class. This class handles important statistics about users and cupboard contents because it has access to all relevant data to do so.

2. Single Responsibility Principle (SRP)
 - Each class has a it's own clear purpose:
 - For example, the Controller Classes:
     CupboardController only handles HTTP requests related to cupboards.
     Notification Controller is soley responsible for managing notification data.
     NotificationService is responsible for sending notifications between the backend and frontend.
 - DAO classes:
      Each DAO handles data for a single entity. If the strategy of storing data changes, only this class needs to be updated.

3. Low Coupling
- Each service and controller only interacts through clear itnerfaces (REST endpoints).
- For example: The NotificationService doesn't directly modify any controllers state. It only makes HTTP requests, so changing its implementation will not break other classes.
- This design principle allows our classes to be cohesive but still loosely connected.

4. Open/Closed
- Our software entities (classes, modules, functions) are open for extension but closed for modification. This means we could easily add new functionality without changing exisiting, tested code.
- The notification system is designed to be extensible. New types of notifications can be added without changing the existing backend or UI logic.
- The Filtering and Sorting utilities in the Needs cupboard can be extended to include new criteria without modifying the substance of the CupboardComponent or service logic.
- DAO classes are designed so that changed to the persistence do not require modifications to main business logic.

## Final Prototype & Features

After weeks of building, testing, and refining, we produced a functioning prototype that demonstrates our full end-to-end workflow: from data handling and logic to UI rendering and user interactions.

## How We Built It

We used multiple technologies and methods:

- **Java** as the primary language  
- **Model–View–Controller (MVC)** architecture  
- **Git & GitHub** workflow with feature branches  
- **Agile sprints**, retrospective evaluations, and task-driven planning  
- **UML diagrams**, sequence diagrams, class models, and architecture documentation  
- **Design principles** such as Infromation Expert, Seperation of Concerns, Low Coupling, and Open/Closed.

This project demonstrates not only the technical outcome but also our team's growth in communication, collaboration, and design thinking.

---