# FTP Server Documentation
## Introduction
This documentation provides an overview and explanation of the FTP (File Transfer Protocol) server developed using socket programming and OS fundamentals. The server allows users to perform basic file operations such as listing files in the current directory, downloading files (RETR), uploading files (STOR), and changing directories (CD).
## Components
The FTP server consists of two main components:
Server: This component listens for incoming connections from clients, accepts connections, and handles client requests.
Client: The client component connects to the server and sends commands to perform various file operations.
## Features
- List Files (LIST): Allows users to list files in the current directory.
- Download File (RETR): Enables users to download a file from the server to the client's local machine.
- Upload File (STOR): Permits users to upload a file from the client's local machine to the server.
- Change Directory (CD): Allows users to navigate through directories on the server.
## Server Implementation (server.py)
## Libraries Used
- socket: For creating and managing sockets.
- threading: For handling multiple client connections concurrently.
- os: For interacting with the operating system (e.g., file operations, directory navigation).
## Functionality
- The server listens on port 3000 for incoming connections.
- Upon connection, the server sends a welcome message to the client.
- It continuously listens for commands from the client.
- It handles various commands such as LIST, RETR, STOR, and CD.
- Error handling is implemented to manage exceptions gracefully.
- Threading is used to handle multiple client connections simultaneously.
## Client Implementation (client.py)
## Libraries Used
- socket: For creating and managing sockets.
- os: For interacting with the operating system (e.g., checking file existence).
## Functionality
- The client connects to the server at the specified IP address and port.
- It displays the welcome message received from the server upon connection.
- It prompts the user to enter commands (LIST, RETR, STOR, CD).
- For RETR and STOR commands, it prompts the user to enter the filename.
- Error handling is implemented to manage exceptions gracefully.
- The client performs the requested operation and displays appropriate messages.
- It closes the connection when the user exits the client.
## Usage
- Starting the Server: Run server.py to start the FTP server. It will start listening on port 3000.
- Connecting with the Client: Run client.py to connect with the server. Enter the server's IP address and port.
- Sending Commands: Enter commands (LIST, RETR, STOR, CD) to perform file operations.
- Exiting the Client: Enter quit or exit to close the client.
## Conclusion
This FTP server implementation provides a simple yet functional file transfer mechanism using socket programming and OS fundamentals. It allows users to interact with the server to perform basic file operations efficiently. With proper error handling and multi-threading, it ensures robustness and scalability.

