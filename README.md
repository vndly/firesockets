# Firesockets
Web sockets support for Firebase

## CLIENT

connect()
Generates a random UUID
Creates a document in the table firesockets

send(message: string)
Creates a new entry in the Socket.Message colection

close()
Changes the status of the Socket document to "closed"

onConnect(socketId: string)
When the document socket is created

onMessage(socketId: string, message: string)
When the server sends a message

onError(socketId: string, error: string)
When an error occurs

onClose(socketId: string)
When the socket is closed

## SERVER

onConnect(socketId: string)
When the document socket is created

onMessage(socketId: string, message: string)
When the client sends a message

onError(socketId: string, error: string)
When an error occurs

onClose(socketId: string)
When the socket is closed

## DATABASE

### Socket
* id: string
* created: datetime
* client: Collection<Message>
* server: Colection<Message>
* status: open | closed

### Message
* id: string
* message: string
* created: datetime