# finance-api
A production-style Spring Boot backend for managing customers, invoices, and payments, designed to demonstrate enterprise backend development practices commonly used in finance and ERP systems.

This project focuses on clean architecture, security, database migrations, and real-world business logic rather than demo-only CRUD operations.

🚀 **Tech Stack**  
• Java 17  
• Spring Boot 3  
• Spring Web, Spring Security  
• Spring Data JPA (Hibernate)  
• PostgreSQL  
• JWT-based Authentication  
• Liquibase (DB migrations)  
• Docker & Docker Compose  
• JUnit + Mockito  

📌 **Key Features**  
• Role-based authentication (JWT)  
• Customer management  
• Invoice creation with line items  
• Partial and full payment handling  
• Automatic invoice status calculation (UNPAID, PARTIALLY_PAID, PAID)  
• Pagination, filtering, and sorting  
• Centralized exception handling  
• API documentation via Swagger  
• Database versioning with migrations  

🧱 **High-Level Architecture**  
• Controller → Service → Repository → Database  
• Service → DTO / Mapper  
• Controllers handle HTTP concerns only  
• Business logic lives in the service layer  
• Entities are never exposed directly  
• DTOs define API contracts  
• Detailed diagrams are available in the _/docs_ folder.  

🗂 **Project Structure**  
<img width="335" height="494" alt="image" src="https://github.com/user-attachments/assets/0825538b-29f4-414c-aab9-eca71a283fd7" />

🔐 **Authentication & Authorization**  
• JWT-based authentication  
• Roles:  
&nbsp;&nbsp;&nbsp; • ADMIN  
&nbsp;&nbsp;&nbsp; • FINANCE  
&nbsp;&nbsp;&nbsp; • USER  

🧾 **Core Business Flow**
1. Create customer  
2. Create invoice with line items  
3. Post payments (partial or full)  
4. System recalculates invoice balance and status  
5. Retrieve outstanding invoices and reports

🗄 **Database Management**  
• PostgreSQL as primary database  
• Schema managed via Liquibase  
• Versioned migrations ensure consistency across environments  
• Indexes added for commonly queried fields  

▶️ **Running the Application**  
Prerequisites  
• Java 17  
• Docker & Docker Compose  

**Run with Docker (recommended)** : _docker-compose up -d_

📖 **API Documentation**  
Swagger UI is available at: [http://localhost:8080/swagger-ui.html](url)  

🧪 **Testing**  
• Unit tests for service layer  
• Mockito used for mocking repositories  
• Focus on invoice and payment business logic  

📚 **Documentation**  
Additional documentation is available in the /docs directory:  
• Architecture overview  
• Database design  
• Authentication flow  
• Invoice & payment lifecycle  
• Design decisions and trade-offs  

🎯 **Purpose of This Project**  
This repository is built as a portfolio project to demonstrate:  
• Enterprise backend development skills  
• Finance-domain business logic  
• Clean code and layered architecture  
• Production-ready practices (security, migrations, Docker)  

👤 **Author**  
Navishka Kularathna  
Software Engineer  
(Java | Spring Boot | PostgreSQL)



