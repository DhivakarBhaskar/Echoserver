# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
```
# echo-server.py


import socket


HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)


with socket.socket(socket.AF_INE
T, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
```
```
# echo-client.py


import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello, world")
    data = s.recv(1024)


print(f"Received {data!r}")
```
## OUTPUT:
<img width="815" height="762" alt="image" src="https://github.com/user-attachments/assets/fe8040f8-4d9d-4aaf-9cbb-1b41ba6309db" />
<img width="805" height="441" alt="image" src="https://github.com/user-attachments/assets/ff2d1be3-e25c-4fe3-b29c-1175deb7052d" />
<img width="812" height="307" alt="image" src="https://github.com/user-attachments/assets/d55f0dc5-dc3f-4adc-a051-6be95ff14096" />



## RESULT:
The program is executed successfully
