# 🔔 Campus Event Portal & Email Notifier

[![Java](https://img.shields.io/badge/Language-Java-brightgreen.svg)](https://www.java.com/)
[![Spring Boot](https://img.shields.io/badge/Framework-Spring%20Boot-6DB33F.svg)](https://spring.io/projects/spring-boot)
[![MySQL](https://img.shields.io/badge/Database-MySQL-4479A1.svg)](https://www.mysql.com/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## 🚀 Project Overview

The **Campus Event Portal & Email Notifier** is an integrat web-based system designed to solve problem of inconsistent and often missed communication within  institutions. It centralizes all academic, placement,  and administrative announcements into a single, unified portal and automatically notifies subscribed students via real-time email alerts.

This system moves communication away from informal channels (like WhatsApp groups and manual emails) to provide a streamlined, organized, and reliable information flow.

## ✨ Key Features

* **Centralized Event Feed:** Students can view all upcoming events (title, description, date, time, location) in one responsive web portal.
* **Secure Authentication:** Faculty and administrators can securely log in  post new events.
* **Category-Based Subscription:** Students can subscribe to specific categories of interest (e.g., **Placement**, **Technical**, **Cultural**, **Sports**, **Academic Notices**).
* **Smart Email Notification Module:** Utilizes **JavaMailSender** to automatically retrieve the list of subscribed students and send personalized email alerts in real time whenever new event is posted in their chosen category.
* **Robust Data Management:** All user data, event details, and subscription preferences are managed securely using a **MySQL database**.

## 🛠️ Technology Stack

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Backend/Core Logic** | Java | Primary programming language. |
| **Web Framework** | Spring Boot | Provides a robust, scalable, and easy-to-configure platform for the REST API and business logic. |
| **Email Service** | JavaMailSender | Used for automating personalized email notifications. |
| **Database** | MySQL | Stores application data, including user credentials, events, and subscription mapping. |
| **Frontend** | HTML/CSS/JavaScript | Designed to be simple, responsive, and user-friendly for easy mobile and desktop access. |

## ⚙️ Setup and Installation

Follow these steps to set up the project locally:

### Prerequisites

* Java Development Kit (JDK) 17+
* Maven (for dependency management)
* MySQL Server (local or cloud instance)
* An email service account (e.g., Gmail) configured for application-specific passwords for `JavaMailSender` integration.

### Steps

1.  **Clone the Repository:**
    ```bash
    git clone [YOUR_REPO_URL]
    cd campus-event-portal
    ```

2.  **Database Configuration:**
    * Create a MySQL database named `campus_events`.
    * Update the `src/main/resources/application.properties` file with your database credentials and JavaMailSender settings:
        ```properties
        # Database Settings
        spring.datasource.url=jdbc:mysql://localhost:3306/campus_events?useSSL=false&serverTimezone=UTC
        spring.datasource.username=YOUR_DB_USERNAME
        spring.datasource.password=YOUR_DB_PASSWORD
        spring.jpa.hibernate.ddl-auto=update # Use 'create' for first run

        # Email Notification Settings
        spring.mail.host=smtp.gmail.com
        spring.mail.port=587
        spring.mail.username=YOUR_GMAIL_USERNAME
        spring.mail.password=YOUR_APP_PASSWORD 
        spring.mail.properties.mail.smtp.auth=true
        spring.mail.properties.mail.smtp.starttls.enable=true
        ```

3.  **Build and Run:**
    ```bash
    # Build the Spring Boot application
    mvn clean install
    
    # Run the application
    java -jar target/campus-event-portal-*.jar
    ```

The application will start on `http://localhost:8080`.

## 🤝 Contribution

Contributions are welcome! If you have suggestions for improving the code, features, or documentation, please fork the repository and submit a pull request.

## 🔮 Future Enhancements

* Integration of **Push Notifications** via a mobile application.
* Implementation of an **AI-powered Event Recommendation System** based on student activity and profile.
* Addition of **Analytics Dashboards** for administrators to track event participation and communication effectiveness.
* Support for **multilingual** content delivery.

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
