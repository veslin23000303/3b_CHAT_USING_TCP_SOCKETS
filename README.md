# 3b.CREATION FOR CHAT USING TCP SOCKETS
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
![image](https://github.com/Purajiths/3b_CHAT_USING_TCP_SOCKETS/assets/145548193/231f1c49-187a-4062-8c8d-a9110664b2cd)

## Server:
![WhatsApp Image 2024-05-10 at 11 07 52_6a81515a](https://github.com/Purajiths/3b_CHAT_USING_TCP_SOCKETS/assets/145548193/2409a8eb-a683-4791-bce3-b16d9456cabb)



## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
