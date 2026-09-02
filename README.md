# Car Rental System 🚗

Car Rental System is a production-grade, full-stack enterprise web application engineered to modernize and streamline vehicle leasing operations. Built using a decoupled, scalable architecture—leveraging a robust Spring Boot RESTful API for the backend and a high-performance Angular 16 component-driven frontend—the platform manages the complete reservation lifecycle. From secure customer onboarding and dynamic fleet inventory tracking to complex reservation state management and optimized relational data handling with MySQL, this system solves core real-world engineering challenges like data consistency, secure role-based access control, and seamless user experiences.

- 🌐 **Live Application Link:** [Launch Car Rental System](https://eloquent-illumination-production-5301.up.railway.app)

---

## 🛠 Tech Stack
- **Frontend:** Angular 16 (Signals, RxJS, Angular Material)
- **Backend:** Spring Boot (Java, REST APIs, Spring Security)
- **Database:** MySQL
- **Tools:** Git/GitHub, Maven, Postman

## ✨ Key Features
- **Secure Authentication:** User login and logout functionality with role-based access.
- **Vehicle Catalog:** Browse available vehicles with real-time status updates.
- **Booking System:** Seamless reservation process with input validation.
- **Admin Dashboard:** Tools for managing inventory and viewing booking history.

## 📸 Screenshots
Register Page

<img width="998" height="593" alt="Register Page" src="https://github.com/user-attachments/assets/22397bcc-2833-47bb-b16a-bf0ccab1e1dd" />

Register as Client

<img width="996" height="593" alt="Register Client" src="https://github.com/user-attachments/assets/dc000591-3a19-444d-ab89-930d07def618" />

Register as Company

<img width="997" height="594" alt="Register Company" src="https://github.com/user-attachments/assets/9d993461-96d7-4daf-95aa-dd0b6b02a720" />


Login Page

<img width="763" height="505" alt="Login Page" src="https://github.com/user-attachments/assets/1eafe907-09ad-48b5-9c3d-d07dc5e2f2d9" />


Vehicle Catlog

<img width="1032" height="634" alt="Available cars page" src="https://github.com/user-attachments/assets/e7ad1335-c028-4c4f-9c8b-6591e81354dd" />


Search a Car

<img width="1352" height="642" alt="Search" src="https://github.com/user-attachments/assets/259c1baf-48c0-4bd0-8133-11aefbe681ca" />


Booking a Car

<img width="1361" height="533" alt="Booking a car" src="https://github.com/user-attachments/assets/d78fb421-6809-4d1a-9a69-1f9f75e68748" />

Admin Dashboard 

<img width="1065" height="486" alt="Dashboard Page" src="https://github.com/user-attachments/assets/ccaf95ff-a1ea-43e1-97b1-13ff4eea70bf" />



## ⚙️ Installation & Setup

### Method A: 🐳 The Dockerized Setup
This project is fully containerized and orchestrated using **Docker** and **Docker Compose**. It separates the architecture into isolated, high-performance environments while maintaining secure connectivity to the underlying data layer.

#### Architecture Breakdown
* **Frontend Container (`ServiceBookingWeb`):** Uses a multi-stage Docker build. Stage 1 utilizes a lightweight Node.js environment to compile optimized production bundles. Stage 2 serves these static assets using a high-performance **Nginx** reverse-proxy web server on port `8081`.
* **Backend Container (`ServiceBookingSystem`):** Uses a multi-stage Maven compilation process to generate a production-ready executable `.jar` file, running dynamically on an **Eclipse Temurin OpenJDK 17** runtime on port `9090`.
* **Database Link:** Integrated directly with the host network interface to communicate seamlessly with localized database configurations.

#### 🚀 How to Run with Docker

1. **Open Ports:** Make sure native web servers (like Apache) are stopped to avoid port conflicts:
   ```bash
   sudo systemctl stop apache2
   ```
2. **Spin Up the Stack:** Navigate to the root directory of the project and execute the orchestrator script:
   ```bash
   docker compose up --build
   ```
   *Note: For subsequent runs, you can drop the `--build` flag to launch the entire full-stack system instantly in under 3 seconds:*
   ```bash
   docker compose up
   ```
3. **Access Modules:** Once the initialization loops settle:
   * **Car Rental UI Landing Page:** Open your browser and navigate to `http://localhost:8081`
   * **REST API Gateway Endpoints:** Operating seamlessly at `http://localhost:9090`

---

### Method B: Manual Local Setup

### 1. Database Setup
1. Create a MySQL database named `service_booking_system_db`.
2. Update `src/main/resources/application.properties` with your MySQL username and password.

### 2. Backend (Spring Boot)
```bash
cd backend
mvn clean install
mvn spring-boot:run
```

### 3. Frontend (Angular)
```
cd frontend
npm install
ng serve
```
Once the server is running, open your browser and navigate to:

http://localhost:4200

