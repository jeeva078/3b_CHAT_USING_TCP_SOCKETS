# EX:3b CREATION FOR CHAT USING TCP SOCKETS
## DATE:26.03.2024
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### CLIENT
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
### SERVER
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
### CLIENT

![3b 1](https://github.com/Divya110205/3b_CHAT_USING_TCP_SOCKETS/assets/119404855/17c7ce9c-b92e-4ad8-9a4d-84e04a0e6b59)

### SERVER

![3b 2](https://github.com/Divya110205/3b_CHAT_USING_TCP_SOCKETS/assets/119404855/b0f40891-b68f-4f44-ab1b-b827a7e670b2)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
