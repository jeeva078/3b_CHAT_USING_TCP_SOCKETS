# EX:3b CREATION FOR CHAT USING TCP SOCKETS
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

![cn 3b -1](https://github.com/jeeva078/3b_CHAT_USING_TCP_SOCKETS/assets/147048597/2df7b0d4-a5a9-4da7-a588-6a743ba2a476)

### SERVER

![cn 3b -2](https://github.com/jeeva078/3b_CHAT_USING_TCP_SOCKETS/assets/147048597/411e24fc-be4b-454c-8ff7-a5b3db6eec79)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
