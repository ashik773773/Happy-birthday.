<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Happy Birthday Cutie Pie 🎂</title>
<style>
body {
  margin:0;
  background: linear-gradient(to top, #ffdde1, #ee9ca7);
  text-align:center;
  font-family: 'Comic Sans MS', cursive;
  overflow:hidden;
}

h1 {
  margin-top:40px;
  color:white;
  font-size:40px;
}

#cake {
  font-size:120px;
  cursor:pointer;
  margin-top:50px;
  transition: transform 0.5s ease;
}

#message {
  display:none;
  margin-top:30px;
  font-size:22px;
  color:white;
  padding:20px;
}

.sparkle {
  position:absolute;
  width:10px;
  height:10px;
  background:pink;
  border-radius:50%;
  animation: explode 1s forwards;
}

@keyframes explode {
  to {
    transform: translate(var(--x), var(--y));
    opacity:0;
  }
}
</style>
</head>

<body>

<h1>Happy Birthday Cutie Pie 🎉💖</h1>

<div id="cake">🎂🕯️🕯️🕯️</div>
<p style="color:white;">Tap the cake to blow the candles 💕</p>

<div id="message">
💌 Dear Mansura Diba 💕<br><br>
From the moment you came into my life, everything feels brighter and warmer.  
Even though miles separate us, my heart celebrates you every single day.  

You are not just my girlfriend —  
You are my happiness, my calm, my favorite notification,  
and my sweetest dream.  

On your 16th birthday,  
I pray your smile never fades and your dreams come true.  

No distance can ever reduce what I feel for you.  
You will always be my Cutie Pie 💖✨  

Happy Birthday My Love 🎂🌸
</div>

<audio id="song" autoplay>
  <source src="https://www2.cs.uic.edu/~i101/SoundFiles/HappyBirthday.mid" type="audio/midi">
</audio>

<script>
const cake = document.getElementById("cake");
const message = document.getElementById("message");

cake.addEventListener("click", function() {
  cake.innerHTML = "🎂";
  cake.style.transform = "scale(1.2)";

  for(let i=0;i<40;i++){
    let sparkle = document.createElement("div");
    sparkle.className="sparkle";
    sparkle.style.left = "50%";
    sparkle.style.top = "50%";
    sparkle.style.setProperty('--x', (Math.random()*400-200)+"px");
    sparkle.style.setProperty('--y', (Math.random()*400-200)+"px");
    document.body.appendChild(sparkle);

    setTimeout(()=> sparkle.remove(),1000);
  }

  setTimeout(()=>{
    message.style.display="block";
  },800);
});
</script>

</body>
</html>
