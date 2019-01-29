## ~~1~~

~~Login button that forwards you to CI login to log in. Callback displays the institution or username you logged in with~~

~~Logging in for the first time captures user info into a database.~~

## 2

Can login via Microsoft.  

Callback page displays the number of times you've logged in.

Meta Database server set up (for authentication database, and RAC meta database, for example). Is accessible from within cadre server network.

Authentication database is set up, configured, and can be accessed from Login server and Data API server.

Data API running on a server. Accessable to outside. One "Status" endpoint that returns true if running.

Interface compiles and hosted on web server with "Hello World" type page. Includes Flask Microservice.

Version 1 of WoS & MAG on new server.  Accessible by all.



## 3

Can login via Google.

User Registration/profiles (post CI Login).

Logging in creates tokens that can be validated by APIs. Callback page returns the token created.

Data API accepts and validates authentication token.

Interface connects to authentication API to validate token and consume DataAPI status endpoint

First draft of 3rd version WoS/MAG Schema - Something ready to show RDC for feedback.

## 4

Can login via Facebook.

Login callback page forwards to the "internal" user interface if successfully logged in. Sends token with redirect. URL of interface should be configurable.

Data API can connect to a database. Status endpoint returns info on the database it's connected to.

Data API has a method for choosing which database the query will be run against (separate endpoints for each DB type?)

MAG Data available as relational database to Data API.

Benchmark existing WoS to new WoS.

Finalized version of 3rd version of schema.

## 5
Data API has endpoint that consumes GraphQL. Can return article data based on article ID.

Interface has a textbox that one can send a graphql request with an article ID to data api. Response is output in plain text.

XML parser can parse 1 xml file.

## 6
Interface can generate more complex queries.

Data API can handle more complex queries, including text search

Interface displays response in a visually appealing format.

XML parser can run on Carbonate.

## 7
RAC Database is set up, configured, and can be accessed from web server

Data API can save result sets to temporary storage, allowing async queries and method for checking status of async queries.

RAC Interface compiles and hosted on web server, including RAC REST API with status endpoint.

Interface allows checking status of async queries

## 8
Data API can insert data subsets into RAC database.

Interface can save queries to RAC database. Interface can load queries retrieved from RAC database.

RAC Interface retrieves list of available data subsets to current user.

Interface allows retrieval of data subsets

## 9
Data API can use RAC saved data subset in addition to main datasets.

Interface offers option to run queries using data subsets instead of main databases

---

##  Other tasks

8.  Data API can combine results from multiple data sets (e.g. WoS and MAG)
9.  Data API can create citation networks.

2)  WoS Data available as relational database to Data API.
3)  PTO Data available as relational database to Data API.
4)  MAG Data available as Graph Database.
5)  WoS Data available as Graph Database.
6)  PTO Data availabe as Graph database.
7)  Spark/Twister2 Cluster available. All nodes can talk to each other. Full data NOT available.
8)  Data sets available on Cluster.
