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
    from http.server import HTTPServer, BaseHTTPRequestHandler
    content = """
    <!DOCTYPE html>
    <html>
    <head>
    <title>My webserver</title>
    </head>
    <body>
    <h1>Top 5 Revenue Generating Companies<h1>
    <UL TYPE=“circle”>
    <LI> Flipkart </LI>    
    <LI> SBI </LI>
    <LI> Infosys </LI>
    <LI> Rahul an Co </LI>
    <LI> ITC </LI>
    </UL>
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
    server_address = ('',8000)
    httpd = HTTPServer(server_address,myhandler)
    print("my webserver is running...")
    httpd.serve_forever()

## OUTPUT:
![image](https://github.com/rahulramakrishnann/Exp1-simple-web-server/assets/143045415/23bc2003-3163-4348-8eec-9d3de95edaf0)

![image](https://github.com/rahulramakrishnann/Exp1-simple-web-server/assets/143045415/93eb801d-48a2-4129-bef0-390888641121)

## RESULT:
The program for implementing simple webserver is executed successfully.
