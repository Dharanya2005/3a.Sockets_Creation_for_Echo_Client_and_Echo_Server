# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
# client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
# sever:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
## OUTPUT
# client:
![Screenshot 2024-04-10 122754](https://github.com/Dharanya2005/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145742468/055c967a-6be2-4696-8302-fb03ab8553d1)
# server:
![Screenshot 2024-04-10 122804](https://github.com/Dharanya2005/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145742468/23809a11-583c-430f-8195-12d1524aeb28)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
