[![progress-banner](https://backend.codecrafters.io/progress/http-server/c5a8883b-5a19-4cf1-881a-96772dbbce98)](https://app.codecrafters.io/users/codecrafters-bot?r=2qF)

This is a Java solution to CodeCrafters'
["Build Your Own HTTP server" Challenge](https://app.codecrafters.io/courses/http-server/overview).

## Overview
This Java application is a basic implementation of an HTTP server. It handles HTTP requests, processes them, and sends appropriate responses. The server supports various response codes, content types, and can handle `GET` and `POST` requests.

## Features
- **HTTP Response Codes**: Implements basic HTTP response codes like `200 OK`, `404 Not Found`, and `201 Created`.
- **Content Types**: Supports `text/plain` and `application/octet-stream` for text and binary files, respectively.
- **Request Parsing**: Parses HTTP requests to extract method, path, version, user-agent, host, and body.
- **Dynamic Response Generation**: Generates responses based on the request path and method.
- **File Handling**: Can serve files from a specified directory and handle file creation through `POST` requests.

## Usage
1. **Compilation**: Compile the Java files using a Java compiler.
2. **Execution**: Run the main class. Optionally, specify the `--directory` argument to set the directory from which files will be served.

   Example: `java Main --directory /path/to/directory`

3. **Interacting with the Server**: The server listens on port `4221`. Use any HTTP client to send requests.

   Examples of HTTP paths:
   - `/` : Returns a simple "Hello World!" message.
   - `/echo/[message]` : Echoes the message sent in the path.
   - `/user-agent` : Returns the user-agent of the HTTP request.
   - `/files/[filename]` : For `GET`, returns the content of the file if it exists. For `POST`, creates or updates the file with the request body.

## Extra Notes
- Ensure the directory specified exists and has the appropriate read/write permissions.
- The server does not implement the full HTTP specification and is intended for educational or testing purposes only.
