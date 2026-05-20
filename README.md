# Vishnu ❤️ Sindhu Wedding Invitation Website Script

Save this as `index.html` and open it in any browser.
You can upload it free using GitHub Pages, Netlify, or Vercel.

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vishnu ❤️ Sindhu Wedding Invitation</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Great+Vibes&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:'Poppins',sans-serif;
    background:#fff8f5;
    color:#333;
    overflow-x:hidden;
}

.hero{
    height:100vh;
    background:linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)),
    url('https://images.unsplash.com/photo-1511285560929-80b456fea0bc?q=80&w=1600&auto=format&fit=crop');
    background-size:cover;
    background-position:center;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    color:white;
    animation:fadeIn 2s ease;
}

.hero-content h1{
    font-family:'Great Vibes',cursive;
    font-size:90px;
    margin-bottom:20px;
}

.hero-content p{
    font-size:22px;
    margin-bottom:10px;
}

.btn{
    display:inline-block;
    margin-top:20px;
    padding:14px 30px;
    background:#d4af37;
    color:white;
    text-decoration:none;
    border-radius:30px;
    transition:0.3s;
}

.btn:hover{
    background:#b68d20;
}

section{
    padding:80px 20px;
    text-align:center;
}

.section-title{
    font-size:42px;
    margin-bottom:20px;
    color:#b68d20;
    font-family:'Great Vibes',cursive;
}

.details p,
.love-story p,
.rsvp p{
    font-size:18px;
    line-height:1.8;
    max-width:800px;
    margin:auto;
}

.countdown{
    display:flex;
    justify-content:center;
    gap:20px;
    flex-wrap:wrap;
    margin-top:30px;
}

.count-box{
    background:white;
    padding:20px;
    border-radius:20px;
    min-width:120px;
    box-shadow:0 5px 15px rgba(0,0,0,0.1);
}

.count-box h2{
    font-size:40px;
    color:#d4af37;
}

.gallery{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:20px;
    margin-top:40px;
}

.gallery img{
    width:100%;
    height:320px;
    object-fit:cover;
    border-radius:20px;
    box-shadow:0 5px 15px rgba(0,0,0,0.15);
}

footer{
    background:#111;
    color:white;
    text-align:center;
    padding:30px 20px;
}

.music-btn{
    position:fixed;
    bottom:20px;
    right:20px;
    background:#d4af37;
    color:white;
    border:none;
    width:60px;
    height:60px;
    border-radius:50%;
    font-size:24px;
    cursor:pointer;
    box-shadow:0 5px 15px rgba(0,0,0,0.3);
}

@keyframes fadeIn{
    from{opacity:0;}
    to{opacity:1;}
}

@media(max-width:768px){
.hero-content h1{
    font-size:60px;
}
}
</style>
</head>
<body>

<!-- Background Music -->
<audio id="bgMusic" loop>
    <source src="YOUR_MUSIC_LINK.mp3" type="audio/mp3">
</audio>

<button class="music-btn" onclick="toggleMusic()">🎵</button>

<!-- Hero Section -->
<div class="hero">
    <div class="hero-content">
        <p>Together with their families</p>
        <h1>Vishnu ❤️ Sindhu</h1>
        <p>Invite you to celebrate their wedding</p>
        <a href="#details" class="btn">Open Invitation</a>
    </div>
</div>

<!-- Wedding Details -->
<section id="details" class="details">
    <h2 class="section-title">Wedding Details</h2>

    <p>
        With joyful hearts and the blessings of our families,<br>
        we invite you to join us as we begin our forever journey together.
    </p>

    <br><br>

    <p>
        📅 <strong>Date:</strong> 18 June 2026<br>
        ⏰ <strong>Time:</strong> Morning Muhurtham<br>
        📍 <strong>Venue:</strong> Mahalingam Farms
    </p>

    <br>

    <a class="btn" target="_blank"
    href="https://www.google.com/maps/place/Mahalingam+farms/@12.1562251,78.2722621,851m/data=!3m2!1e3!4b1!4m6!3m5!1s0x3bac1572566927e9:0xe5796517d1003a06!8m2!3d12.1562251!4d78.274837!16s%2Fg%2F11k3q0sj5z?entry=ttu&g_ep=EgoyMDI2MDUxMy4wIKXMDSoASAFQAw%3D%3D">
    View Location
    </a>
</section>

<!-- Countdown -->
<section>
    <h2 class="section-title">Countdown To Wedding</h2>

    <div class="countdown">
        <div class="count-box">
            <h2 id="days">0</h2>
            <p>Days</p>
        </div>

        <div class="count-box">
            <h2 id="hours">0</h2>
            <p>Hours</p>
        </div>

        <div class="count-box">
            <h2 id="minutes">0</h2>
            <p>Minutes</p>
        </div>

        <div class="count-box">
            <h2 id="seconds">0</h2>
            <p>Seconds</p>
        </div>
    </div>
</section>

<!-- Love Story -->
<section class="love-story">
    <h2 class="section-title">Our Love Story</h2>

    <p>
        Every love story is beautiful,
        but ours is our favorite.

        What started with smiles and conversations
        slowly became a beautiful forever.

        Now together with our families,
        we invite you to celebrate our new beginning.
    </p>
</section>

<!-- Gallery -->
<section>
    <h2 class="section-title">Gallery</h2>

    <div class="gallery">
        <img src="https://images.unsplash.com/photo-1522673607200-164d1b6ce486?q=80&w=1200&auto=format&fit=crop" alt="Couple Photo">

        <img src="https://images.unsplash.com/photo-1519741497674-611481863552?q=80&w=1200&auto=format&fit=crop" alt="Couple Photo">

        <img src="https://images.unsplash.com/photo-1515934751635-c81c6bc9a2d8?q=80&w=1200&auto=format&fit=crop" alt="Couple Photo">
    </div>
</section>

<!-- Reception -->
<section>
    <h2 class="section-title">Reception</h2>

    <p>
        Join us for an evening filled with
        joy, celebration, and togetherness.

        Reception Dinner
        on 18 June 2026
        at Mahalingam Farms.
    </p>
</section>

<!-- RSVP -->
<section class="rsvp">
    <h2 class="section-title">RSVP</h2>

    <p>
        Your presence is the greatest gift to us.
        Kindly confirm your attendance.
    </p>

    <br>

    <a class="btn" href="mailto:yourmail@gmail.com">
        Confirm Attendance
    </a>
</section>

<!-- Footer -->
<footer>
    <h2>Vishnu ❤️ Sindhu</h2>
    <p>18 June 2026 | Mahalingam Farms</p>
</footer>

<script>
// Countdown Timer
const weddingDate = new Date("June 18, 2026 06:00:00").getTime();

const timer = setInterval(function(){

const now = new Date().getTime();
const distance = weddingDate - now;

const days = Math.floor(distance / (1000 * 60 * 60 * 24));
const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
const seconds = Math.floor((distance % (1000 * 60)) / 1000);


document.getElementById("days").innerHTML = days;
document.getElementById("hours").innerHTML = hours;
document.getElementById("minutes").innerHTML = minutes;
document.getElementById("seconds").innerHTML = seconds;

if(distance < 0){
    clearInterval(timer);
}

},1000);

// Music Play/Pause
const music = document.getElementById('bgMusic');
let isPlaying = false;

function toggleMusic(){
    if(isPlaying){
        music.pause();
    } else {
        music.play();
    }
    isPlaying = !isPlaying;
}
</script>

</body>
</html>
```

## How To Use

1. Save as `index.html`
2. Add your own couple photos
3. Replace `YOUR_MUSIC_LINK.mp3` with your music file
4. Open in browser
5. Upload online using:

   * GitHub Pages
   * Netlify
   * Vercel

## Free Hosting Websites

* [https://pages.github.com](https://pages.github.com)
* [https://netlify.com](https://netlify.com)
* [https://vercel.com](https://vercel.com)
