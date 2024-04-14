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
## client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## server:
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
## client:
![Screenshot 2024-04-14 213808](https://github.com/praveen2p/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/151658061/aa809094-bd55-4e6e-9f43-f4b5c03ee30b)

## server:
![Screenshot 2024-04-14 213819](https://github.com/praveen2p/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/151658061/232b0858-ba7b-402c-bc23-82919d43c126)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
