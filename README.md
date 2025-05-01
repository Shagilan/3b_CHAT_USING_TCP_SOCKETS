# 3b.CREATION FOR CHAT USING TCP SOCKETS
# NAME:SHAGILAN U
# REG.NO:212224040303
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
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```

## OUPUT

![image](https://github.com/user-attachments/assets/925dfa49-c1d0-4a41-9f6c-308e4a48747c)
![image](https://github.com/user-attachments/assets/47260e8b-1f2b-4130-b2a3-f84182b3e481)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
