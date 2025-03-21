# Prerequisites
#######
- JDK 11 
- Maven 3 
- MySQL 8

# Technologies 
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- Tomcat
- MySQL
- Memcached
- Rabbitmq
- ElasticSearch
# Database
Here,we used Mysql DB 
sql dump file:
- /src/main/resources/db_backup.sql
- db_backup.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < db_backup.sql

# 🌐 Virtual Profile - AWS Deployment Project

This project demonstrates how to deploy a **Virtual Profile** web application using various AWS services for a secure, scalable, and production-ready environment.
![img alt]()

---

## 🚀 Project Overview

The **Virtual Profile** is a web application deployed on AWS using a full-stack setup with RDS, ElasticCache, Amazon MQ, and Elastic Beanstalk. It includes:

- Backend: Java (Maven) packaged as a `.war` file
- Deployment: AWS Elastic Beanstalk with auto-scaling
- CDN: AWS CloudFront
- Domain: Integrated with GoDaddy + SSL

---

## 🛠️ Setup and Deployment

### 1. 🔐 Security Group & Key Pair

Created a **dedicated Security Group** and **Key Pair** to allow secure access between services like RDS, ElasticCache, MQ, and Beanstalk.

---

### 2. 🗃️ RDS (Relational Database Service)

- Used **Amazon RDS with SQL** to manage account-related data.
- Configured access within the same Security Group.

---

### 3. ⚡ ElasticCache (Memcached)

- Integrated **ElasticCache (Memcached)** to optimize performance and reduce database load.

---

### 4. 📩 Amazon MQ

- Configured **Amazon MQ** as a managed message broker to handle asynchronous communication within the app.

---

### 5. ☁️ AWS Elastic Beanstalk Deployment

- Initialized the project locally and built it using **Maven**:
  ```bash
  mvn clean package
  ```
- Clone the Project and run it using maven to get the target.war file and deploy it into beanstalk to get the web app running.


### 6. ☁️ Using Multiple Instances of VM's for each Service if you don't want to use Beanstalk.
![img alt]()




