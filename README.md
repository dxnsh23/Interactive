# Ex.08 Design of Interactive Image Gallery
## Date:07.05.2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>NATURE</h1>
    </header>
    <div class="gallery">
        <div class="gallery-item" onclick="openModal(this)">
            <img src="download (17).jpeg" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="download (22).jpeg"  >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="download (24).jpeg" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="Batman pfp.jpeg" >
        </div>
    </div>

    <div id="modal" class="modal">
        <span class="close" onclick="closeModal()">&times;</span>
        <img class="modal-content" id="modalImage">
        <div id="caption"></div>
    </div>

    <script src="style.js"></script>
</body>
</html>

body {
    margin: 0;
    font-family: Arial, sans-serif;
  }
  
  header {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 1rem;
  }
  
  /* Put images in a row */
  .gallery {
    display: flex;
    justify-content: center;
    gap: 20px;
    padding: 20px;
  }
  
  /* Style each image */
  .gallery-item img {
    width: 200px;
    border: 3px solid transparent;
    cursor: pointer;
    transition: transform 0.3s, border-color 0.3s;
  }
  
  /* Highlight the clicked image */
  .gallery-item img.active {
    border-color: #4CAF50;
    transform: scale(1.05);
    box-shadow: 0 0 10px green;
  }
  
  /* Modal styles */
  .modal {
    display: none;
    position: fixed;
    z-index: 1000;
    top: 0; left: 0;
    width: 100%; height: 100%;
    background: rgba(0, 0, 0, 0.8);
  }
  
  .modal-content {
    display: block;
    margin: 80px auto;
    width: 80%;
    max-width: 700px;
  }
  
  .close {
    position: absolute;
    top: 15px;
    right: 30px;
    color: white;
    font-size: 40px;
    cursor: pointer;
  }

  function openModal(element) {
    const modal = document.getElementById("modal");
    const modalImage = document.getElementById("modalImage");
    const caption = document.getElementById("caption");

    modal.style.display = "flex";
    modalImage.src = element.querySelector("img").src;
    caption.textContent = element.querySelector("img").alt;
}

function closeModal() {
    const modal = document.getElementById("modal");
    modal.style.display = "none";
}
```

## OUTPUT:
![alt text](<Screenshot 2025-05-07 111658-1.png>)
![alt text](<Screenshot 2025-05-07 111725.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
