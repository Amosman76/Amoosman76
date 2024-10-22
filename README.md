# Amoosman76![Uploading IMG_4523.JPG…]()
<!doctype html>
<html lang="en"> 
 <head> 
  <meta charset="UTF-8"> 
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
  <title>Happy Birthday [Her Name]!</title> 
  <link rel="stylesheet" href="styles.css"> <!-- For adding custom styles --> 
 </head> 
 <body> 
  <div class="container"> 
   <h1>Happy Birthday MAAB OSMAN!</h1> 
   <p class="intro-text">Wishing you all the happiness in the world today!</p> <!-- Add a countdown timer --> 
   <div class="countdown"> 
    <p> ❤️ كل عام وانت بخير ☀️ ربع قرن من الجمال والصفاء - رعاك الله:</p> 
    <div id="timer"></div> 
   </div> <!-- Add some photo gallery or a special message section --> 
   <div class="gallery"> <!-- --> 
   </div> <!-- Add interactive elements like balloons or confetti --> 
   <canvas id="balloonsCanvas"></canvas> <!-- For balloon animations --> 
  </div> 
  <script src="scripts.js"></script> <!-- Link to your JavaScript for animations --> 
 </body>
</html>
body {
    font-family: 'Arial', sans-serif;
    background-color: #f0e7d8;
    text-align: center;
    margin: 0;
    padding: 20px;
}

h1 {
    font-size: 3rem;
    color: #ff6f61;
}

.intro-text {
    font-size: 1.5rem;
    margin-bottom: 20px;
}

.container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    background: #fff;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.countdown {
    margin-top: 20px;
}

.gallery {
    margin-top: 30px;
}

/* Add some styling for animations here */
// Countdown Timer Script
const countdown = () => {
    const targetDate = new Date('YYYY-MM-DD HH:MM:SS').getTime(); // Replace with her birthday time
    const now = new Date().getTime();
    const difference = targetDate - now;

    const days = Math.floor(difference / (1000 * 60 * 60 * 24));
    const hours = Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const minutes = Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60));
    const seconds = Math.floor((difference % (1000 * 60)) / 1000);

    document.getElementById('timer').innerHTML = `${days}d ${hours}h ${minutes}m ${seconds}s`;

    if (difference < 0) {
        clearInterval(interval);
        document.getElementById('timer').innerHTML = "It's your special moment!";
    }
};

const interval = setInterval(countdown, 1000);
