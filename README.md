<h1 align = "center"> SPRINGBOOT VALIDATION (USER MANAGEMENT) </h1>

<p align="center">
<a href="Java url">
    <img alt="Java" src="https://img.shields.io/badge/Java->=8-darkblue.svg" />
</a>
<a href="Maven url" >
    <img alt="Maven" src="https://img.shields.io/badge/maven-3.0.5-brightgreen.svg" />
</a>
<a href="Spring Boot url" >
    <img alt="Spring Boot" src="https://img.shields.io/badge/Spring Boot-3.0.6-brightgreen.svg" />
</a>
  
<!-- <a >
    <img alt="MySQL" src="https://img.shields.io/badge/MySQL-blue.svg">
</a> -->
</p>
   
This project is a basic web application that allows Users  manage User details. Users can do basic CRUD operation on List .  

---
<br>

## Framework Used
* Spring Boot

---
<br>

## Dependencies
The following dependencies are required to run the project:

* Spring Boot Dev Tools
* Spring Web
* Spring Data JPA
* Lombok
* Validation
* H2 database


<!-- <br>

## Database Configuration
To connect to a MySQL database, update the application.properties file with the appropriate database URL, username, and password. The following properties need to be updated:
```
spring.datasource.driverClassName=com.mysql.cj.jdbc.Driver
spring.datasource.url = jdbc:mysql://localhost:3306/<DatabaseName>
spring.datasource.username = <userName>
spring.datasource.password = <password>
spring.jpa.show-sql = true
spring.jpa.hibernate.ddl-auto = update

spring.jpa.properties.hibernate.show_sql=true
spring.jpa.properties.hibernate.use_sql_comments=true
spring.jpa.properties.hibernate.format_sql=true

```
<br> -->

## Language Used
* Java

---
<br>

## Data Model

The Job data model is defined in the Job class, which has the following attributes:
<br>

* User Model
```
   	@Id
	@GeneratedValue(strategy = GenerationType.AUTO)
private String userId;

	@NotEmpty
private String userName;

@DateTimeFormat
private String dateofBirth;

@Email
private String email;

@NotEmpty
@Pattern(regexp="(^$|[0-9]{10})")
private String phoneNumber;

@DateTimeFormat(iso = DateTimeFormat.ISO.DATE)
@JsonFormat(pattern = "MM/dd/yyyy")
private String date;

@DateTimeFormat(iso = ISO.TIME)
@JsonFormat(pattern = "HH-MM-SS")
private String time;
```

<!-- ```
* Stack Type
    FMCG,
    IT,
    HEALTH
``` -->

<!-- * AppointmentKey Model
```
appId = Long
LocalDateTime : Timestamp
```

* Authentication Token 
```
tokenId : Long
token : string
tokenCreationDate : LocalDate
@OneToOne 
Patient : patient
```
* Doctor  Model
```
doctorId : Long
doctorName : string
 @Enumerated(EnumType.STRING)
Specialization : specialization
@OneToMany(mappedBy = "doctor")
List<Appointment> : appointments
```
* Patient Model 
```
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long patientId;
    private String patientFirstName;
    private String patientLastName;
    @Column(nullable = false, unique = true)
    private String patientEmail;
    @Column(nullable = false)
    private String patientPassword;
    private String patientContact;
```
* Specialization 
```
    ENT,
    ORTHO,
    GYNO,
    NEURO,
    DERMO
``` -->
## Data Flow

1. The Users at client side sends a request to the application through the API endpoints.
2. The API receives the request and sends it to the appropriate controller method.
3. The controller method makes a call to the method in service class.
4. The method in service class builds logic and retrieves or modifies data from the database, which is in turn given to controller class
5. The controller method returns a response to the API.
6. The API sends the response back to the User.

---

<br>


## API End Points 

The following endpoints are available in the API:

* Stock Controller:
```
GET /Allusers:   fetch all users List   
POST /adduser : create a new User accout
GET/getUser/{id}": return User based on user Id 

PUT/udateUserInfo : update the User with sutable Id
DELETE/delateUser/{id} : delete the User which is matching with Id 
```

<!-- * Todo Controller
```
GET /get-todo:returns the all  Todo`s
POST/creat-todo : add Todo to user Todo list
PUT/Update-todo : It updates the excisting todo otherwise create new Todo
GET/get/{id} : get todo by its id; -->

<!-- ```
 * Patient Controller:
```
POST /patient/signup:patient a new Doctor accout    
POST /patient/signin: the excisting patient login in to is accouct
GET /doctor: Return available Doctor`s  Appointments
DELETE/appointment : Delete patient Appointment
```  -->
<br>

## DataBase Used
* H2 database
```
We have used Persistent database to implement CRUD Operations.
```
---
<br>

## Project Summary

This project is a basic web application that allows Users  manage their daily Stocks . Users can do basic CRUD operation on Stocks  . 



## Author

👤 **Ashok Yelagandula**

* GitHub: [AshokYelagandula](https://github.com/ashok0706)

<!-- * LinkedIn: [Ajinkya Padule](https://www.linkedin.com/in/ajinkya-padule-04b8541a6/) -->
    
---

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page]("url").
    
---
    
## Show your support

Give a ⭐️ if this project helped you!
    
---
    
<!-- ## 📝 License

Copyright © 2023 [Ajinkya Padule](https://github.com/AjinkyaPersonal).<br />

This project is [MIT]("url") licensed. -->
    
---
