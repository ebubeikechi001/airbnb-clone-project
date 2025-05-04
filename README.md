# Airbnb Clone Project

## 🏗 Project Overview
This project is a full-stack Airbnb clone built to simulate the core functionalities of a modern booking platform. It focuses on backend architecture, security, database design, and collaborative development.

## 🎯 Project Goals
- Understand and implement scalable backend systems.
- Practice collaborative workflows with GitHub.
- Develop secure, well-documented APIs.
- Design and manage efficient CI/CD pipelines.
- Integrate Django, MySQL, GraphQL, Docker, and GitHub Actions.

## 🔧 Tech Stack
- **Backend Framework**: Django
- **Database**: MySQL
- **API Layer**: GraphQL
- **Containerization**: Docker
- **CI/CD**: GitHub Actions
- **Version Control**: Git + GitHub

- ## 👥 Team Roles

In a real-world software project, clear role definition helps ensure smooth collaboration and efficient execution. Below are the key roles and responsibilities for this Airbnb Clone Project:

### 🔹 Backend Developer
Responsible for building the server-side logic of the application using Django. Handles API development, business logic, and system integration.

### 🔹 Database Administrator (DBA)
Designs, manages, and optimizes the MySQL database. Ensures data integrity, performance tuning, and proper indexing of tables.

### 🔹 DevOps Engineer
Implements CI/CD pipelines using GitHub Actions and manages Docker containers. Ensures smooth deployment and monitors server reliability.

### 🔹 Software Architect
Defines the overall system architecture and selects appropriate tools, frameworks, and coding standards. Ensures scalability and maintainability of the project.

### 🔹 QA Engineer
Responsible for testing the application to ensure it meets both functional and non-functional requirements. Develops and runs test cases to catch bugs early.

### 🔹 Product Owner
Maintains the product vision and requirements. Prioritizes features, manages the product backlog, and ensures alignment with user needs.

### 🔹 Business Analyst
Acts as the bridge between stakeholders and the development team. Gathers requirements, maps user workflows, and translates business needs into technical tasks.

## 🧰 Technology Stack

The Airbnb Clone Project leverages a combination of powerful technologies to build a scalable, secure, and maintainable web application. Each tool plays a specific role in the system architecture:

- **Django**: A high-level Python web framework used to develop the backend logic and handle requests, responses, and user authentication.

- **MySQL**: A reliable relational database management system used to store structured data like users, bookings, listings, and reviews.

- **GraphQL**: A query language for APIs that allows clients to request only the data they need, improving efficiency and flexibility in data retrieval.

- **Docker**: A containerization tool that ensures consistent environments across development, testing, and production by packaging the application with all its dependencies.

- **GitHub**: A version control platform for managing the codebase, collaborating with team members, and tracking changes through commits and pull requests.

- **GitHub Actions**: A CI/CD tool used to automate workflows, such as testing and deploying the application when code changes are pushed.

- **Markdown**: A lightweight markup language used to create formatted text for the project documentation, especially in `README.md` files.


## 🗃️ Database Design

The Airbnb Clone Project uses a relational database (MySQL) to manage structured data and relationships. Below are the key entities and their important fields:

### 1. **Users**
Represents users of the platform (both hosts and guests).
- `id`: Unique identifier
- `name`: Full name
- `email`: Email address (unique)
- `password`: Hashed password
- `is_host`: Boolean flag to determine if the user is a host

### 2. **Properties**
Represents listings available for booking.
- `id`: Unique identifier
- `title`: Name of the property
- `description`: Detailed information about the property
- `price_per_night`: Cost of booking per night
- `host_id`: Foreign key linking to the `Users` table

### 3. **Bookings**
Tracks reservations made by users.
- `id`: Unique identifier
- `user_id`: Foreign key linking to the user who made the booking
- `property_id`: Foreign key linking to the property booked
- `start_date`: Check-in date
- `end_date`: Check-out date

### 4. **Reviews**
Captures feedback from users about their stays.
- `id`: Unique identifier
- `user_id`: Foreign key linking to the reviewer
- `property_id`: Foreign key linking to the property reviewed
- `rating`: Numeric score (e.g., 1 to 5)
- `comment`: Textual feedback

### 5. **Payments**
Handles transactions for bookings.
- `id`: Unique identifier
- `booking_id`: Foreign key linking to the related booking
- `amount`: Total amount paid
- `payment_method`: e.g., Credit Card, PayPal
- `status`: Payment status (e.g., successful, failed)

---

### 🔗 Entity Relationships

- A **User** can list multiple **Properties** (one-to-many).
- A **User** can make multiple **Bookings** (one-to-many).
- A **Booking** is made for one **Property** and by one **User** (many-to-one).
- A **Property** can have multiple **Reviews** from different **Users** (one-to-many).
- Each **Booking** has one associated **Payment** (one-to-one).

This design ensures data integrity and models real-world relationships between users, listings, transactions, and feedback.
