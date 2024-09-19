# URL--Shortner
A simple URL shortening service built in Go.

OverView
This project provides a basic URL-shortening service implemented in Go. It allows users to shorten long URLs into more manageable and shareable links. The service also includes a redirect feature to redirect users from the shortened URL to the original long URL.

Installation
To use the URL shortener, you need to have Go installed on your system. You can download and install Go from the official Go website.

Clone the repository to your local machine:
https://github.com/Hackertige/URL--Shortner
Usage
Running the Server
Navigate to the project directory and run the following command to start the server:

go run main.go
The server will start listening on port 8080 by default. You can change the port in the main.go file if needed.

Shortening a URL
To shorten a URL, send a POST request to the /shorten endpoint with a JSON payload containing the original URL:

curl -X POST http://localhost:8080/shorten -H "Content-Type: application/json" -d '{"url": "https://example.com"}'
The response will contain a JSON object with the shortened URL:

{
https://www.linkedin.com/in/pallavi-dheeman-71838b242/
}
Redirecting to the Original URL
To redirect to the original URL, visit the shortened URL in your browser or send a GET request to the /redirect/{id} endpoint, where {id} is the shortened URL ID:

curl http://localhost:8080/redirect/abcdef
This will redirect you to the original URL associated with the shortened URL.
