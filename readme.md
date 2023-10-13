# Multi-Threaded Client-Server Chat Application

## Overview

This is a multithreaded client-server chat application developed in C for Unix/Linux systems. It allows multiple clients to connect to a central server and engage in real-time chat with each other. Clients can run in separate terminals, and they don't need to be on the same machine.

## Demo
![multi-threaded-client-server-dem](https://github.com/tapasrnk/multithreaded-client-server/assets/74441392/1cf0cd62-2cf9-4138-b6d0-e960bea0c7fb)

## Prerequisites

- Unix/Linux operating system
- C compiler (e.g., GCC)
- Basic understanding of terminal commands

## How to Run

### Server

1. Open a terminal for the server.
2. Compile the server code using GCC:
   ```bash
   gcc server.c -o server && ./server _PORT_

### Client

1. Open multiple terminals for clients (4 in this example).
2. Compile the server code using GCC:
   ```bash
   gcc client.c -o client && ./client _SERVER-IP-ADDRESS_ _SERVER-PORT_
3. Replace _SERVER-IP-ADDRESS_ with the IP address of the server and _SERVER-PORT_ with the port number on which the server is running. For example:
   ```bash
   gcc client.c -o client && ./client 10.10.75.20 1235
# Usage

Use the following commands to interact with the server:

- `~list`: To see the list of free users. Example: `~list`
- `~connect_to_$userid`: To connect to a user with user-id $userid. Example: `~connect_to_03`
- `~stop`: To stop the chat and log off the session. Example: `~stop`
- `~quit`: To disconnect from the server. Example: `~quit`
- `~my_id`: To know your user id. Example: `~my_id`
- `$message`: To send a message $message. Note that the size of the message should be less than 200 characters and should not contain spaces. Example: `hello_user_03_how_are_you`

Users can receive messages from other users only after sending a message. Chatting occurs by sending one message alternately between two users. The server logs active user sessions and when two users connect for a chat or log out of the session.
# Important Notes
- Use only the `~quit` command to disconnect from the server; otherwise, the server might crash.
- If you encounter any issues, consider restarting the server and the clients.

# Contact

For any questions or issues, please contact [tapasrnk@gmail.com](tapasrnk@gmail.com) .

