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
spring.datasource.url=jdbc:mysql://localhost:3306/WMS
spring.datasource.username=root
spring.datasource.password=
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.hibernate.ddl-auto=update

## Data Model
Core Entities
Person (MappedSuperclass)

Base class for all person entities
Fields: email, gender, name, phone
Workshop

Represents a workshop event
Fields: id, name, description, start_date, end_date
Session

Represents individual sessions within workshops
Fields: id, name, description, date, time, workshop_id
Relationships: Many-to-Many with presenters, undergraduates, and postgraduates
Presenter

Extends Person
Fields: id, affiliation, country, job_title
Relationships: Many-to-Many with sessions
Undergraduate

Extends Person
Fields: id, degree, university
Relationships: Many-to-Many with sessions
Postgraduate

Extends Person
Fields: id, institute, research_interest, second_degree
Relationships: Many-to-Many with sessions

## Setup Instructions
Prerequisites
Java 17+ (or appropriate version)
MySQL Server
Maven or Gradle
