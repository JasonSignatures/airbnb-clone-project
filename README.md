## Back end Pro Dev Program
| Build RESTful APIs | Manage NoSQL databases | Collaborate effectively using GitHub and Agile practices. |

## 🧑‍🤝‍🧑 Team Roles

Below are the key team roles and their responsibilities in this Backend Development project:

### 1. Backend Developer
Responsible for building and maintaining the server-side logic of the application.  
They design and implement RESTful APIs, handle data processing, and ensure the backend integrates seamlessly with the frontend.  
**Key skills:** Node.js / Python / Java, Express, API design, and version control (Git).

### 2. Database Administrator (DBA)
Manages the database systems used in the project.  
They are responsible for database design, optimization, data security, and backup management to ensure data integrity and performance.  
**Key skills:** SQL / NoSQL, PostgreSQL, MongoDB, database modeling, and data recovery.

### 3. DevOps Engineer
Ensures smooth deployment, integration, and scalability of the backend application.  
They automate workflows, manage servers, and oversee CI/CD pipelines to maintain efficient and reliable operations.  
**Key skills:** Docker, CI/CD tools, cloud services (AWS/Azure), and system monitoring.

### 4. Quality Assurance (QA) Engineer
Tests the backend services and APIs to detect and fix bugs before deployment.  
They create and execute test plans, ensure that features meet requirements, and maintain high software quality.  
**Key skills:** API testing tools (Postman), automated testing frameworks, and bug reporting.

### 5. Project Manager
Coordinates the team, defines goals, manages timelines, and ensures the project stays on track.  
They facilitate communication between developers, clients, and stakeholders to ensure smooth progress.  
**Key skills:** Agile/Scrum methodologies, communication, and project planning.

## 🧩 Technology Stack

Below are the main technologies used in this Backend Development project, along with their purposes:

### 1. **Django**
A high-level Python web framework used to build robust and scalable backend applications.  
It provides built-in features for authentication, database management, and API development.

### 2. **PostgreSQL**
A powerful, open-source relational database management system (RDBMS).  
Used for storing and managing structured data with reliability, performance, and data integrity.

### 3. **GraphQL**
A modern query language for APIs that allows clients to request exactly the data they need.  
It improves efficiency by reducing over-fetching and under-fetching of data.

### 4. **Docker**
Used to containerize the application, ensuring consistency across development and production environments.  
It simplifies deployment and scaling of the backend services.

### 5. **Git & GitHub**
Version control tools that track code changes, enable team collaboration, and manage the project’s source code repository.

### 6. **Postman**
A tool for testing and documenting APIs.  
It helps verify that the backend endpoints work correctly and respond as expected.

### 7. **Heroku (or AWS / Render)**
A cloud platform used for deploying and hosting the backend application, making it accessible online.

## 🗃️ Database Design

The project’s database is designed to efficiently manage user data, property listings, bookings, reviews, and payments.  
It follows a **relational database model** using tables that are linked through foreign key relationships.

---

### **1. Users**
Stores information about all registered users (property owners and customers).

**Key Fields:**
- `id` — unique identifier for each user  
- `name` — full name of the user  
- `email` — user’s email address (used for login)  
- `password` — securely hashed password  
- `role` — defines whether the user is a customer or property owner  

**Relationships:**  
A user can have multiple properties.  
A user can also make multiple bookings and write multiple reviews.

---

### **2. Properties**
Represents the properties (e.g., apartments, houses, hotels) listed by users.

**Key Fields:**
- `id` — unique property identifier  
- `owner_id` — foreign key referencing `Users(id)`  
- `title` — name or title of the property  
- `location` — address or city where the property is located  
- `price_per_night` — cost of booking the property per night  

**Relationships:**  
A property belongs to one user (the owner).  
A property can have many bookings and multiple reviews.

---

### **3. Bookings**
Stores all booking transactions made by users for specific properties.

**Key Fields:**
- `id` — unique booking identifier  
- `user_id` — foreign key referencing `Users(id)`  
- `property_id` — foreign key referencing `Properties(id)`  
- `check_in_date` — start date of the booking  
- `check_out_date` — end date of the booking  

**Relationships:**  
A booking belongs to one user and one property.  
A booking can have one payment record associated with it.

---

### **4. Reviews**
Contains feedback from users who have booked and stayed at properties.

**Key Fields:**
- `id` — unique review identifier  
- `user_id` — foreign key referencing `Users(id)`  
- `property_id` — foreign key referencing `Properties(id)`  
- `rating` — numerical rating (e.g., 1–5 stars)  
- `comment` — text feedback from the user  

**Relationships:**  
A review belongs to one user and one property.  
A property can have many reviews.

---

### **5. Payments**
Tracks the financial transactions for bookings.

**Key Fields:**
- `id` — unique payment identifier  
- `booking_id` — foreign key referencing `Bookings(id)`  
- `amount` — total payment amount  
- `payment_method` — e.g., card, PayPal, or bank transfer  
- `status` — indicates if the payment is pending, completed, or failed  

**Relationships:**  
A payment is linked to one booking.  
Each booking can have one corresponding payment record.

---

### **Entity R**




