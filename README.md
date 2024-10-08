# Auction Project: Backend

# Overview 
**This is the backend for the Auction Project, built with Spring Boot and MySQL. It handles auction operations, including creating auctions, placing bids, managing product listings, and updating user balances in real-time, and also handles user authentication and authorization, ensuring secure access to the system.**

### Prerequisites
Before setting up and running the backend of the Football Project, ensure that the following software is installed on your system:

1. **Java Development Kit (JDK)**:
   
    - **version**: 1.8 or higher
    - **Installation**: [Download JDK](https://www.oracle.com/java/technologies/downloads/?er=221886)
      
2. **Maven**:

   - **Version**: 3.6.3 or higher (used for building and managing the Java project)
   - **Installation**: [Download Maven](https://maven.apache.org/download.cgi)

3. **MySQL**:
   
   - **Version**: 5.7 or higher
   - **Installation**: [Download MySQL](https://dev.mysql.com/downloads/installer)
   - **Setup**: Ensure you have a MySQL server running and create a database named 'auction'

4. **Git (optional, for cloning the repository)**:
   
   - **Installation**: [Download Git](https://git-scm.com/downloads)

6. **IDE (Integrated Development Environment)**:
   
   - **Recommended**: IntelliJ IDEA
   - **installation**: [Download IntelliJ IDEA](https://www.jetbrains.com/idea/download/?section=windows)

### Environment Variables

To run the application, you’ll need to set up the following environment variables:

1. **DB_URL**:
   - **Description**: The URL of the MySQL database
   - **Example**: DB_URL=jdbc:mysql://localhost:3306/auction

2. **DB_USERNAME**:
   - **Description**: The username for accessing the MySQL database
   - **Example**: DB_USERNAME=root

3. **DB_PASSWORD**:
   - **Description**: The password for accessing the MySQL database
   - **Example**: DB_PASSWORD=1234

4. **JAVA_HOME**:
   - **Description**: The path to the JDK installation
   - **Example**: JAVA_HOME=C:\Program Files\Java\jdk1.8.0_251

5. **MAVEN_HOME**:
   - **Description**: The path to the Maven installation
   - **Example**: MAVEN_HOME=C:\Program Files\Apache\maven

### Running the project

- Navigate to the project directory : cd /path/to/your/project

- Run the project using Maven:
   - mvn clean install
   - mvn spring-boot:run

## Features
- User registration and secure login.
- Automatic user balance initialization ($1000 for new users).
- Auction product management (upload, update and view).
- Real-time bidding system.
- Automatic winner determination after auction closure.
- Balance updates for both bidders and sellers after placing bids or closing Auctions.
- For every bid placed in an auction, $2 is deducted from the user's balance.
- The winner of the auction will have an additional 5% of the final bid amount deducted from their balance.
- A seller can close an auction only after a minimum of 3 bids have been placed.
- Admin panel for managing users and products.
