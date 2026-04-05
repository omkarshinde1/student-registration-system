# student-registration-system

🚀 FULL STACK PROJECT SETUP (Angular + Spring Boot + MySQL)

==============================
🔹 PART 1: BACKEND (Spring Boot)
================================

1. Go to: https://start.spring.io

Select:

* Project: Maven
* Language: Java
* Dependencies:

  * Spring Web
  * Spring Data JPA
  * MySQL Driver
  * Lombok

Click Generate → Download → Extract

---

2. Open Project Folder

cd student-backend

---

3. Create Database (MySQL)

Run this in MySQL:

CREATE DATABASE student_db;

---

4. Configure Database

Open file:
src/main/resources/application.properties

Add:

spring.datasource.url=jdbc:mysql://localhost:3306/student_db
spring.datasource.username=root
spring.datasource.password=yourpassword

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

---

5. Run Backend

mvn spring-boot:run

👉 Backend will run on:
http://localhost:9090

==============================
🔹 PART 2: FRONTEND (Angular)
=============================

1. Install Angular CLI (if not installed)

npm install -g @angular/cli

---

2. Create Angular Project

ng new student-frontend

Select:

* Routing: Yes
* Style: CSS

---

3. Open Project

cd student-frontend

---

4. Install Dependencies

npm install

---

5. Run Frontend

ng serve

👉 Open in browser:
http://localhost:4200

==============================
🔹 PART 3: CONNECT FRONTEND + BACKEND
=====================================

1. Use API URL in Angular Service:

http://localhost:9090/api/students

---

2. Enable CORS in Backend Controller:

@CrossOrigin(origins = "http://localhost:4200")

---

==============================
🔹 PART 4: TEST PROJECT
=======================

1. Open:
   http://localhost:4200

2. Test:

* Add Student
* View List
* Update Student
* Delete Student

👉 Project Working ✅

==============================
🔹 COMMON ERRORS
================

Port Error:
Add in application.properties:
server.port=9091

---

Frontend Error:
npm install

---

Connection Error:

* Check backend running
* Check API URL

==============================
🔥 FINAL FLOW
=============

1. Run Backend
2. Run Frontend
3. Open Browser
4. Test CRUD

==============================
DONE 🚀
=======
