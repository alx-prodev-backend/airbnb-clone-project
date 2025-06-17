
# Airbnb Clone Project
# Team Roles
## 📌 Team Roles and Responsibilities

### 🔍 Business Analyst (BA)
- Understands customer’s business processes
- Translates customer business needs into requirements
- Bridges the gap between a customer and the development team
- Aligns customer vision with technical implementation
- Helps define requirements and manage workflows

### 🎯 Product Owner (PO)
- Owns the product vision and guides its evolution
- Ensures the final product meets customer requirements
- Defines business strategy and manages product backlog
- Works closely with the BA to align goals and implementation
- More customer-oriented than technical

### 🛠️ Project Manager (PM)
- Delivers the product on time and within budget
- Manages and motivates the development team
- Facilitates communication and transparency in Agile projects
- Connects high-level stakeholder goals with team execution

### 🎨 UI/UX Designer
- Transforms the product vision into user-friendly designs
- Handles user research, wireframing, prototyping, and visual design
- Ensures functional and engaging user experiences
- Works throughout the development lifecycle

### 🧠 Software Architect
- Designs high-level architecture of the software product
- Selects appropriate tools, platforms, and technologies
- Sets code standards and conducts code reviews
- Ensures security, stability, and scalability

### 💻 Software Developer
- Implements the actual code for the application
- Front-End Developers: Build user-facing parts of the application
- Back-End Developers: Implement core logic, algorithms, and integrations
- Full-Stack Developers: Handle both front-end and back-end tasks

### ✅ Quality Assurance (QA) Engineer
- Verifies if the application meets all requirements
- Tests both functional and non-functional aspects (performance, usability, etc.)
- Creates test cases, scenarios, and documents results
- Designs procedures to prevent defects during development

### 🤖 Test Automation Engineer
- Writes and maintains scripts for automated testing
- Builds test automation ecosystems
- Identifies what should be automated vs. tested manually
- Ensures cost-effective and valuable automation

### 🔄 DevOps Engineer
- Links development and operations teams
- Automates and unifies software delivery (CI/CD pipelines)
- Facilitates continuous integration and code release processes
- Balances speed and stability in software updates

---

> This document provides a comprehensive overview of team member roles for the Airbnb Clone Project. Each role is critical for delivering a functional, user-friendly, and stable application.

## 🧰 Technology Stack

Here are the key technologies used in this project, along with their roles:

- **Django**: A high-level Python web framework that encourages rapid development and clean, pragmatic design. It is used to build the server-side logic and RESTful APIs for the application.

- **PostgreSQL**: A powerful, open-source object-relational database system. It is used as the primary database to store and manage structured data for the application.

- **GraphQL**: A query language for APIs and a runtime for executing those queries. It provides a flexible and efficient approach to accessing and manipulating data from the frontend.

- **HTML/CSS/JavaScript**: Core frontend technologies used to build the user interface of the web application.

- **Docker**: A containerization platform used to package the application and its dependencies for consistent and scalable deployment across environments.

- **Nginx**: A web server used to serve static files and act as a reverse proxy for the Django application, improving performance and scalability.

- **Gunicorn**: A Python WSGI HTTP Server for UNIX. It is used to serve the Django application in production.

- **Git & GitHub**: Version control system and platform for collaboration and source code management.

---

> This tech stack allows us to build a scalable, efficient, and user-friendly Airbnb Clone application with modern web technologies.

## 🗂️ Database Design

This section outlines the core entities and their relationships in the Airbnb Clone project:

### 🧑 Users
- **id**: Unique identifier for the user
- **name**: Full name of the user
- **email**: Email address (used for login)
- **password_hash**: Hashed password for security
- **role**: Indicates if the user is a host or guest

### 🏡 Properties
- **id**: Unique identifier for the property
- **owner_id**: Foreign key linking to the User who owns the property
- **title**: Short descriptive title of the property
- **description**: Detailed property information
- **location**: Physical address or coordinates

### 📅 Bookings
- **id**: Unique identifier for the booking
- **user_id**: Foreign key linking to the User who made the booking
- **property_id**: Foreign key linking to the booked Property
- **check_in**: Date of arrival
- **check_out**: Date of departure

### ⭐ Reviews
- **id**: Unique identifier for the review
- **user_id**: Foreign key linking to the User who submitted the review
- **property_id**: Foreign key linking to the reviewed Property
- **rating**: Numeric score (e.g., 1–5 stars)
- **comment**: Textual feedback from the user

### 💳 Payments
- **id**: Unique identifier for the payment
- **booking_id**: Foreign key linking to the related Booking
- **amount**: Total payment amount
- **payment_status**: Indicates if payment is completed or pending
- **payment_date**: Date of the transaction

### 🔗 Entity Relationships
- A **User** can be both a **host** (owns properties) and a **guest** (books properties).
- A **User** can have many **Properties**.
- A **Property** can have many **Bookings**.
- A **Booking** is associated with one **User** and one **Property**.
- A **Property** can have many **Reviews**.
- A **Review** is linked to one **User** and one **Property**.
- A **Booking** can have one **Payment**.

---

> This design enables efficient tracking of users, property listings, booking schedules, user feedback, and payment records.


## Feature Breakdown

### ✨ Main Features
This Airbnb Clone project offers a robust set of core features to simulate the functionalities of a real-world property rental platform:

### 👥 User Management
Users can sign up, log in, and manage their profiles. The system supports different roles, such as hosts (property owners) and guests (travelers), ensuring tailored experiences for each user type.

### 🏠 Property Management
Hosts can list properties with detailed descriptions, pricing, availability, and images. This feature allows property owners to manage and update their listings efficiently.

### 📆 Booking System
Guests can view property availability and make reservations for specific dates. The system ensures that bookings do not overlap and provides confirmation to both hosts and guests.

### 💬 Reviews and Ratings
Users can leave reviews and rate properties after completing their stays. This feedback mechanism builds trust within the platform and helps guests make informed decisions.

### 💳 Payment Integration
A secure payment module handles booking transactions. It processes payments, tracks payment statuses, and generates receipts to ensure transparency and accountability.

### 🔎 Property Search and Filters
Guests can search for properties using keywords, location, and filters like price range or amenities. This feature improves the user experience by helping them find suitable options quickly.

