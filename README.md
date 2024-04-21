# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name : VINCY JOVITHA V
## Register Number : 212223230242

## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client:
```
import socket 
s=socket.socket() 
s.bind(('localhost',9000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    print("Client > ",ClientMessage) 
    msg=input("Server > ") 
    c.send(msg.encode())
```

### Server:
```
import socket 
s=socket.socket() 
s.connect(('localhost',9000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```

## OUTPUT
### Client:
![client3b](https://github.com/VincyJovitha01/3b_CHAT_USING_TCP_SOCKETS/assets/147121113/f039f6f3-4ff2-4d26-a9fc-da424fb7092f)

### Server:
![server3b](https://github.com/VincyJovitha01/3b_CHAT_USING_TCP_SOCKETS/assets/147121113/41183ff2-8543-4cf5-b959-d994acb4948d)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
