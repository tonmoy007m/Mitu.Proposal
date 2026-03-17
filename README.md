# Mitu.Proposal
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Mitu ❤️</title>

<style>
body{
    margin:0;
    padding:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    font-family:Arial, sans-serif;
    background:linear-gradient(135deg,#ff9a9e,#fad0c4);
    text-align:center;
}

h1{
    color:white;
    font-size:40px;
}

p{
    color:white;
    font-size:20px;
}

button{
    padding:15px 35px;
    font-size:20px;
    border:none;
    border-radius:12px;
    margin:15px;
    cursor:pointer;
}

#yes{
    background:#28a745;
    color:white;
}

#no{
    background:#ff4d4d;
    color:white;
    position:absolute;
}

.heart{
    position:fixed;
    color:red;
    animation:float 5s linear infinite;
}

@keyframes float{
    0%{transform:translateY(0);}
    100%{transform:translateY(-800px);}
}
</style>

</head>

<body>

<h1>Mitu, Will You Be Mine? ❤️</h1>
<p>I really like you. Will you be my girlfriend?</p>

<button id="yes" onclick="yes()">Yes 💖</button>
<button id="no" onmouseover="move()">No 😢</button>

<script>

function yes(){
document.body.innerHTML =
"<h1 style='color:white;margin-top:200px;font-size:45px;'>❤️ I Love You Mitu ❤️<br>You made me the happiest person alive!</h1>";
}

function move(){
let x=Math.random()*window.innerWidth;
let y=Math.random()*window.innerHeight;

document.getElementById("no").style.left=x+"px";
document.getElementById("no").style.top=y+"px";
}

function createHeart(){
let heart=document.createElement("div");
heart.className="heart";
heart.innerHTML="❤️";

heart.style.left=Math.random()*100+"vw";
heart.style.bottom="0";

document.body.appendChild(heart);

setTimeout(()=>{heart.remove();},5000);
}

setInterval(createHeart,500);

</script>

</body>
</html>
```
