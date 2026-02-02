# Happy-valentines-baby
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Will You Be My Valentine ❤️</title>

<style>
body {
    margin: 0;
    height: 100vh;
    background: linear-gradient(135deg, #ff6a88, #ff99ac);
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: Arial, sans-serif;
    color: white;
    text-align: center;
    overflow: hidden;
}

.card {
    background: rgba(255,255,255,0.18);
    padding: 35px;
    border-radius: 25px;
    backdrop-filter: blur(10px);
    box-shadow: 0 15px 35px rgba(0,0,0,0.3);
    max-width: 360px;
}

h1 {
    font-size: 32px;
    margin-bottom: 10px;
}

p {
    font-size: 18px;
    margin-bottom: 15px;
}

#countdown {
    font-size: 22px;
    margin: 20px 0;
    font-weight: bold;
}

button {
    padding: 14px 26px;
    font-size: 18px;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    margin: 10px;
}

.yes {
    background: #ff2e63;
    color: white;
}

.no {
    background: #222;
    color: white;
    position: absolute;
}

.heart {
    position: absolute;
    font-size: 22px;
    animation: float 6s linear infinite;
}

@keyframes float {
    0% { transform: translateY(0); }
    100% { transform: translateY(-100vh); }
}
</style>
</head>

<body>

<!-- 🎶 Background Song: Without You – Prem Dhillon -->
<iframe width="0" height="0"
src="https://www.youtube.com/embed/3Z9p0nJ8b9w?autoplay=1&loop=1&playlist=3Z9p0nJ8b9w"
allow="autoplay">
</iframe>

<div class="card">
    <h1>Khush Karan 💖</h1>
    <p>Will you be my Valentine? 🥺❤️</p>

    <div id="countdown">Loading countdown…</div>

    <button class="yes" onclick="yesClick()">YES ❤️😍</button>
    <button class="no" id="noBtn">NO 🙈</button>
</div>

<script>
// ⏳ Countdown to Valentine (14 Feb)
const valentineDate = new Date("February 14, 2026 00:00:00").getTime();

setInterval(() => {
    const now = new Date().getTime();
    const distance = valentineDate - now;

    const days = Math.floor(distance / (1000 * 60 * 60 * 24));
    const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));

    document.getElementById("countdown").innerHTML =
        `${days} Days 💕 ${hours} Hrs ⏳ ${minutes} Min ❤️`;
}, 1000);

// YES click
function yesClick() {
    document.body.innerHTML = `
        <h1 style="font-size:40px;">I Love You Khush Karan 😘❤️</h1>
        <p style="font-size:24px;">My forever Valentine 💍💖</p>
    `;
}

// NO button runs away 😄
const noBtn = document.getElementById("noBtn");
noBtn.addEventListener("mouseover", () => {
    noBtn.style.left = Math.random() * (window.innerWidth - 120) + "px";
    noBtn.style.top = Math.random() * (window.innerHeight - 60) + "px";
});

// 💕 Floating hearts
setInterval(() => {
    const heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "❤️💖💕💘";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.bottom = "0";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 6000);
}, 350);
</script>

</body>
</html>
