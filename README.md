# What is node js!!

**Node.js is a powerful runtime environment for server-side JavaScript!!**

# Learning More

**Node.js has a vast ecosystem, and there are many libraries and frameworks to explore. Some popular libraries and frameworks include Express, Socket.io, and Sequelize for databases. I recommend referring to the official Node.js documentation and tutorials specific to the libraries you want to use.**

# Learn Core modules

## 1. Http Module

_Http Module: The http module allows you to create an HTTP server, handle HTTP requests, and serve HTTP responses. It's a fundamental module for building web applications and APIs._

```javascript
const http = require('http');

const server = http.createServer((req, res) => {
    res.writeHead(200, { 'Content-Type': 'text/plain' });
    res.end('Hello, World!\n');
});

server.listen(8080, 'localhost', () => {
    console.log('Server running at http://localhost:8080/');
});
```

## Fs Module

_Fs Module (File System): The **fs** module provides methods for working with the file system, including reading from and writing to files, creating directories, and performing file-related operations._

```javascript
const fs = require('fs');

fs.readFile('file.txt', 'utf8', (err, data) => {
    if (err) throw err;
    console.log(data);
});
```

## Path Module

_Path Module: The **path** module simplifies working with file and directory paths. It provides methods for handling and manipulating file paths in a cross-platform manner._

```javascript
const path = require('path');

const filePath = path.join(__dirname, 'files', 'example.txt');
console.log(filePath);
```

## Events Module

_Events Module: The **events** module allows you to work with events and event emitters. Node.js is event-driven, and many core modules and custom objects use event emitters to handle asynchronous events._

```javascript
const EventEmitter = require('events');

const eventEmitter = new EventEmitter();

eventEmitter.on('greet', () => {
    console.log('Hello, world!');
});

eventEmitter.emit('greet');
```

## Util Module

_Util Module: The **util** module provides various utility functions that can be helpful when working with JavaScript objects and inheritance, such as **util.inherits** and **util.promisify.**_


```javascript
const util = require('util');

const Person = function (name) {
    this.name = name;
};

util.inherits(Person, EventEmitter);

const person = new Person('John');
person.on('speak', function (message) {
    console.log(`${this.name} said: ${message}`);
});

person.emit('speak', 'Hello, world!');
```

# Node.js Core Modules

Node.js is a JavaScript runtime environment that comes with a set of built-in core modules to provide essential functionality for various tasks. These core modules are included with Node.js and can be used in your applications without the need to install additional packages.

## List of Core Modules

1. **http Module**: For creating HTTP servers and handling HTTP requests.
2. **https Module**: Similar to `http`, but for secure HTTPS servers.
3. **fs Module (File System)**: For working with the file system, reading and writing files, and managing directories.
4. **path Module**: For handling and manipulating file paths.
5. **os Module (Operating System)**: Provides information about the operating system on which Node.js is running.
6. **util Module (Utilities)**: Contains utility functions for working with JavaScript objects, including object inheritance.
7. **events Module**: For working with events and event emitters, which are fundamental to Node.js's event-driven architecture.
8. **stream Module**: Provides a framework for working with streams, which are a core concept in Node.js for reading and writing data efficiently.
9. **querystring Module**: For parsing and formatting URL query strings.
10. **url Module**: Provides utilities for URL manipulation and parsing.
11. **zlib Module**: For compressing and decompressing data using the zlib library.
12. **crypto Module**: Offers cryptographic functionality, including encryption, decryption, and secure hashing.
13. **os Module**: Allows you to interact with the operating system, providing information about the system and user environment.
14. **net Module**: Provides support for creating TCP servers and clients.
15. **dgram Module**: Enables UDP (User Datagram Protocol) communication.
16. **dns Module (Domain Name System)**: For domain name resolution and DNS queries.
17. **readline Module**: Provides an interface for reading input from a readable stream interactively.
18. **repl Module (Read-Eval-Print Loop)**: Creates a REPL environment (similar to a command-line interface) for running JavaScript interactively.
19. **child_process Module**: Allows you to spawn child processes and interact with them.
20. **cluster Module**: Helps in creating child processes to take advantage of multi-core systems.
21. **console Module**: Provides methods for printing messages to the console.

These are the core modules that are bundled with Node.js. You can use these modules to perform various tasks, from building web servers to interacting with the file system, managing child processes, and more. Understanding these core modules is essential for Node.js development.