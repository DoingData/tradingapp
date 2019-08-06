# Introduction
The Trading App is online stock trading simulation REST API. Application have features as 
Account creation and make money deposit and withdrawl allows user to purchase and sell stock.
 The app can be used as back end REST API for front end or app development.<br />
 This app is implemented with java spring and springboot. Data is stored in postgreSQL 
 database and the information about the stock is realtime fetched from **IEXcloud.**

## Quick Start

### Prerequisities 
- Docker
- Java 8
- IEX token to access market data  <br />```(https://iexcloud.io/docs/api/)```  
- PostgreSQL
- Maven

### Runing the app
- Clone git respository <br/> ```https:github.com/UsmanAsifJrvs/trading-app```

- Start the app using bash with four arguments <br/>
    ```bash run```
  
### Architecture
App is developed with multiple layers and diiferent components each layer
 have a specific functionality
- Controller
- DAO
- Service
- PSQL
- IEX
- SpringBoot

#### Controller
Job of controllers is to handle requests and map them to desired service methods, and 
then collect the response provided by service layer.

#### Service
All the business logic happens in service layer. Controller layer send requests to
 methods in this layer to access the business logic which access and process data
 and return back to controller layer.
 #### DAO
 The Data Access Object layer performs **CRUD** Operations using DML,DCL and TCL on 
 postgreSQL database and also access data from IEX cloud. It also recieve requests 
 from service layer performs the operations and sends the results back.
 
#### SpringBoot
Spring Framework is used to create components and for dependency injection.
 IoC is used where objects define their dependencies. It has embeded Apache tomcat server
 which makes easy to run web applications.
 #### postgreSQL
 postgreSQL is database of choice to store data which is being used in this application
 init.sql provides the setup for database creation and schema.sql provides the schema
 of database in psql.
 #### IEX
 IEX cloud Api  is used to get almost realtime data from stock market and only required 
 tickers are used fro whole data stream.
## Improvements
- Current Implementation allows traders to have only one account, Authorization for multiple
accounts can be added in future implementations.
- More information from IEX ticker can be used to provide to customer
- more secure and multilevel authentication should be implemented for user access
- login access with google or facebook user id's can be implemented. 
- Email or SMS alert notifications can be implemented for voltality of users favourite 
stocks 
