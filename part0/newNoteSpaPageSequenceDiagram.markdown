sequenceDiagram
    participant browser
    participant server

    Note right of browser: The user write some notes in the input and press save.

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: Response 201(Note created)
    deactivate server

    Note right of browser: The browser re-render the notes adding the las one