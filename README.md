# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## NAME: PRAJAN P
## REGNO: 212223240121
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

SERVER:
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
CLIENT:

![376909294-d2e03042-6d6b-4fd3-ac08-a916046f5492](https://github.com/user-attachments/assets/1d22a1b9-f9c0-49e6-a81b-e6e6e38974ea)

SERVER:

![376909307-e6aa2220-dace-45c6-ba72-8d083afa7514](https://github.com/user-attachments/assets/a322c642-23ec-4c66-915b-b740e1aebc45)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
