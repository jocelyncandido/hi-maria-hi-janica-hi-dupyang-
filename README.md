<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Special Message</title>

<style>
body{
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    font-family:Arial;
    background: linear-gradient(270deg,#ff9a9e,#fad0c4,#fbc2eb,#a6c1ee);
    background-size:800% 800%;
    animation: gradientMove 10s ease infinite;
}

@keyframes gradientMove{
0%{background-position:0% 50%;}
50%{background-position:100% 50%;}
100%{background-position:0% 50%;}
}

.card{
    background:white;
    padding:40px;
    border-radius:20px;
    text-align:center;
    box-shadow:0 15px 35px rgba(0,0,0,0.2);
}

button{
    padding:15px 30px;
    font-size:18px;
    border:none;
    border-radius:10px;
    background:#ff4b5c;
    color:white;
    cursor:pointer;
    transition:0.3s;
}

button:hover{
    transform:scale(1.1);
}

#message{
    display:none;
    font-size:28px;
    margin-top:20px;
}
</style>
</head>

<body>

<div class="card">
<h1>Open this message 🎁</h1>

<button onclick="showMessage()">Click Me</button>

<div id="message">
✨ Hi Maria, Kang2, and Dupyo! 👋
</div>

</div>

<script>
function showMessage(){
    document.getElementById("message").style.display="block";

    // confetti
    for(let i=0;i<100;i++){
        let confetti=document.createElement("div");
        confetti.style.position="fixed";
        confetti.style.width="10px";
        confetti.style.height="10px";
        confetti.style.background="hsl("+Math.random()*360+"deg,100%,50%)";
        confetti.style.left=Math.random()*100+"vw";
        confetti.style.top="-10px";
        confetti.style.opacity="0.8";
        confetti.style.transform="rotate("+Math.random()*360+"deg)";
        confetti.style.transition="top 3s linear";
        document.body.appendChild(confetti);

        setTimeout(()=>{
            confetti.style.top="100vh";
        },10);
    }
}
</script>

</body>
</html>
