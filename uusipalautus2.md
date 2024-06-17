```mermaid
sequenceDiagram
    participant browser
    participant server

    browser ->> server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server -->> browser: processesses data and sends back new JSON file (no page reload)
    deactivate server

    Note right of browser: new data is being reloaded by existing JavaScript code
