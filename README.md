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

Developed by : **Yuuvasri R**<br>
Reg No : **212225230313**

### Client
```python
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
```
### Server
```python
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    print(s.recv(1024).decode()) 
    s.send("Acknowledgement Recived".encode())```
## OUTPUT
<img width="1104" height="958" alt="Screenshot 2026-05-19 144922" src="https://github.com/user-attachments/assets/13078681-09ab-4857-bf8f-009433ca6010" />
<img width="1110" height="966" alt="Screenshot 2026-05-19 144932" src="https://github.com/user-attachments/assets/e71d7bcb-f9ee-4c8f-a3af-7af60bf69066" />
## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.

















































.














































.






































.
