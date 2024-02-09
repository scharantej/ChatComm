# Flask Application Design for a Progressive Web App for Text Chat over WebRTC

## HTML Files

- **index.html:** This is the main HTML file that serves as the entry point for the application. It includes the necessary JavaScript libraries and establishes the WebSocket connection for real-time communication.
- **chat.html:** This HTML file displays the chat interface with text input fields, a message history section, and buttons for sending messages and connecting/disconnecting from the chat session.

## Routes

- **/:** The root route, which redirects to the main chat interface (chat.html).
- **connect:** This route handles the WebSocket connection request and establishes a WebSocket. It also broadcasts the new user's connection to other connected clients.
- **message:** This route receives chat messages sent by clients via WebSockets. It then forwards these messages to all other connected clients in the chat session.
- **disconnect:** This route handles WebSocket disconnection requests. It broadcasts the disconnecting user's departure to other connected clients and closes the WebSocket connection.

## CSS and JavaScript

- The application will utilize CSS for styling elements in the HTML files, ensuring a visually appealing user interface.
- JavaScript will be employed to enable WebSocket communication, handle dynamic interactions on the web pages, and provide real-time chat functionality.