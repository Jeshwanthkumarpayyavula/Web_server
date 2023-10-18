# Developing a Simple Webserver
Name: Jeshwanthkumar
refno: 23002519
emailid: jeshwanthkumarpayyavula@gmail.com

# AIM:

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver
# PROGRAM:
```from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
<body>
<h1>Welcome</h1>
</body>
</head>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request recieved")
        self.send_response(200)
        self.send_header('Content-type','text/html;charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver")
server_address = ('',80)
httpd = HTTPServer(server_address,HelloHandler)
```
# OUTPUT:
![image](https://github.com/Jeshwanthkumarpayyavula/Web_server/assets/145742402/dffae081-3fee-4d4a-b03e-0e3ac342dc1c)

# RESULT:

The program is executed succesfully
