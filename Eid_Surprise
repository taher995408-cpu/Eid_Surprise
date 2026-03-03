<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Eid Mubarak Surprise</title>

<style>
body {
    text-align: center;
    font-family: Arial, sans-serif;
    background: linear-gradient(to right, #0f2027, #203a43, #2c5364);
    color: white;
    padding: 40px;
    overflow-x: hidden;
}

/* 🌙 চাঁদ অ্যানিমেশন */
.moon {
    position: fixed;
    top: 50px;
    left: -100px;
    font-size: 60px;
    animation: moveMoon 20s linear infinite;
    opacity: 0.8;
}

@keyframes moveMoon {
    from { left: -100px; }
    to { left: 110%; }
}

button {
    padding: 12px 25px;
    font-size: 18px;
    background: gold;
    border: none;
    cursor: pointer;
    margin-top: 15px;
}

#message {
    margin-top: 25px;
    font-size: 22px;
}

/* ⏳ লোডিং স্পিনার */
.loader {
    border: 6px solid #f3f3f3;
    border-top: 6px solid gold;
    border-radius: 50%;
    width: 40px;
    height: 40px;
    margin: 20px auto;
    animation: spin 1s linear infinite;
    display: none;
}

@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

#countdown {
    font-size: 20px;
    margin-bottom: 20px;
    color: #ffd700;
}

.share-btn {
    display: inline-block;
    margin: 10px;
    padding: 10px 20px;
    background: #25D366;
    color: white;
    text-decoration: none;
    font-weight: bold;
}

.fb-btn {
    background: #1877F2;
}

.ad-box {
    margin-top: 40px;
    padding: 15px;
    background: rgba(255,255,255,0.1);
}
</style>

</head>
<body>

<div class="moon">🌙</div>

<h1>🌙 ঈদ মোবারক সারপ্রাইজ 🌙</h1>

<div id="countdown"></div>

<p>এই ঈদে তোমার জন্য একটি বিশেষ বার্তা অপেক্ষা করছে!</p>

<button onclick="showMessage()">সারপ্রাইজ দেখতে ক্লিক করুন</button>

<div class="loader" id="loader"></div>

<div id="message"></div>

<br>

<a class="share-btn" id="whatsappShare" target="_blank">
WhatsApp এ শেয়ার করুন
</a>

<a class="share-btn fb-btn" id="facebookShare" target="_blank">
Facebook এ শেয়ার করুন
</a>

<div class="ad-box">
    এখানে আপনার বিজ্ঞাপন দেখানো হবে
</div>

<script>

// ====== ঈদের তারিখ ======
var eidDate = new Date("March 31, 2026 00:00:00").getTime();

var countdownFunction = setInterval(function() {
    var now = new Date().getTime();
    var distance = eidDate - now;

    var days = Math.floor(distance / (1000 * 60 * 60 * 24));
    var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));

    document.getElementById("countdown").innerHTML =
    "ঈদ আসতে বাকি: " + days + " দিন " + hours + " ঘন্টা " + minutes + " মিনিট";

    if (distance < 0) {
        clearInterval(countdownFunction);
        document.getElementById("countdown").innerHTML = "🌙 ঈদ মোবারক 🌙";
    }
}, 1000);

// ====== সারপ্রাইজ মেসেজ + ২ সেকেন্ড suspense ======
function showMessage() {

    var loader = document.getElementById("loader");
    var messageDiv = document.getElementById("message");

    messageDiv.innerHTML = "";
    loader.style.display = "block";

    setTimeout(function() {

        var messages = [
            "🌙 এই ঈদ তোমার জীবনে শান্তি ও সুখ বয়ে আনুক।",
            "✨ তোমার স্বপ্নগুলো এই ঈদে আরও উজ্জ্বল হোক।",
            "💛 পরিবারে বরকত আর আনন্দে ভরে উঠুক এই ঈদ।",
            "🌸 নতুন আশা, নতুন আলো নিয়ে আসুক এই ঈদ।",
            "❤️ তোমার জীবনের প্রতিটি দিন হোক ঈদের মতো আনন্দময়।"
        ];

        var random = messages[Math.floor(Math.random() * messages.length)];

        loader.style.display = "none";
        messageDiv.innerHTML = random;

    }, 2000);
}

// ====== শেয়ার লিংক ======
var currentURL = window.location.href;
var shareText = "🌙 এই ঈদে তোমার সারপ্রাইজ দেখো এখানে: " + currentURL;

document.getElementById("whatsappShare").href =
"https://wa.me/?text=" + encodeURIComponent(shareText);

document.getElementById("facebookShare").href =
"https://www.facebook.com/sharer/sharer.php?u=" + encodeURIComponent(currentURL);

</script>

</body>
</html>
