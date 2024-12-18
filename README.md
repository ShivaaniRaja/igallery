# Ex.08 Design of Interactive Image Gallery
## Date:15:12:24

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
  <title>Interactive Photo Gallery</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: url('backgroundgallery.jpg') no-repeat center center fixed;
      background-size: cover;
      margin: 0;
      padding: 0;
      color: white;
    }

    /* Title at the top */
    .title {
      text-align: center;
      font-size: 36px;
      font-weight: bold;
      padding: 20px 0;
      background-color: rgba(0, 0, 0, 0.7);
      color: white;
      margin-top: 0;
    }

    .gallery-container {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 15px;
      padding: 10px;
      justify-items: center;
    }

    .gallery-item {
      position: relative;
      overflow: hidden;
      border-radius: 8px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
    }

    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.3s ease;
    }

    .gallery-item:hover img {
      transform: scale(1.1);
    }

    /* Lightbox styles */
    .lightbox {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.8);
      justify-content: center;
      align-items: center;
    }

    .lightbox img {
      max-width: 40%;
      max-height: 50%;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.5);
    }

    .lightbox .close-btn {
      position: absolute;
      top: 20px;
      right: 20px;
      background-color: rgba(0, 0, 0, 0.7);
      color: white;
      font-size: 24px;
      border: none;
      border-radius: 50%;
      padding: 10px;
      cursor: pointer;
    }

    .lightbox .close-btn:hover {
      background-color: rgba(0, 0, 0, 0.9);
    }

    /* Name Box Styles */
    .name-box {
      position: fixed;
      bottom: 50px;
      left: 50%;
      transform: translateX(-50%);
      background-color: rgba(0, 0, 0, 0.6);
      color: white;
      padding: 10px 20px;
      font-size: 24px;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.4);
    }

  </style>
</head>
<body>

  <!-- Title Section -->
  <div class="title">
    PICTURE GALLERY
  </div>

  <div class="gallery-container">
    <div class="gallery-item" onclick="openLightbox('image1')">
      <img src="image1.jpg" alt="Image 1">
    </div>
    <div class="gallery-item" onclick="openLightbox('image2')">
      <img src="image2.jpg" alt="Image 2">
    </div>
    <div class="gallery-item" onclick="openLightbox('image3')">
      <img src="image3.jpg" alt="Image 3">
    </div>
    <div class="gallery-item" onclick="openLightbox('image4')">
      <img src="image4.webp" alt="Image 4">
    </div>
    <div class="gallery-item" onclick="openLightbox('image5')">
      <img src="image5.jpg" alt="Image 5">
    </div>
  </div>

  <!-- Lightbox -->
  <div id="lightbox" class="lightbox">
    <button class="close-btn" onclick="closeLightbox()">×</button>
    <img id="lightbox-img" src="" alt="Full Image">
  </div>

  <!-- Name Box at the Bottom -->
  <div class="name-box">
    DESIGNED AND DEVELOPED BY R.SHIVAANI (24007075)
  </div>

  <script>
    function openLightbox(imageId) {
      const lightbox = document.getElementById('lightbox');
      const lightboxImg = document.getElementById('lightbox-img');

      // Set the source for the image based on the clicked image
      switch(imageId) {
        case 'image1':
          lightboxImg.src = 'image1.jpg';
          break;
        case 'image2':
          lightboxImg.src = 'image2.jpg';
          break;
        case 'image3':
          lightboxImg.src = 'image3.jpg';
          break;
        case 'image4':
          lightboxImg.src = 'image4.webp';
          break;
        case 'image5':
          lightboxImg.src = 'image5.jpg';
          break;
      }

      // Show the lightbox
      lightbox.style.display = 'flex';
    }

    function closeLightbox() {
      const lightbox = document.getElementById('lightbox');
      lightbox.style.display = 'none';
    }
  </script>

</body>
</html>
```
## OUTPUT: 
![alt text](<Screenshot 2024-12-15 111544-1.png>) 
![alt text](<Screenshot 2024-12-15 111602-1.png>) 
![alt text](<Screenshot 2024-12-15 111617-1.png>)
![alt text](<Screenshot 2024-12-15 111632-1.png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
