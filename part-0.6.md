sequenceDiagram
participant browser
participant server

browseer->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
activate server
server->>browser: The HTML document
deactivate server

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
activate server
server->>browser: The CSS File
deactivate server

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
activate server
server->>browser: The JS file
deactivate server

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
activate server
server->>browser: The data in json
deactivate server

browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
activate server
The event handler renders the new note on the page and sends the new note in json format with date to the server