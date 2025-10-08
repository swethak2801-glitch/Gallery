# Ex.08 Design of Interactive Image Gallery
# Date:8.10.25
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request. from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Image Gallery with Modal</title>
  <style>
    
    .gallery {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      justify-content: center;
    }

    .gallery img {
      width: 200px;
      height: 150px;
      cursor: pointer;
      border-radius: 8px;
      transition: transform 0.3s;
    }

    .gallery img:hover {
      transform: scale(1.05);
    }

    
    .modal {
      display: none;
      position: fixed;
      z-index: 10;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.9);
      justify-content: center;
      align-items: center;
    }

    .modal img {
      max-width: 90%;
      max-height: 80%;
      border-radius: 10px;
    }

    .close {
      position: absolute;
      top: 20px;
      right: 40px;
      color: white;
      font-size: 40px;
      font-weight: bold;
      cursor: pointer;
    }

    h1{
       text-align: center;
       color: blueviolet;
    }

   
  </style>
</head>
<body background="i6.jpg">

  <h1>DORAEMON IMAGE GALLERY</h1>
  <hr color="lightblue">
  <div class="gallery">
    <img src="i1.jpg" alt="Image 1" onclick="openModal(this)">
    <img src="i2.jpg" alt="Image 2" onclick="openModal(this)">
    <img src="i3.jpg" alt="Image 3" onclick="openModal(this)">
    <img src="i4.jpg" alt="Image 4" onclick="openModal(this)">
    <img src="i5.jpg" alt="Image 5" onclick="openModal(this)">
  </div>

  
  <div id="myModal" class="modal">
    <span class="close" onclick="closeModal()">&times;</span>
    <img id="modalImage" src="">
  </div>
  <hr color="lightblue">

  <script>
    function openModal(img) {
      const modal = document.getElementById("myModal");
      const modalImg = document.getElementById("modalImage");
      modal.style.display = "flex";
      modalImg.src = img.src;
    }

    function closeModal() {
      const modal = document.getElementById("myModal");
      modal.style.display = "none";
    }
  </script>

</body>
</html>
```
# OUTPUT:
<img width="1915" height="913" alt="Screenshot 2025-10-08 222537" src="https://github.com/user-attachments/assets/90a2c60b-0e2f-4e3f-8c10-13ef2d1cc9c9" />

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
