# ChatHu P2P Chatting System

ChatHu is a peer-to-peer (P2P) chat application that leverages a central server for user management while providing direct communication channels between clients. The system is designed with a focus on asynchronous operation, non-blocking I/O, and thread safety, ensuring a robust and efficient user experience.

## Architecture Overview

The ChatHu system comprises two primary components:

- **Server**: Acts as the central node for user registration, authentication, and peer discovery.
- **Client**: Provides a user interface for message exchange and implements direct peer-to-peer communication.

## Server

The server component of ChatHu is engineered for concurrent client handling, with a breakdown into several modules:

- **Server Main**: Listens for incoming client connections and spawns new threads for individual client handling.
- **ClientHandler**: Manages client requests, processes commands, and maintains communication with the connected client.
- **ClientData**: Stores client-related information such as username, IP address, port, and a history of executed commands.
- **ClientMap**: A thread-safe collection that maps usernames to their corresponding ClientData objects for quick lookups.

## Client

The client-side of ChatHu is designed with an asynchronous architecture, allowing for a responsive user interface that can handle incoming communication without blocking user interaction.

### Key Features:

- **Asynchronous Communication**: Ensures the UI remains responsive while handling networking operations.
- **Peer Discovery**: Clients can request a list of online users from the server for initiating direct P2P communication.
- **Direct P2P Messaging**: Allows clients to send messages directly to peers without routing through the server.
- **Command Execution**: Supports various commands like BROADCAST, STOP, LIST, KICK, MESSAGE, and STAT.

## Getting Started

To run ChatHu, follow these steps:

1. Ensure that Java is installed on your system.
2. Clone the repository to your local machine.
3. Compile and run the server component from the `server` directory.
4. Compile and run the client component from the `client` directory.
5. Use the client UI to connect to the server, discover peers, and start chatting.

## Contributions

Contributions are welcome! If you have any features, bug fixes, or improvements, please fork the repository, make your changes, and submit a pull request.
