# Notes

- Use a websocket (a bi-directional chat that allows both client and server to send messages to each other at any time.)

- We can write a kind of http server. This server is always running. We can keep polling this server
to constantly get updates, or we could just set up websockets that will keep a connection open between the server and client.

- app.js runs as a client in the browser and listens to our server at whatever port. It then manipulates the DOM (index.html defined divs) with whatever information it receives from the server.

- We want our client to listen to new messages from the server and users active. Add event handlers to our client's websocket (what connects it to the server) and do something when our clients receive a new message or event.

- JSON stringify
```
socket.send(
    JSON.stringify({
        event: "send-message",
        message: message,
    }),
```
