# TCPIPDesktopServer
This is a simple Jetpack Compose Desktop application that will act as a TCP IP server. It will listen for a client, accept a connection, and then send and receive messages continuously.
<br>
# Key Concepts
**Server:** <br>
The desktop application. It creates a ServerSocket to listen for connections on a specific port. Once a client connects, it accepts the connection, creating a Socket for that specific client.

**Client:** <br>
The Android application. It creates a Socket and attempts to connect to the server's IP address and port.

**IP Address and Port:** <br>
The client needs the server's IP address and the port number it is listening on to establish a connection. They must be on the same network (e.g., connected to the same Wi-Fi router).

**Threading:** <br>
Network operations, especially blocking ones like waiting for a connection (server.accept()) or reading from a stream, must not be performed on the main UI thread. This is why we use Kotlin Coroutines to manage these tasks in the background.

<br> <br>
**Screenshot:** <br>
<img width="1182" height="891" alt="image" src="https://github.com/user-attachments/assets/6b921073-9dbb-482d-b76a-b4345a50a719" />
