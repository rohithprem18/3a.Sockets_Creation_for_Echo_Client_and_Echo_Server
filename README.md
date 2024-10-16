# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
### Name: ROHITH PREM S
### Register Number: 212223040172
## AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
### Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())

```
### Server:
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
## OUPUT:
### Client:
![exp 3a client](https://github.com/user-attachments/assets/e56a6904-39cb-490f-a0b0-9da604a67878)

### Server:
![exp 3a server](https://github.com/user-attachments/assets/160691df-7b53-4d93-ae66-4736a07fd9b0)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
