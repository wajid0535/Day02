# Day02
HTTP1.1 VS HTTP2.0,OBJECTS.
Difference between HTTP/2 and HTTP/1.1:
HTTP stands for hypertext transfer protocol & it is used in client-server communication. By using HTTP user sends the request to the server & the server sends the response to the user. There are several stages of development of HTTP but we will focus mainly on HTTP/1.1 which was created in 1997 & the new one is HTTP/2 which was created in 2015.
HTTP/1.1: For better understanding, let’s assume the situation when you make a request to the server for the guvi.html page & server responds to you as a resource guvi.html page. before sending the request and the response there is a TCP connection established between client & server. again you make a request to the server for image img.jpg & the server gives a response as an image img.jpg. the connection was not lost here after the first request because we add a keep-alive header which is the part of the request so there is an open connection between the server & client. there is a persistent connection which means several requests & responses are merged in a single connection. These are the drawbacks that lead to the creation of HTTP/2: The first problem is HTTP/1.1 transfer all the requests & responses in the plain text message form. The second one is head of line blocking in which TCP connection is blocked all other requests until the response does not receive. all the information related to the header file is repeated in every request.
HTTP/2: HTTP/2 was developed over the SPDY protocol. HTTP/2 works on the binary framing layer instead of textual that converts all the messages in binary format. it works on fully multiplexed that is one TCP connection is used for multiple requests. HTTP/2 uses HPACK which is used to split data from header. it compresses the header. The server sends all the other files like CSS & JS without the request of the client using the PUSH frame.
Difference between HTTP/1.1 and HTTP/2 are:
HTTP/1.1:
Ithe usest works on the textual format.	
There is head of line blocking that blocks all the requests behind it until it doesn’t get its all resources. 
It uses requests resource Inlining for use getting multiple pages.
It compresses data by itself.
HTTP/2.0:
It works on the binary protocol.
It allows multiplexing so one TCP connection is required for multiple requests.
It uses PUSH frame by server that collects all multiple pages 
It uses HPACK for data compression.



Objects and its internal representation in Javascript:


Objects are important data types in javascript. Objects are different than primitive datatypes (i.e. number, string, boolean, etc.). Primitive data types contain one value but Objects can hold many values in form of Key: value pair. These keys can be variables or functions and are called properties and methods, respectively, in the context of an object.

Every object has some property associated with some value. These values can be accessed using these properties associated with them.

var myCar = new Object();

myCar.make = 'Suzuki';

myCar.model = 'Altros';

myCar.year = 1978;

myCar.wheels = 2;

After creating myCar object, the value inside the object can be accessed using keys.
i.e.

myCar.year

Output: 1978

These values can be accessed using brackets notation also.

myCar.year

Output: 1978.
