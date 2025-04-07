# Biometric Fingerprint Login System

A Java desktop application that uses biometric fingerprint verification to authenticate users. The system integrates the **Mantra MFS100** fingerprint scanner to provide secure and seamless login functionality via a graphical user interface (GUI) built with **Java Swing**.

---

## Features

- Fingerprint-based login using MFS100 biometric scanner
- Java Swing-based login interface
- User authentication with fingerprint matching
- Integration with **MySQL** database for user data management
- Realtime fingerprint capture and verification using **MFS100 SDK**

---

## Tech Stack

- **Java**
- **Java Swing** – for GUI development
- **MySQL** – for user data storage and authentication
- **Eclipse IDE** – for development and debugging
- **MFS100 SDK** – to interact with the Mantra fingerprint scanner

---

## UI Preview

![image](https://github.com/user-attachments/assets/05b29626-c60c-4a49-9866-af864d7b8fb0)


---

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/biometric-fingerprint-login.git
```

### 2. Setup MySQL Database
- Create a database named `biometric_login`
- Create a `users` table with the following schema:
```sql
CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(50) NOT NULL,
  fingerprint_template BLOB NOT NULL
);
```

- Insert at least one user with fingerprint template registered through the scanner.

### 3. Install MFS100 Driver and SDK
- Download and install the **Mantra MFS100 RD Service** and SDK from the [official website](https://www.mantratec.com/Download).
- Add the required JAR files (`MFS100.jar`) and native libraries (`dll` files) from the SDK to your Eclipse project's build path.

### 4. Configure and Run the Project
- Open the project in **Eclipse IDE**
- Ensure JDBC connector (`mysql-connector-java.jar`) is added to the build path
- Update database connection credentials in the code (`DBConnection.java` or similar)
- Run `Main.java` to launch the login UI

---

## How It Works

1. User opens the application and sees a login screen.
2. User enters their username.
3. Fingerprint is captured using the **MFS100 scanner**.
4. The fingerprint is matched against the stored template in the database.
5. On successful match, user is granted access.

---
## Acknowledgments

- [Mantra Softech](https://www.mantratec.com) for providing the MFS100 SDK
- Java Swing community for UI design inspiration


---
