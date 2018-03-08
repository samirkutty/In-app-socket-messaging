# In-app-socket-messaging
This app showcases how socket.io can be used for to throw a notification once a process is completed on the server

To run the project: 
1. clone the project 
2. cd to the respective socket-io-client and socket-io-server directories
3. npm install
4. in the client directory: npm start
5. in the server directory: node app.js


Steps to integrate:
On Server(socket-io-server): 
1. npm install socket.io, express and axios 
2. In app.js setup the server and the port. Then setup a socket connection with the client as shown.
3. Once connected make an api call to required data.
4. Once data is available the socket will emit an event called FromAPI

On Client(socket-io-client): 
1. In App.js in the src directory, listen to the emit event 'FromAPI' and use the data received to compare and throw the in app notification.

Working: 
The temperature is displayed on the screen using DarkSky api. Everytime there is a change in the temperature an alert message is shown to the user.
