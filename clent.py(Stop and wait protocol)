import socket as s
def client():
    host = s.gethostname()
    port = 1234
    client_socket = s.socket()
    client_socket.connect((host,port))
    n = int(input("enter the number of packets"))
    input_data = "enter packets of data"
    c =0
    while(c<n):
        data_packet = input(input_data)
        client_socket.send(data_packet.encode())
        acknowledgement = client_socket.recv(1024).decode()
        if(acknowledgement == "Not Received"):
            input_data = "Data Not received!! Resend "
        else:
            input_data = "Enter packets of data"
            print(acknowledgement)
            c+=1
    client_socket.close()
client()
