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
Client:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
Server:
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
Client:

<img width="882" height="268" alt="3b client" src="https://github.com/user-attachments/assets/4412743e-ed10-42d2-ad6c-4a93f7e25f22" />

Server:

<img width="949" height="268" alt="3b server" src="https://github.com/user-attachments/assets/c3e77141-99b7-4bb8-b427-28d00525a81c" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
