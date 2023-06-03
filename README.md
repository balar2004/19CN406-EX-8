# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER
# AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
# ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server, it will send ACK signal to client otherwise it will
send NACKsignal to client.
6. Stop the program
# PROGRAM:
# CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
 ```
# SERVER:
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
# OUTPUT:
# CLIENT SIDE:
![Client-5](https://github.com/balar2004/19CN406-EX-8/assets/118791778/268a192e-4da2-432d-89d6-9e4b97e51a05)
# SERVER SIDE:
![Server-5](https://github.com/balar2004/19CN406-EX-8/assets/118791778/b1eb1c19-5a8b-4750-a768-2ad640c1e1d5)
# RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
