# Developing a Simple Webserver
## AIM:
To develop a simple webserver to serve html pages.
## DESIGN STEPS:
### Step 1: 
HTML content creation
### Step 2:
Design of webserver workflow
### Step 3:
Implementation using Python code
### Step 4:
Serving the HTML pages.
### Step 5:
Testing the webserver

## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Webserver</title>
</head>
<body>
    <h1>Top 5 Revenue Companies</h1>
    <ol>
        <li>Flipkart</li>
        <li>SBI/li>
        <li>Infosys</li>
        <li>Rahul and co</li>
        <li>ITC</li>
    </ol>
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8080)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```
## OUTPUT:
![WhatsApp Image 2024-09-24 at 5 45 05 PM](https://github.com/user-attachments/assets/9e2957fd-6bac-4608-b663-4e38fbc4b5d9)
![WhatsApp Image 2024-09-24 at 5 45 05 PM (1)](https://github.com/user-attachments/assets/d12f81cf-83b3-4902-bfbb-354ba3348104)


## RESULT:
The program for implementing simple webserver is executed successfully.
