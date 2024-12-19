## Another try 

<div id="image-container">
    <img id="image-display" src="assets/img/distribution-actor-director-age-1-film.png" alt="Image 1" style="width:100%; max-width:600px;">
</div>

<div id="slider-container" style="margin-top: 20px;">
    <input type="range" id="image-slider" min="0" max="2" value="0" style="width: 100%;">
</div>

<script src="test2.js"></script>

## Anotherother try 


<div id="selector-container" style="margin-top: 20px;">
    <select id="image-selector" style="width: 100%;">
        <option value=0>Actor-Director Behaviour</option>
        <option value=1>Actor-Movie Behaviour</option>
        <option value=2>Actor-Gender Behaviour</option>
    </select>
</div>

<div id="image-container">
    <img id="image-display" src="assets/img/distribution-actor-director-age-1-film.png" alt="Image 1" style="width:100%; max-width:600px;">
</div>


<script src="test.js"></script>

## JavaScript - Slider Change Image Example

This example lets you move a slider to select an image dynamically.

---

<div style="margin-top: 20px;">
  <h4 style="color: black; text-align: center;">Move the slider to select an image</h4>
  <hr style="border-top: 1px dotted #ccc;" />

  <div style="text-align: center;">
    <label for="image-slider">Choose a position:</label>
    <input type="range" id="image-slider" min="0" value="0" style="width: 80%; margin: 10px auto;" />
  </div>

  <div id="slider-result" style="
      height: 250px;
      width: 80%;
      margin: 20px auto;
      border: 1px solid #000;
      text-align: center;
      display: flex;
      justify-content: center;
      align-items: center;
    ">
    <p style="color: gray;">Image will appear here</p>
  </div>
</div>

<script>
  // Array of image paths
  const images = [
    'assets/img/distribution-actor-director-DoB.png',
    'assets/img/distribution-actor-director-age-1-film.png',
    'assets/img/distribution-actor-director-age-movie.png',
    'assets/img/distribution-nbr-film-actor-director.png'
  ];

  document.addEventListener('DOMContentLoaded', () => {
    // DOM elements
    const imageSlider = document.getElementById('image-slider');
    const sliderResult = document.getElementById('slider-result');

    // Check if sliderResult and imageSlider exist
    if (!imageSlider || !sliderResult) {
      console.error("Required DOM elements are missing.");
      return;
    }

    // Dynamically set slider range
    imageSlider.max = images.length - 1;

    // Function to update the image display
    function updateImage() {
      const index = parseInt(imageSlider.value, 10); // Get current slider value
      const imagePath = images[index];

      // Check if the image path exists
      if (imagePath) {
        sliderResult.innerHTML = `
          <img src="${imagePath}" alt="Selected Image" style="max-width: 100%; height: 100%;">
        `;
      } else {
        sliderResult.innerHTML = `<p style="color: red;">Image not found!</p>`;
        console.error(`Image not found for index: ${index}`);
      }
    }

    // Initial image load
    updateImage();

    // Event listener for slider changes
    imageSlider.addEventListener('input', updateImage);
  });
</script>

## Try image time scrolling

Click on the `start` button to see the evolution of the newtork over time. 

<div id="image-container">
    <img id="image-display" src="assets/img/distribution-actor-director-age-1-film.png" alt="Image 1" style="display: block; margin: 0 auto; width: 80%;"/>
</div>

<button id="action-button"> start </button>

<script src="script.js"></script>



