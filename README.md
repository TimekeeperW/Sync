# Sync
objects synchronization service
This design is mainly Server and Client. Server uses multiple threads, each time receiving a request, a new thread is created to process the request. The newProtocol is used to process the request data and write to postgreSQL, then return.

# Server
The server listens to the port 9003 of this machine. When a new request is received, a new thread is created to process the request.

[server](http://)

# Client
[client1](http://)
[client2](http://)
When the client connects to the server for the first time, the server will return obja information. The client can then enter the 

> obja=Hello

information in the console, set the value of obja in the server, and return.

And you can use multiple clients to connect to the server at the same time.

# Protocol
Protocol is used to process input data, and because it is a multi-threaded environment, Protocol uses a synchronization lock.

At the same time Protocol will store the processed data in postgreSQL.
[progre](http://)
