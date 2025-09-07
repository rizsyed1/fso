<!-- Create a diagram depicting the situation where the user goes to the single-page app version of the notes app at https://studies.cs.helsinki.fi/exampleapp/spa. -->
```mermaid
  sequenceDiagram
    participant browser
    participant server

    Note right of browser: The browser starts executing the javascript code that adds the new note data to the front end.

    browser->>server: POST https://studies.cs.helsinki.fi/new_note_spa [{"content": "note", "date": "2025-09-07T20:13:40.163Z"}]
    activate server
    server-->>browser: [{"message": "note created"}]
    deactivate server
```