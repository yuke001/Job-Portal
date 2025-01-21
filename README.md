# Job Portal

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Directory Structure](#directory-structure)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [License](#license)

## Introduction
The **Job Portal** application is a web-based platform designed to connect job seekers and recruiters. Job seekers can search and apply for jobs, while recruiters can post job openings, view applications, and manage candidate profiles. The application also includes features like profile management, email notifications, and role-based access.

## Features
### For Job Seekers:
- Register and complete profiles.
- Browse and search for jobs.
- Apply for jobs and track application status.

### For Recruiters:
- Register and manage job postings.
- View and manage job applications.
- Access a list of applied candidates.

### General Features:
- Secure login with OTP verification.
- Role-based access control.
- Email notifications for job applications and updates.
- Responsive design for different devices.

## Technologies Used
- **Java**: Core application logic.
- **Spring Boot**: Backend framework.
- **Thymeleaf**: Templating engine for dynamic HTML pages.
- **MySQL**: Database for storing job portal data.
- **Maven**: Dependency and build management.
- **Cloudinary API**: For image uploads.
- **HTML/CSS**: Frontend structure and styling.

## Directory Structure
```plaintext
└── yuke001-job-portal/
    ├── mvnw
    ├── mvnw.cmd
    ├── pom.xml
    ├── src/
    │   ├── main/
    │   │   ├── java/
    │   │   │   └── com/
    │   │   │       └── jsp/
    │   │   │           └── job_portal/
    │   │   │               ├── JobPortalApplication.java
    │   │   │               ├── controller/
    │   │   │               │   ├── GeneralController.java
    │   │   │               │   ├── JobSeekerController.java
    │   │   │               │   └── RecruiterController.java
    │   │   │               ├── dto/
    │   │   │               │   ├── Education.java
    │   │   │               │   ├── Experience.java
    │   │   │               │   ├── Job.java
    │   │   │               │   ├── JobApplication.java
    │   │   │               │   ├── JobSeeker.java
    │   │   │               │   └── Recruiter.java
    │   │   │               ├── helper/
    │   │   │               │   ├── AES.java
    │   │   │               │   ├── CloudinaryHelper.java
    │   │   │               │   ├── MessageRemover.java
    │   │   │               │   └── MyEmailSender.java
    │   │   │               ├── repository/
    │   │   │               │   ├── ApplicationRepository.java
    │   │   │               │   ├── JobRepository.java
    │   │   │               │   ├── JobSeekerRepository.java
    │   │   │               │   └── RecruiterRepository.java
    │   │   │               └── service/
    │   │   │                   ├── JobSeekerService.java
    │   │   │                   ├── MyExceptionHandler.java
    │   │   │                   └── RecruiterService.java
    │   │   └── resources/
    │   │       ├── application.properties
    │   │       ├── static/
    │   │       │   └── assets/
    │   │       └── templates/
    │   │           ├── (various HTML templates for UI)
    │   └── test/
    │       └── java/
    │           └── com/
    │               └── jsp/
    │                   └── job_portal/
    │                       └── JobPortalApplicationTests.java
    └── .mvn/
        └── wrapper/
            └── maven-wrapper.properties
```

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yuke001/Job-Portal.git
   cd Job-Portal
   ```

2. **Configure Database**
   - Open `src/main/resources/application.properties`.
   - Set your MySQL database credentials:
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/job_portal
     spring.datasource.username=your-username
     spring.datasource.password=your-password
     ```

3. **Install Dependencies**
   Use Maven to install required dependencies:
   ```bash
   ./mvnw clean install
   ```

4. **Run the Application**
   Start the application using:
   ```bash
   ./mvnw spring-boot:run
   ```

5. **Access the Application**
   Open your browser and navigate to:
   ```
   http://localhost:8080
   ```

## Usage
- Register as a job seeker or recruiter.
- Use the dashboard to manage your profile, jobs, and applications.

## License
This project is licensed under the [MIT License](LICENSE).

---

Feel free to contribute to the project by submitting issues or pull requests!

