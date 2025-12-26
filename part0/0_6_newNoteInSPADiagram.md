sequenceDiagram
    participant browser
    participant server

    browser->>: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server

    Note right of browser: The browser sends JSON data of the new note to the server

    server-->>browser: {"message":"note created"}
    deactivate server

    Note right of browser: The browser stays in the same page, no further request