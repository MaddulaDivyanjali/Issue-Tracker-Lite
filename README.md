A full-stack Issue Tracker application built as a capstone project using with Spring Boot 3.3 (Backend) and Angular 18 (Frontend) for the Java + Spring + Angular 24-week bootcamp capstone. It enables secure user authentication, role-based access, and full lifecycle issue management.
📋 Project Overview
IssueTracker Lite is a service-desk style application where users can:

✅ Create, read, update, and delete (CRUD) issues
🔍 Search issues by title
🏷️ Filter by status (Open, In Progress, Resolved)
📊 Filter by priority (Low, Medium, High)
📎 Upload and download multiple attachments per issue
📱 Access via responsive, mobile-friendly UI
📖 Interact with a complete REST API with Swagger documentation
🎯 Learning Objectives
✓ Model relational schema and connect Spring Data JPA to MySQL
✓ Design RESTful APIs with validation, global error handling, OpenAPI/Swagger
✓ Build Angular SPA with routing, reactive forms, and responsive layout
✓ Implement file upload/download with secure file storage
✓ Apply clean architecture and coding practices
🛠️ Tech Stack
Backend
Java 21 LTS
Spring Boot 3.3.0
Spring Data JPA
MySQL 8.0+
Maven
SpringDoc OpenAPI 2.1.0 (Swagger)
Frontend
Angular 18.x
TypeScript 5.2
RxJS 7.8
CSS Grid & Flexbox
npm/Node.js LTS
🚀 Quick Start
Prerequisites
JDK 21 (Download)
Maven 3.8+
Node.js LTS
MySQL 8.0+
Angular CLI: npm install -g @angular/cli@18
Step 1: Setup MySQL Database
# Connect to MySQL
mysql -u root -p

# Create database
CREATE DATABASE issuetracker CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
EXIT;
Update server/src/main/resources/application.yaml:

spring:
  datasource:
    url: jdbc:mysql://localhost:3306/issuetracker?serverTimezone=UTC&useSSL=false
    username: root
    password: your_password
Step 2: Run Backend
cd server
mvn clean spring-boot:run
Backend: http://localhost:8080

API: http://localhost:8080/api
Swagger UI: http://localhost:8080/swagger-ui/index.html
Step 3: Run Frontend
cd client
npm install
npm start
Frontend: http://localhost:4200

📁 Project Structure
issuetracker_lite/
├── server/                   # Spring Boot Backend
│   ├── src/main/java/com/example/issuetracker/
│   │   ├── controller/       # REST endpoints
│   │   ├── service/          # Business logic
│   │   ├── repository/       # Data access
│   │   ├── entity/           # Domain models
│   │   ├── dto/              # Data transfer objects
│   │   └── exception/        # Error handling
│   ├── src/main/resources/
│   │   ├── application.yaml  # Config
│   │   ├── schema.sql        # DB schema
│   │   └── data.sql          # Sample data
│   └── pom.xml
│
├── client/                   # Angular Frontend
│   ├── src/app/
│   │   ├── app.component.ts
│   │   ├── issue-list.component.ts
│   │   ├── issue-detail.component.ts
│   │   ├── issue-new.component.ts
│   │   ├── issue-edit.component.ts
│   │   └── services/issue.service.ts
│   ├── angular.json
│   ├── tsconfig.json
│   ├── proxy.conf.json
│   └── package.json
│
├── .github/
│   └── copilot-instructions.md
│
└── README.md
🔌 API Endpoints
Method	Endpoint	Description
GET	/api/issues	List issues (with filters)
GET	/api/issues/{id}	Get issue details
POST	/api/issues	Create issue
PUT	/api/issues/{id}	Update issue
DELETE	/api/issues/{id}	Delete issue
POST	/api/issues/{id}/attachments	Upload files
GET	/api/attachments/{id}/download	Download file
Query Parameters: ?q=search&status=OPEN&priority=HIGH

✨ Key Features
Issue Management
Create, read, update, delete (CRUD)
Search by title
Filter by status (OPEN, IN_PROGRESS, RESOLVED)
Filter by priority (LOW, MEDIUM, HIGH)
Responsive card grid layout
File Management
Upload multiple attachments
Download with original filename
Metadata stored in database
Files stored on disk
Validation & Error Handling
Client-side form validation
Server-side validation with structured errors
Global exception handling
User-friendly error messages
Responsive Design
Mobile-first CSS
Breakpoints: 600px, 768px
Touch-friendly interface
Works on all devices
📚 Sample Data
Auto-loaded on first run:

8 sample issues
4 sample attachments
Various statuses and priorities
🧪 Testing
Swagger UI
Visit: http://localhost:8080/swagger-ui/index.html

Manual Testing
Create an issue
Upload attachment
Search and filter
Edit and delete
🐛 Troubleshooting
MySQL connection error:

Ensure MySQL is running
Check credentials in application.yaml
CORS/API errors:

Verify backend is running on port 8080
Use npm start which configures proxy
Port already in use:

ng serve --port 4201
📖 Documentation
Backend: See server/README.md
Frontend: See client/README.md
API Docs: Visit http://localhost:8080/swagger-ui/index.html
AI Agent Guide: See .github/copilot-instructions.md
🎓 Learning Outcomes
Relational database design with MySQL
Spring Boot REST API development
Validation and error handling
Angular SPA with routing and forms
File upload/download implementation
Responsive web design
Clean code practices
📦 Deliverables Checklist
✓ Source code (backend & frontend)
✓ Database schema and sample data
✓ Complete README with setup steps
✓ Swagger API documentation
✓ Responsive UI
✓ Production-ready code
🚢 Production Deployment
Backend:

cd server
mvn clean package -DskipTests
java -jar target/issuetracker-server-0.0.1-SNAPSHOT.jar
Frontend:

cd client
npm run build
# Deploy dist/ contents to web server
🎉 Success Criteria
✓ App runs locally with README steps ✓ Database connects and tables created ✓ All CRUD endpoints working ✓ File upload & download functional ✓ Angular list, create, edit, detail screens working ✓ Responsive on mobile/tablet/desktop ✓ Validation working client & server side ✓ Error handling displays to users

📞 Support
For detailed information:

Backend setup: server/README.md
Frontend setup: client/README.md
API documentation: Swagger UI at /swagger-ui/index.html
Status: ✅ Complete & Ready Last Updated: December 2025 Version: 1.0.0
