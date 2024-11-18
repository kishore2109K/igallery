# Ex.08 Design of Interactive Image Gallery
## Date:18.11.24

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
HTML code:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>5 Superheroes Gallery</title>
    <link rel="stylesheet" href="styles.css"> <!-- Link to the external CSS -->
</head>
<body>

<header>
    <h1>Interactive Photo Gallery</h1>
</header>

<div class="gallery-container">
    <img src="HD-wallpaper-ironman-ironman-2-superhero-thumbnail.jpg" alt="Iron Man" class="gallery-image" onclick="openLightbox(0)">
    <img src="one-swing-at-a-time-ecp43rcqayizcyuf.jpg" alt="Spider-Man" class="gallery-image" onclick="openLightbox(1)">
    <img src="272_Comics_Wallpaper_1080x1920px.jpg.webp" alt="Superman" class="gallery-image" onclick="openLightbox(2)">
    
    <div class="bottom-row">
        <img src="mhe7usa7y9g81.jpg" alt="Batman" class="gallery-image" onclick="openLightbox(3)">
        <img src="images (1).jpeg" alt="Thor" class="gallery-image" onclick="openLightbox(4)">
    </div>
</div>

<div class="lightbox" id="lightbox">
    <button class="close" onclick="closeLightbox()">&times;</button>
    <img src="" alt="" id="lightbox-image">
</div>

<script src="scripts.js"></script> 
</body>
</html>
```
CSS code:
```
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f5f5f5;
    color: #333;
}

header {
    text-align: center;
    background-color: #3b3b3b;
    color: white;
    padding: 2rem 0;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

header h1 {
    font-size: 3rem;
    margin: 0;
}

header p {
    font-size: 1.2rem;
    margin-top: 10px;
}

.gallery-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* 3 images in the first row */
    grid-template-rows: auto auto; /* Two rows */
    grid-gap: 1.5rem;
    padding: 3rem;
    max-width: 1200px;
    margin: 0 auto;
}

.gallery-container .bottom-row {
    grid-column: span 3; /* Bottom row takes up the full width */
    display: flex;
    justify-content: center;
    gap: 1.5rem;
}

.gallery-image {
    width: 80%; /* Reduced width */
    height: auto; /* Maintain aspect ratio */
    object-fit: cover;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
    transition: transform 0.3s, box-shadow 0.3s;
    cursor: pointer;
    border: 2px solid transparent;
    transition: all 0.3s ease-in-out;
}

.gallery-image:hover {
    transform: scale(1.05);
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
    border: 2px solid #ff9900;
}

/* Lightbox */
.lightbox {
    position: fixed;
    top: 0;
    left: 0;
    width: 50%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    display: none;
    justify-content: center;
    align-items: center;
    z-index: 1000;
}

.lightbox img {
    max-width: 90%;
    max-height: 80%;
    border-radius: 10px;
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.4);
}

.lightbox .close {
    position: absolute;
    top: 20px;
    right: 30px;
    font-size: 2rem;
    color: white;
    cursor: pointer;
    background-color: transparent;
    border: none;
}

.lightbox .close:hover {
    color: #ff9900;
}
```
JS code:
```
const images = [
    "HD-wallpaper-ironman-ironman-2-superhero-thumbnail.jpg",
    "one-swing-at-a-time-ecp43rcqayizcyuf.jpg",
    "272_Comics_Wallpaper_1080x1920px.jpg.webp",
    "mhe7usa7y9g81.jpg",
    "images (1).jpeg"
];

const lightbox = document.getElementById("lightbox");
const lightboxImage = document.getElementById("lightbox-image");

function openLightbox(index) {
    lightboxImage.src = images[index];
    lightbox.style.display = "flex";
}

function closeLightbox() {
    lightbox.style.display = "none";
    lightboxImage.src = "";
}
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/696c496d-f61a-4d34-8bba-51652ca288da)
![image](https://github.com/user-attachments/assets/7880b31b-b1e9-4d59-970c-988e355908be)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
