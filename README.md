# CLOUD-DATA-STORAGE-SERVER

### NAME: Nishanth R S
### REG NO: 212224040223

## Aim

To create and configure an Amazon Relational Database Service (Amazon RDS) instance as a cloud data storage server, configure the required security settings, connect it to a web application, and perform database operations using the application.

## Algorithm / Steps

1. Create a Security Group for the RDS database.
2. Add an inbound rule to allow MySQL (Port 3306) access from the Web Security Group.
3. Create a DB Subnet Group using two Availability Zones.
4. Launch an Amazon RDS MySQL database instance.
5. Configure the database with the required identifier, username, password, storage, and instance class.
6. Associate the database with the created Security Group and Subnet Group.
7. Wait until the database status becomes **Available**.
8. Copy the RDS endpoint.
9. Open the web application using the provided Web Server IP address.
10. Enter the RDS endpoint, database name, username, and password.
11. Connect the application to the database.
12. Verify the connection by adding, editing, and deleting records in the Address Book application.


## Program

### Security Group Configuration

* Security Group Name: **DB Security Group**
* Inbound Rule: **MySQL/Aurora (3306)**
* Source: **Web Security Group**

### DB Subnet Group

* Name: **DB-Subnet-Group**
* VPC: **Lab VPC**

### Amazon RDS Configuration

* Engine: **MySQL**
* Template: **Dev/Test**
* Availability: **Multi-AZ**
* DB Instance Identifier: **lab-db**
* Username: **main**
* Password: **lab-password**
* Instance Class: **db.t3.micro**
* Storage: **20 GB (General Purpose SSD)**

### Connect the Application

```text
Endpoint : <RDS Endpoint>
Database : lab
Username : main
Password : lab-password
```

After submitting the above details, perform Add, Edit, and Delete operations on the Address Book application.

## Output
<img width="1024" height="694" alt="image" src="https://github.com/user-attachments/assets/065fc32c-134e-4041-a86f-8d621a96bd8d" />

<img width="1024" height="701" alt="image" src="https://github.com/user-attachments/assets/4e43d6da-219c-437c-9483-22b39ac5e0fb" />
<img width="1513" height="1039" alt="image" src="https://github.com/user-attachments/assets/b60f53ce-b111-412d-9d2a-aaf6bfd5a2b8" />

<img width="1552" height="681" alt="image" src="https://github.com/user-attachments/assets/47eb6e28-d7bb-4759-b5d1-6c1ef5b4dea3" />
<img width="1907" height="904" alt="image" src="https://github.com/user-attachments/assets/f00996c3-9f16-4f0b-9656-b2a9d5a3a4fb" />

## Result

Thus, an Amazon RDS database instance was successfully created and configured as a cloud data storage server. The database was securely connected to a web application, and data operations such as inserting, updating, and deleting records were successfully performed through the application.

