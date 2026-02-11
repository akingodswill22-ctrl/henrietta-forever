henrietta-forever<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Henrietta 💖</title>

<style>
body {
    text-align: center;
    font-family: Arial, sans-serif;
    background: linear-gradient(to right, #ffdde1, #ff758c);
    margin-top: 100px;
    overflow: hidden;
}

h1 {
    font-size: 2.8em;
    color: #fff;
}

h2 {
    color: #fff;
}

button {
    padding: 15px 40px;
    font-size: 20px;
    border: none;
    border-radius: 40px;
    cursor: pointer;
    margin: 15px;
    transition: 0.3s;
}

#yesBtn {
    background-color: #ff1e56;
    color: white;
}

#noBtn {
    background-color: gray;
    color: white;
}

#message {
    margin-top: 40px;
    font-size: 24px;
    color: white;
    display: none;
}

.from {
    position: fixed;
    bottom: 20px;
    width: 100%;
    font-size: 18px;
    color: white;
}

.heart {
    position: fixed;
    color: white;
    animation: float 4s linear infinite;
}

@keyframes float {
    0% { transform: translateY(0); opacity: 1; }
    100% { transform: translateY(-700px); opacity: 0; }
}
</style>
</head>
<body>

<h1>Henrietta 💕</h1>
<h2>Will You Be My Valentine? ❤️</h2>

<button id="yesBtn" onclick="acceptLove()">Yes 💖</button>
<button id="noBtn" onclick="removeNo()">No 😢</button>

<div id="message"></div>

<div class="from">Forever yours, Akin 💌</div>

<script>

let size = 20;
setInterval(function(){
    size += 2;
    document.getElementById("yesBtn").style.fontSize = size + "px";
}, 1000);

function removeNo() {
    document.getElementById("noBtn").style.display = "none";
}

function acceptLove() {

    let messageBox = document.getElementById("message");
    messageBox.style.display = "block";
    messageBox.innerHTML = "Henrietta 🥰❤️<br><br>You’ve made me the happiest man alive 💘<br><br>Will you marry me? 💍";

    createHearts();

    let phoneNumber = "234XXXXXXXXXX"; // Replace with your number
    let message = "Akin 💕 I said YES! I'm yours forever ❤️💍";
    let url = "https://wa.me/" + phoneNumber + "?text=" + encodeURIComponent(message);

    setTimeout(function() {
        window.open(url, "_blank");
    }, 3000);
}

function createHearts() {
    setInterval(function() {
        var heart = document.createElement("div");
        heart.className = "heart";
        heart.innerHTML = "💖";
        heart.style.left = Math.random() * window.innerWidth + "px";
        heart.style.bottom = "0px";
        heart.style.fontSize = (Math.random() * 30 + 20) + "px";
        document.body.appendChild(heart);

        setTimeout(function() {
            heart.remove();
        }, 4000);
    }, 200);
}

</script>

</body>
</html>
