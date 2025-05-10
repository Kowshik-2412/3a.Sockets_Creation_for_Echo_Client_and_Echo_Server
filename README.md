# NAME:Kowshik P
# REGISTER NO:212224040164

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
# CLIENT.PY:
```
import socket
server = socket.socket()
server.bind(('localhost', 8000))
server.listen(1)

print("Server is ready and waiting...")
client, address = server.accept()
print("Connected to:", address)

while True:
    message = client.recv(1024).decode()
    if not message:
        break
    print("Client:", message)
    client.send(message.encode())

client.close()
server.close()
print("Server stopped.")
```
# SERVER.PY:
```
import socket
server = socket.socket()
server.bind(('localhost', 8000))
server.listen(1)

print("Server is ready and waiting...")
client, address = server.accept()
print("Connected to:", address)

while True:
    message = client.recv(1024).decode()
    if not message:
        break
    print("Client:", message)
    client.send(message.encode())

client.close()
server.close()
print("Server stopped.")
```
## OUPUT:
![image](https://github.com/user-attachments/assets/ff00414b-886b-4d75-98d2-77ba830582bf)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
