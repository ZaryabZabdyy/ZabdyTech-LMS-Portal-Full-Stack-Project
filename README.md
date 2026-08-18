# Zabdy's Tech LMS Portal 🚀

An enterprise-grade, full-stack Learning Management System (LMS) designed for modern technical education. **Zabdy's Tech** delivers robust course management for disciplines including Artificial Intelligence, Python Programming, and .NET Development. Built with an emphasis on high performance, clean architecture, and decoupled communication, it ensures a seamless and secure learning experience.

---

## 🏗️ Architecture & Technology Stack

### Backend
* **Framework:** ASP.NET Core 8 Web API
* **Architecture:** RESTful principles with clean separation of concerns, structured routing, and explicit HTTP status handling.
* **Data Access:** Entity Framework Core with a tightly normalized, relational SQL Server database schema ensuring optimal query performance and data integrity.
* **Authentication:** Secure stateless authentication mechanisms utilizing JSON Web Tokens (JWT).

### Frontend
* **Core:** Vanilla JavaScript (ES6+), HTML5, and custom modular CSS.
* **Design Philosophy:** Responsive layout emphasizing modern dark-themed aesthetics, structural clarity, and optimized asset delivery without heavy framework overhead.

---

## 📊 Database Schema & Normalization

The system utilizes a fully normalized relational database designed to minimize data redundancy and maintain referential integrity across complex interactions. Core entities include:
* **Users / Students:** Manages profile credentials, roles, and authorization states.
* **Courses:** Houses curriculum metadata for tracks like Python, AI, and .NET Development.
* **Modules & Lessons:** Hierarchical relational mapping linking specific learning nodes directly to parent courses.
* **Enrollments:** Tracks user-to-course associations, progress states, and completion metrics.

---

## 🔌 API Design & Business Rules

The backend exposes clean, versioned REST endpoints returning uniform JSON responses. Business logic rules enforced at the API layer include:
* **Strict Payload Validation:** Ensuring incoming client requests conform to strict data contracts before hitting the database context.
* **Role-Based Access Control (RBAC):** Restricting administrative configuration endpoints while keeping student learning endpoints publicly accessible via valid token authorization.
* **Standardized Response Format:** 

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Operation completed successfully",
  "data": {
    // Payload contents
  }
}
