# 3b.CREATION FOR CHAT USING TCP SOCKETS
## NAME:VESLIN ANISH A
## REGISTER NO:212223240175
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## Client:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## Server:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUPUT
## Client:
![Screenshot 2024-05-15 102353](https://github.com/veslin23000303/3b_CHAT_USING_TCP_SOCKETS/assets/151148539/478ed14d-d0f9-45c1-aeb8-dcb642c853bc)


## Server:

![Screenshot 2024-05-15 102407](https://github.com/veslin23000303/3b_CHAT_USING_TCP_SOCKETS/assets/151148539/1a837a7f-fbee-4477-9bf8-5e98e4b89718)




## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
