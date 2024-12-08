# Ex.06 Book Front Cover Page Design
# Date:25.11.2024
# AIM:
To design a book front cover page using HTML and CSS.

# DESIGN STEPS:
## Step 1:
Create a Django Admin project.

## Step 2:
Create an app in the Django interface.

## Step 3:
Create a folder named 'static' in the app folder.

## Step 4:
Create a new HTML file in the static folder.

## Step 5:
Write the HTML code with relevant CSS properties.

## Step 6:
Choose the appropriate style and color scheme.

## Step 7:
Insert the images in their appropriate places.

## Step 8:
Publish the website in the LocalHost.

# PROGRAM:


```

view.py

from http.server import BaseHTTPRequestHandler, HTTPServer
from importlib.resources import contents
from django.http import HttpResponse
from django.shortcuts import render


content='''<html>
     <head>
          <meta name="viewport"
          content="width=device-width, initial-scale=1.0">
          <style>
         


         .bookpage{
              width: 400px;
              height: 600px;
              color:rgba(243, 195, 195, 0.938)00, 17, 17;
              margin-left : auto;
              margin-right : auto;
              padding: 20px;

              font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
              background-image: url(cover2.png);
              background-size: cover;
              }
             .insight{
                color:whitesmoke;
              }

             .hrstyle{
             width:100px;
             }
             .author{
             display: inline;
             position: relative;
             color:rgb(51, 117, 180);
             top:240px;

             font-family:Georgia;
             font-size: medium;
             }
             .booktitle{
             font-family: 'Courier New',Courier,monospace;
             font-size: larger;
             text-align: center;
             position: relative;
             top: 30px;
             color:white;
             
             }
             .id {
             width:400px;
             position: relative;
             top:250px;
             }
             .pub{
             font-size: medium;
             position: relative;
             top:204px;
             left:350px;
             color:white;
             }
             .ed{
             color:white;
             font-size: medium;
             font-family: Verdana;
             position:relative;
             top:150px;
             }
             .mypic{
             position:relative;
             top:200px;
             left: 275px;
             width: 40px;
             height: 90px;
             background-size:cover;
             }
             </style>
             <title>Book Cover Page</title>
             </head>
             <body>
             <div class="bookpage">
             <div class="insight">
                DHASVANTH PUBLICATION
             </div>
             <div class="hrstyle">
                <hr style="color: rgb(128, 128, 96);">
             </div>
             <div class="booktitle">
             <h1>THE GOD REALLY EXIST?</h1>
             </div>
             <div class ="mypic">
               <img src="photo.jpg" width="130" height="145" alt="">
             </div>
             <div class="id">
             <hr style="color: rgb(145, 145, 114);">
             </div>
             <div class="author">
             <p><b>Santhosh Venkatesan</b></p>
             </div>
             <div class="pub">
             SEC
             </div>
             <div class="ed">
             <b>FIRST VERSION</b>
          </div>
    </body>
</html>'''
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header("content-type","text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()

urls.py

from tempfile import template
from django.contrib import admin
from django.urls import path
from app2.views import MyServer

urlpatterns = [
    path('admin/', admin.site.urls),
    # path('new/',views.trial),
    # path('page/',views.slot),
    # path('home/',template.slot),
    path('server/',MyServer.as_view())
]
```
# OUTPUT:

![Screenshot 2024-12-08 213605](https://github.com/user-attachments/assets/4ae8e874-fa0c-4354-aade-4cd6bdda8048)

![Screenshot 2024-12-08 222700](https://github.com/user-attachments/assets/cafd0dc4-a30d-42a8-a5ab-6fc68aab933c)


# RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.
