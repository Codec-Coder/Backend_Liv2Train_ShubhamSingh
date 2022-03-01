# Backend_Liv2Train_ShubhamSingh
Spring boot API with h2 database and JPA ORM .


I have Installed the Spring Tool Suite 4 fro eclipse from https://spring.io/tools#suite-three (Linux version).

For api testing I have used postman https://www.postman.com/downloads/

The project uses in memory H2 database along with JPA for Object Relational Mapping(ORM)
Project details.
  Routing is handled by resources package.
  Storing and retrieving of data is handled within service package.
  Interface for daabase operations is in dao package.
  The classes for data models are in centermodel package.
  Exceptions are handled within exceptions package.
  
Documentation for the APIs :
  **** for Registering a Center -> url http:localhost:8080/create
  
  sample JSON body
  {
  "centerName" :String value less than 41 characters(Required),
  "centerCode":String value 12 character (Required),
  "address":Object (Required){
      "address":String value for address,
      "city":String value for city,
      "state":String value for state,
      "pincode":String value 6 character
  },
   "studentCapacity":Integer,
   "coursesOffered":List of String,
   "contactEmail" :String value (Unique Email, Required),
   "contactPhone" :String value 12 character (Required)
  }
  
  **** for Retrieving Reistered Centers -> url http:localhost:8080/centers
  
  sample JSON body
  {
  "centerName" :String value less than 41 characters(Required),
  "centerCode":String value 12 character (Required),
  "address":Object (Required){
      "address":String value for address,
      "city":String value for city,
      "state":String value for state,
      "pincode":String value 6 character
  },
   "studentCapacity":Integer,
   "coursesOffered":List of String for courses Offered,
   "createdOn":String value for time,
   "contactEmail" :String value (Unique Email, Required),
   "contactPhone" :String value 12 character (Required)
  }
  
  **** Invalid error message 
  
  sample JSON body
  {
    "timestamp": String value representing current time,
    "status": Integer value for http status,
    "error": String value representing error,
    "message": String value representing error message
  }
