# asciiart-logo

Library _asciiart-logo_ creates a rectangular panel with ASCII-art from application name, and optional additional information (author, application version, etc).

_asciiart-logo_ uses [FIGlet](http://www.figlet.org/examples.html) fonts for ASCII art title text.

## Quick Start

Download and installation of the library

``` Bash
npm install --save asciiart-logo
```

Usage in source code

``` JavaScript
const logo = require('asciiart-logo');
console.log(
  logo({
    title: 'Foo Bar',
    font: 'speed',
    padding: 5,
    margin: 2
  })
  .emptyLine()
  .right('version 3.7.123')
  .emptyLine()
  .wrap('This is a longer text that describes the values of the component for command line applications.')
  .render()
);
```

... and the output on the console:

``` console

  ,------------------------------------------------------------------.
  |                                                                  |
  |                                                                  |
  |     __________                     ________                      |
  |     ___  ____/______ ______        ___  __ )______ _________     |
  |     __  /_    _  __ \_  __ \       __  __  |_  __ `/__  ___/     |
  |     _  __/    / /_/ // /_/ /       _  /_/ / / /_/ / _  /         |
  |     /_/       \____/ \____/        /_____/  \__,_/  /_/          |
  |                                                                  |
  |                                                                  |
  |                                              version 3.7.123     |
  |                                                                  |
  |     This is a longer text that describes the values of the       |
  |     component for command line applications.                     |
  |                                                                  |
  |                                                                  |
  `------------------------------------------------------------------'

```

You may be interested also in complete [example code](./example.js) that shows typical usage of the asciiart-logo library.

## Dependency

Component uses the library [figlet](https://www.npmjs.com/package/figlet) for ASCII art text rendering.
