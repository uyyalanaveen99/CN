import socket as s
import time as t
def server():
    host = s.gethostname()
    port = 1234
    socket_server = s.socket()
    socket_server.bind((host,port))
    socket_server.listen(2)
    connec,adress = socket_server.accept()
    print("Connection from" + str(adress))
    c = 1
    while True:
        
        data = connec.recv(1024).decode()
        if not data:
            break
        if c%4 == 0:
            c+=1
            t.sleep(2)
            data = "Not Recieved"
            connec.send(data.encode())
            continue
        print("Recieved Data: "+str(data))
        data = "Data Recieved : " +str(data)
        connec.send(data.encode())
        c+=1
    connec.close()

server()
            
