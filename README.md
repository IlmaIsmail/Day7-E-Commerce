# Day7-E-Commerce

# University Workshop Management System
A Spring Boot application for managing university workshops, sessions, and participants.

## Overview
The University Workshop Management System (WMS) is designed to facilitate the organization and management of academic workshops. It allows tracking of:

    Workshops and their details
    Workshop sessions
    Presenters
    Undergraduate participants
    Postgraduate participants

## Technical Stack
    Framework: Spring Boot
    Database: MySQL
    ORM: Hibernate/JPA
    Language: Java

## Database Configuration
The application connects to a MySQL database with the following configuration:

    spring.application.name=University
    spring.datasource.url=jdbc:mysql://localhost:3307/university
    spring.datasource.username=root
    spring.datasource.password=
    spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
    spring.jpa.hibernate.ddl-auto=update

## Data Model
### Core Entities
1. Person (MappedSuperclass)

       Base class for all person entities
       Fields: email, gender, name, phone
   
3. Workshop
   
        Represents a workshop event
        Fields: id, name, description, start_date, end_date
   
5. Session
   
        Represents individual sessions within workshops
        Fields: id, name, description, date, time, workshop_id
        Relationships: Many-to-Many with presenters, undergraduates, and postgraduates
   
7. Presenter

        Extends Person
        Fields: id, affiliation, country, job_title
        Relationships: Many-to-Many with sessions
   
9. Undergraduate

        Extends Person
        Fields: id, degree, university
        Relationships: Many-to-Many with sessions
   
11. Postgraduate

        Extends Person
        Fields: id, institute, research_interest, second_degree
        Relationships: Many-to-Many with sessions

## Setup Instructions
    Prerequisites
    Java 17+ (or appropriate version)
    MySQL Server
    Maven or Gradle

## Outputs

![Screenshot (87)](https://github.com/user-attachments/assets/27fa7336-5180-46ef-a239-da2465aefda8)

![Screenshot (88)](https://github.com/user-attachments/assets/a553ed2f-8449-487f-8104-af7bcef1e3f9)


![Screenshot (89)](https://github.com/user-attachments/assets/34411e6a-89c2-4e57-b8e8-62b6f6f6c2da)
-994f-a378dbd45e22)

![Screenshot (90)](https://github.com/user-attachments/assets/362ca84e-159f-49ed-a9af-50baebe256f7)
