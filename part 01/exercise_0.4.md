_note over_ **browser**:
the **browser** will send the user input to the **server**
_end note_

**browser**->**server**: HTTP POST https://fullstack-exampleapp.herokuapp.com/new_note
_note over_ **server**:
**server** responds with status code **302**, asking
the **browser** to do a new HTTP GET request to
the _notes_ address, **browser** reloads page
_end note_

**server**-->**browser**: Status Code **302**

**browser**->**server**: HTTP GET https://fullstack-exampleapp.herokuapp.com/notes
**server**-->**browser**: HTML-code
**browser**->**server**: HTTP GET https://fullstack-exampleapp.herokuapp.com/main.css
**server**-->**browser**: main.css
**browser**->**server**: HTTP GET https://fullstack-exampleapp.herokuapp.com/main.js
**server**-->**browser**: main.js
_note over_ **browser**:
**browser** starts executing js-code
that requests JSON data from **server**
_end note_

**browser**->**server**: HTTP GET https://fullstack-exampleapp.herokuapp.com/data.json
**server**-->**browser**: data.json
**server**-->**browser**: `[{ content: "HTML is easy", date: "2019-05-23" }, ...]`
_note over_ **browser**:
**browser** executes the event handler
that renders notes to display
_end note_
