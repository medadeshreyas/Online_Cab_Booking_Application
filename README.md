<p align="center">
  <img src="https://user-images.githubusercontent.com/104069112/201516383-6939ff92-784d-4683-b623-ec20d7d7fad7.gif" width="160" alt="animated" />
</p>
          
 <p align="center">              
- Exotic Cab Service Pvt.Ltd-
  <p/>
  
 #  Online Cab Booking System
 
Introducing a cutting-edge project that I have recently developed - a RESTful API web service for an online cab booking platform. This project is designed to perform all the fundamental CRUD operations, along with user validation at every step. Whether you are a customer, driver, or administrator, this application has something for everyone.

Customers can register themselves with the application, and log in to get a valid session token. They can view the list of available cabs and book a trip, and only logged-in users can access their trip history, profile updates, and other features.

Drivers can log in to the application and update their information using their username and password. They can add and update their cab details and mark their availability according to the trip status. The driver can also end the trip, and the application generates a bill for the trip.

Admins have the administrator role of the entire application and can only be registered admins with a valid session token. They can add, update, and delete drivers or customers from the main database and access the details of different customers, drivers, and trip bookings.


## Features

- Authentication and validation for customers, drivers, and administrators is implemented through the use of session UUIDs.

**Administrator**

- The ability to act as the primary overseer of the entire application
- The capability to add, update, and delete drivers or customers from the main database
- Access to details pertaining to customers, drivers, and trip bookings

**Customer**

- The ability to register with the application and log in to receive a valid session token
- The capability to view a list of available cabs and book a trip
- The ability to access trip history, update profile information, and utilize other features, but only for logged-in users.

 **Driver**
 
- The ability to log in to the application and update personal information using a username and password
- The capability to add and update cab details
- The ability to mark availability status according to the status of trips
- The ability to end a trip and have the application generate a bill for the completed trip.


### Technical Stacks

- Spring Boot 
- Spring Framework
- Spring Data JPA 
- MySQL 
- Hibernate
- Java
- Swagger UI
- Postman


### Modules
-  Login Module
-	Admin Module
-	Customer Module
-	Driver Management Module
-	Cab Management Module
-	Booking Management Module


##   ER_Diagram                                            
![ER_Diagram](https://user-images.githubusercontent.com/104069112/201485913-289d5d89-fe19-4123-8852-6f0773aa9637.png)

### Installation & Run
- Before running the API server, you have to update the database configuration inside the application.properties file
- Update the port number, username and password as per your local database configuration
````
    server.port=8888

    spring.datasource.url=jdbc:mysql://localhost:3306/cabdb;
    spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
    spring.datasource.username=root
    spring.datasource.password=root
    
````
## API Root Endpoint

`https://localhost:8888/`

`http://localhost:8888/swagger-ui.html`


## API Module Endpoints

### Admin Module

* `POST /login` : Admin can login with username  and password provided at the time of registation
* `POST /insert/{key}` : Register a new admin with proper data validation and admin session
* `PUT /update/{key}` : Updates admin details
* `DELETE /delete/{id}` : Deletes the admin with passed id
* `GET /trips/{key}` : Get list of trips of all the trips
* `GET /tripsByCab/{type}` : Get list of trips by cab types
* `GET /tripsByDate/{date}` : Get list of trips by date
* `GET /tripsByCustomer/{id}` : Get list of all the customers trips by customer id
* `GET /tripsByCustomer/{id}/{date}` : Get list of all trips for the day by id and date


### Customer Module


* `POST /save` : Adding new customer
* `PUT /update` : Updates customer details 
* `DELETE /delete/{id}` : Deletes logged in user on the basis of id
* `GET /customer/{id}` : Getting customer on the basis of id
* `POST /validateCustome` : Checks valid coustomer


### Driver Module

* `POST /driver` : Register a new driver with proper data validation and admin session
* `PUT /driver` : Updates the driver details
* `DELETE /driver/{driverId}` : Deletes driver on the basis of id
* `GET /drivers` : Gets the best driver whose rating is over 4.5
* `GET /driver/{id}` : Get driver details by id
* `GET /listOfDrivers/{id}` : Gets list of all the drivers

### Cab Module

* `POST /cab` : Register a new cab 
* `PUT /cab` : Updates the cab details
* `DELETE /cab/{cId}` : Delete cab on the basis of cab id
* `GET /cabs/{carType}` : Gets the list of cabs on the basis of cab type
* `GET /countofcabs/{carType}` : Gets the total number of cabs on the basis of cab type

### Book a Trip


![Screenshot (793)](https://user-images.githubusercontent.com/104069112/201608930-22b7f222-9723-40a2-b3dc-c76b4a95e542.png)


#### This project is developed by team of 5 Back-End Developers during project week at Masai School
### Contributors

- [@Prateek Chauhan](https://github.com/PRA3EEK)
- [@Shreyas Vilas Medade](https://github.com/medadeshreyas)
- [@Ujjawal Prakash](https://github.com/ujjawalyt)
- [@Namdev Patil](https://github.com/namdevmanoharpatil)
- [@Sabira Farooq](https://github.com/Sab01123)
#### For any feedback, report, suggestions, you can contact with anyone of the team member
### THANK YOU
