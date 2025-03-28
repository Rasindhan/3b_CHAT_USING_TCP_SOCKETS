![Screenshot 2025-03-16 162152](https://github.com/user-attachments/assets/d5779c7f-7190-49f6-a18f-37b016f257da)# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
```

CLIENT: 
 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())

 
SERVER: 
 
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
CLIENT: 
![Screenshot 2025-03-28 113529](https://github.com/user-attachments/assets/5f6af6bc-a06b-4496-a924-3d264183a619)

SERVER: 
![Screenshot 2025-03-28 113541](https://github.com/user-attachments/assets/357c689e-57f9-4489-b6e2-0df86b8fc024)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
