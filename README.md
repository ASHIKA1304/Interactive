# Ex.08 Design of Interactive Image Gallery
## Date:07-05-25

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

## file.html
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
            <img src="Doremon.png" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="Bheem.png"  >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="Raju.png" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="Titoo.png" >
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
```

## style.js
```
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

![alt text](<Screenshot 2025-05-07 105310.png>)

![alt text](<Screenshot 2025-05-07 105327.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
