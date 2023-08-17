# Building-Go-Web-Services-and-Applications
## Building a Web Service
- What are Web Services?
    - Clients
        - clients are the things that connect to the particular application.
        - Mobile devices, laptops, desktops
    - The web service is what sits behind the web app (front end).
    - The web service takes care of the heavy lifting for the web app.
    - It takes care of all the database calls and the processing of data to and from the DB then back to the web app.
    - Allows for a seperation of concerns because the front end isn't directly pulling from the DB.
    - Typically an API (application programming interface) which allows us to move information between the web app and the DB
    - RESTful Web Service
        - REST stands for Representational State Transfer.
        - It begins with the client. The client then sends requests, usually in a uniform interface, using JSON or XML to a sever using several different methods, the first of those methods being GET.
        - CRUD Operations
            - GET method would allow you to get information as the name implies.
            - POST method to put new information into a system.
            - PUT method to update information
            - DELETE method to delete information
        - All the above methods are HTTP methods. The RESTful web servise is built upon HTTP.
        - HTTP is handling the traffic, the request to and from the server, using the methods.
        - REST is being used as an architectural style to give us some guidance on how to design and build web services.
        - REST is stateless
        - A RESTful web service should not maintain any client-specific state on the server.
        - This means that all the information required to handle a request should be handled in the request itself rather than being stored on the server.
        - Responses from RESTful web services should be cacheable, meaning that they should be stored and reused by the clients to reduce the number of request to the server.
    - HTTP Requests & Responses
        - Three elements make up HTTP requests
            - Request line
                - Consists of several different things ex: ```GET /hello-world HTTP/1.1```
            - Headers
                - Key value pairs that are stored in the header of a request, and they provide additional information about th request, such as the content type and the client's IP address or the servers response time.
            - Body
                - It's the information that's being put with the request and sent to the server.
        - Request and responses are very similar, but they have some differences.
            - instead of a request line the response has a status line. And the status line consists of an HTTP version, a status code, and then a character return.
- Understanding the net/http Package