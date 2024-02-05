# TCP-chatroom
Project: TCP Chat Application in Python

Date: 10th September 2019
Category: Network Programming / Programming / Python Programming
Comments: 39 Comments

Description:
Implemented a TCP chat application using Python, leveraging its capabilities for efficient network programming. The application follows a client-server architecture, with one central server hosting the chat and multiple clients connecting to it.

Server Implementation:

Utilized the socket and threading libraries for network connections and multitasking.
Defined connection data, including the host IP address and a free port number (localhost:55555 in this example).
Created a server socket, bound it to the specified host and port, and set it to listen for incoming connections.
Maintained lists for connected clients and their nicknames.
Implemented a function to broadcast messages to all connected clients.
Implemented functions to handle messages from clients, remove and close clients, and manage the connection.
Established a continuous loop for accepting new connections, requesting and storing client nicknames, and initiating handling threads for each client.
Client Implementation:

Allowed users to choose a nickname before connecting to the server.
Established a connection to the server using the server's address and port.
Created two threads for receiving messages from the server and sending user messages to the server simultaneously.
The receiving thread constantly listened for messages, sending the user's nickname to the server when prompted ('NICK').
The writing thread waited for user input, combined it with the nickname, and sent it to the server.
Result:
Developed a fully-functioning TCP chat application enabling communication among multiple clients through a central server. The application can be extended with custom features such as chat rooms, commands, and roles.

Note:
Implemented encoding and decoding of messages as bytes (using ASCII) due to the inherent requirement of socket communication.
