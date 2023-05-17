# Diagram 

This diagram depicting the situation where the user creates a new note on the single-page app version of the notes app at https://studies.cs.helsinki.fi/exampleapp/spa by writing something into the text field and clicking the submit button.

```mermaid
sequenceDiagram
    participant browser
    participant server

    activate browser
    Note right of browser: The browser starts execung JavaScrypt code which adds the new note to the notes list
    Note right of browser: and sends the new note to the server
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server->>browser: status code 201 created
    deactivate server
    Note right of browser: The browser executes JavaScrypt code callback function that rerenders the page
    deactivate browser
```