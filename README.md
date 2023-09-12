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
# CLIENT:
```python
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
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
# SERVER:
```python
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
#CLIENT OUTPUT:
![Screenshot 2023-08-29 161036](https://github.com/Darshans05/Echoserver/assets/115534676/2e5a5324-761a-47ee-b34c-a2afb46535f4)
#SERVER OUTPUT:
![SERVER](https://github.com/Darshans05/Echoserver/assets/115534676/a0c3419d-d16b-4db6-9b3f-61b6e124a7de)
## RESULT:
The program is executed successfully
