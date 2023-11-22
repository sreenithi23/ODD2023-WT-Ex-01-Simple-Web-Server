# Ex-01-Simple-Web-Server
name : sreenithi


ref no: 2300660
## Date:

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
<title>webservers</title>
</head>
<body>
<h1>Top Five Web Apllication Development Framework</h1>
<h1>1.Django</h1>
<h2>2.MEAN Stack</h2>
<h3>3.React<h3>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

server_address = ('', 80)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()
```


## OUTPUT:

![Screenshot 2023-11-21 195322](https://github.com/sreenithi23/ODD2023-WT-Ex-01-Simple-Web-Server/assets/147017600/bf6f2ec4-8e00-4407-91ee-e15a470f3301)


## RESULT:
The program for implementing simple webserver is executed successfully.
