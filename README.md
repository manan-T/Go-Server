# Simple Go Web Server

This project demonstrates a basic web server written in Go. It serves static files, handles HTTP requests, and includes a form that accepts user input.

## Features

- **Static File Serving**: Serves static files from the `static` directory.
- **Form Handling**: Handles a form submission via a POST request and displays the submitted data.
- **Hello Handler**: A simple endpoint that responds with a greeting message.

## Project Structure

```
.
├── main.go        # The main Go file with the server implementation
├── static         # Directory for static files
│   ├── index.html # Homepage for the web server
│   └── form.html  # Form page for user input
```

## Endpoints

### `/` (Static File Server)
Serves the static files located in the `static` directory. For example:
- `index.html` is served when you visit `http://localhost:8080/`

### `/hello`
- **Method**: GET
- **Response**: "hello!"
- **Error Handling**: Returns a 404 if the path is incorrect or if a non-GET method is used.

### `/form`
- **Method**: POST
- **Functionality**: Handles form submissions and displays the submitted `name` and `address` values.
- **Error Handling**: Parses the form and returns an error message if parsing fails.

## How to Run

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Setup the Project**
   Ensure you have Go installed. If not, [download and install Go](https://go.dev/dl/).

3. **Build and Run the Server**
   ```bash
   go run main.go
   ```

4. **Access the Application**
   Open your browser and navigate to:
   - [http://localhost:8080/](http://localhost:8080/) to view the static website.
   - [http://localhost:8080/form](http://localhost:8080/form) to submit the form.
   - [http://localhost:8080/hello](http://localhost:8080/hello) to view the greeting message.

## Example Usage

### Submitting the Form
1. Go to [http://localhost:8080/form](http://localhost:8080/form).
2. Enter your `Name` and `Address` in the form.
3. Click `Submit`.
4. The server will respond with:
   ```
   POST request successful
   Name = <Your Name>
   Address = <Your Address>
   ```

## File Descriptions

### `main.go`
Contains the implementation of the Go web server with three main functionalities:
- Serving static files.
- Handling the `/form` POST request.
- Responding to the `/hello` GET request.

### `static/index.html`
A basic static HTML page displayed when accessing the root endpoint (`/`).

### `static/form.html`
A simple HTML form that allows users to input their name and address and submit the data via a POST request.

## Requirements

- Go 1.20+
