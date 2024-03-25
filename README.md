# EX01 Developing a Simple Webserver
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
'''
<html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saveetha</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <style>
        a{
            padding: 10px;
            text-decoration: none;
            color:white;
            font-family: arial;
            font-size: 18px;
        }
        a:hover{
            color: rgb(242, 44, 44);
        }   
    </style>
</head>
<body style="background-color:black;">
     <div style="display:flex">
        <div style="width: 20%"><img style="width: 70%" src="net.jpg"></div>
        <div style="width: 55%;padding-top: 13px    ">
            <a href="https://www.netflix.com/browse">Home</a>
            <a href="https://www.netflix.com/browse">About</a>
            <a href="https://www.netflix.com/browse/genre/34399">Life at SEC</a>
            <a href="https://www.netflix.com/browse/genre/83">Saveetha</a>
            <a href="https://www.netflix.com/browse/my-list">Result</a>
            <a href="https://www.netflix.com/browse/original-audio">Placement</a>
        </div>  
        <div style="width: 20%;padding-top: 8px">
        <input style="width: 80%;height: 30px;background-image: url('search.jpeg');background-color: white; background-size: contain;background-repeat: no-repeat;padding-left: 40px;" type="text" placeholder="search" >
        </div>
     </div>
     
     <h1 style="color:white;text-align: center;font-style: italic;font-size: 50px;">TOP PLACEMENTS</h1>
     <div id="carouselExample" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="s3.png" class="d-block w-100" alt="..." width="50%">
          </div>
          <div class="carousel-item">
            <img src="s1.png" class="d-block w-100" alt="...">
          </div>
          <div class="carousel-item">
            <img src="s2.png" class="d-block w-100" alt="...">
          </div>
          <div class="carousel-item">
            <img src="s4.png" class="d-block w-100" alt="...">
          </div>
          <div class="carousel-item">
            <img src="s5.png" class="d-block w-100" alt="...">
          </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExample" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
     <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>  
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type','text/html;charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address=('',8000)
httpd=HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type','text/html;charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address=('',8000)
httpd=HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
'''
## OUTPUT:
![Screenshot 2024-03-25 155722](https://github.com/Karthickraja23006120/simplewebserver/assets/139335315/b5950301-98f0-4bc0-965e-4336db73ef5c)
![Uploading Screenshot 2024-03-25 155736.png…]()



## RESULT:
The program for implementing simple webserver is executed successfully.
