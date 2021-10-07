# About
A basic command line file transfer program built using the Python sockets library.

A client and a server application which allows a client to download a file of
it's choosing from the server. The client and the server communicate through stream(TCP) sockets, exchanging both control and actual file data.

# Usage

### Server 
Usage: python server.py listen_port

Arguments:
* listen_port - Port for the server to recieve connections on (between 1024 and 64000, inclusive)

Upon running the server, it will continuously serve clients, until shut down.

### Client
Usage: python client.py server_ip server_port target_file

Arguments:
* server_ip - Address of the server, either the hostname or IP address (e.g. 192.168.1.1 or fileserver.example.com)
* server_port - Port that the server is recieving connections on (between 1024 and 64000, inclusive)
* target_file - Name of the file to download from the server

The client will only request and download the target file, then will exit.

# Packet Formats
The client and server operates on a defined request/response format, listed below.

### FileRequest
![File Request Format](https://i.postimg.cc/nrBvLcmZ/image.png "File Request Format")

### FileResponse
![File Response Format](https://i.postimg.cc/Bb7GX4fY/image.png "File Response Format")