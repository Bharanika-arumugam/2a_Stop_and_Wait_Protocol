# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
Name:A.S.BHARANIKA

Reg no:212224040048
```
## Client

import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
   print(ack)
   continue
 else:
   c.close()
   break


## Server

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```


## OUTPUT
## Client
![Screenshot 2025-05-14 182800](https://github.com/user-attachments/assets/21a233fc-cfd5-4d4e-bf9e-0e4a251d1083)

## Server
![Screenshot 2025-05-14 182818](https://github.com/user-attachments/assets/55a87bad-693a-4373-a26f-da275fb6050a)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
