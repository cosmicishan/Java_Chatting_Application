# Java_Chatting_Application
Chatting Application using Socket in Java

![Screenshot from 2023-10-27 22-56-51](https://github.com/cosmicishan/Java_Chatting_Application/assets/37193732/39b34763-e399-4d49-8d5f-7c6752778584)

This Chatting Application comprises both a client and a server implemented in Java using Swing for the graphical user interface. The client and server interact to enable real-time messaging between users.

**Server (Server.java)**

The server component manages communication between clients and provides a graphical user interface for administrators. It handles the following functionalities:

* User Interface: The server's GUI includes a header panel displaying the server's profile picture, username, and status, a chat window for conversation history, a message input field, and a send button.

* Message Sending: Administrators can enter messages in the input field and click "Send" to transmit messages to connected clients. Messages are formatted using the formatLabel() method and then sent to clients via DataOutputStream.

* Message Reception: The server listens for incoming messages from clients using a ServerSocket, and it receives messages via DataInputStream. Received messages are formatted using formatLabel() and displayed in the chat window.

* Network Communication: The server communicates with clients using DataInputStream and DataOutputStream.

**Client (Client.java)**

The client represents the user's side and has a similar graphical interface to the server. It interacts with the server to exchange messages in real-time. The main interaction flow involves:

The client's GUI includes a chat window, message input field, and send button. Users can enter messages in the input field and click "Send" to send messages to the server. The server continuously listens for incoming messages from clients and displays them in the chat window. The server also broadcasts these messages to all connected clients.


*In summary, the client and server Java files interact as follows:*

The server creates a ServerSocket to listen for incoming connections.

The client establishes a connection to the server using a Socket and sets up DataInputStream and DataOutputStream for communication.

The client sends messages to the server using DataOutputStream.

The server receives these messages, formats them, and displays them in the chat window. Simultaneously, it broadcasts the messages to other connected clients.

This interaction allows users to exchange messages in real-time through the server, and the chat history is displayed in the client's chat window.
