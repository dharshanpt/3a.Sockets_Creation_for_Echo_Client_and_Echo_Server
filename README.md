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
## SERVER:
```
import socket
s = socket.socket()
s.bind(('localhost',8001))
s.listen(5)
c,addr = s.accept()
while True:
    ClientMessage = c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## CLIENT:
```
import socket
s = socket.socket()
s.connect(('localhost',8001))
while True:
    msg=input("client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## OUPUT
<img width="1120" height="478" alt="Screenshot 2025-10-28 091315" src="https://github.com/user-attachments/assets/e4ecc4c4-5588-4be5-b7a6-26d5852ac892" />

<img width="1403" height="481" alt="Screenshot 2025-10-28 091309" src="https://github.com/user-attachments/assets/9d6447ee-9d55-46e1-9dcf-c713f9fcc012" />
## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
