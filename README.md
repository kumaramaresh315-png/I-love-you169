<div id="lockScreen" style="
position:fixed;inset:0;
background:linear-gradient(135deg,#ff4b6e,#ff85a2);
display:flex;align-items:center;justify-content:center;
z-index:9999;color:white;text-align:center;
font-family:Poppins,sans-serif;">
  <div style="
  background:rgba(255,255,255,0.15);
  padding:30px;border-radius:20px;
  backdrop-filter:blur(10px);
  width:90%;max-width:350px;">
    <h1 style="font-family:'Playfair Display',serif;">For Navya ❤️</h1>
    <p>Enter the password to unlock my heart 💖</p>
    <input id="pass" type="password" placeholder="Password"
      style="padding:12px;width:100%;border:none;
      border-radius:30px;margin:15px 0;font-size:16px;">
    <button onclick="unlock()" style="
      padding:12px 30px;border:none;
      border-radius:30px;font-size:16px;
      background:white;color:#ff4b6e;cursor:pointer;">
      Unlock 🔐
    </button>
    <p style="font-size:12px;opacity:.8;margin-top:10px">
      Hint: Your Name ❤️
    </p>
  </div>
</div>
<script>
function unlock(){
  const p=document.getElementById("pass").value.toLowerCase();
  if(p==="navya"){
    document.getElementById("lockScreen").style.display="none";
  }else{
    alert("Wrong password 💔 Try again");
  }
}
</script>
<a href="https://wa.me/?text=Navya%20❤️%20This%20is%20something%20very%20special%20I%20made%20for%20you%20💖%20Open%20this%20link%20👇"
target="_blank"
style="
margin-top:20px;
display:inline-block;
padding:12px 28px;
border-radius:30px;
background:#25D366;
color:white;
text-decoration:none;
font-size:16px;
box-shadow:0 10px 25px rgba(0,0,0,.3);">
💌 Share on WhatsApp
</a>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Amaresh ❤️ Navya</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box}
body{
  font-family:'Poppins',sans-serif;
  background:linear-gradient(135deg,#ff4b6e,#ff85a2);
  color:#fff;
  overflow:hidden;
}
.slide{
  height:100vh;
  width:100%;
  display:flex;
  justify-content:center;
  align-items:center;
  flex-direction:column;
  text-align:center;
  position:absolute;
  top:0;left:0;
  transition:opacity 1s;
}
.hidden{opacity:0;pointer-events:none}
h1{
  font-family:'Playfair Display',serif;
  font-size:42px;
  margin-bottom:10px;
}
h2{font-size:24px;margin-bottom:20px}
p{
  max-width:700px;
  font-size:18px;
  line-height:1.8;
  margin:20px;
}
button{
  padding:14px 32px;
  font-size:18px;
  border:none;
  border-radius:50px;
  background:#fff;
  color:#ff4b6e;
  cursor:pointer;
  transition:0.3s;
}
button:hover{transform:scale(1.08)}
.heart{
  position:absolute;
  bottom:-20px;
  animation:float 6s linear infinite;
  opacity:0.7;
}
@keyframes float{
  0%{transform:translateY(0)}
  100%{transform:translateY(-120vh)}
}
.firework{
  position:absolute;
  width:6px;height:6px;
  background:#fff;
  border-radius:50%;
  animation:explode 1.5s ease-out forwards;
}
@keyframes explode{
  to{
    transform:translate(var(--x),var(--y));
    opacity:0;
  }
}
</style>
</head>

<body>

<!-- 🎵 Background Music -->
<audio autoplay loop>
  <source src="https://cdn.pixabay.com/audio/2023/02/28/audio_4b4c41b92f.mp3" type="audio/mpeg">
</audio>

<!-- Slide 1 -->
<div class="slide" id="s1">
  <h1>Navya ❤️</h1>
  <h2>This is for you</h2>
  <p>
    Sometimes life becomes beautiful without warning…  
    and then **you** happened.
  </p>
  <button onclick="next(1)">Begin ✨</button>
</div>

<!-- Slide 2 -->
<div class="slide hidden" id="s2">
  <h1>Dear Navya</h1>
  <p>
    From late-night talks to silent smiles,  
    from dreams to doubts —  
    every moment with you feels special.
  </p>
  <button onclick="next(2)">Next 💗</button>
</div>

<!-- Slide 3 -->
<div class="slide hidden" id="s3">
  <h1>My Feelings</h1>
  <p>
    You are my calm in chaos,  
    my strength in weakness,  
    my happiness without reason.  
    <br><br>
    Loving you feels natural… effortless… eternal.
  </p>
  <button onclick="next(3)">Continue 💕</button>
</div>

<!-- Slide 4 (Countdown) -->
<div class="slide hidden" id="s4">
  <h1>One Question…</h1>
  <h2 id="count">3</h2>
</div>

<!-- Slide 5 (Proposal) -->
<div class="slide hidden" id="s5">
  <h1>Navya 💍</h1>
  <p>
    Will you hold my hand,  
    walk with me through every season of life,  
    and be **mine forever**?
  </p>
  <button onclick="yes()">YES ❤️</button>
</div>

<!-- Slide 6 (Final) -->
<div class="slide hidden" id="s6">
  <h1>Forever Begins Now 💖</h1>
  <p>
    I promise to love you deeply,  
    respect you endlessly,  
    and choose you every single day.
  </p>
  <h2>— Amaresh Rai</h2>
</div>

<script>
let current=1;

function next(n){
  document.getElementById("s"+n).classList.add("hidden");
  document.getElementById("s"+(n+1)).classList.remove("hidden");
}

setTimeout(()=>countdown(),1000);
function countdown(){
  let c=3;
  let el=document.getElementById("count");
  let timer=setInterval(()=>{
    el.innerText=c;
    c--;
    if(c<0){
      clearInterval(timer);
      next(4);
    }
  },1000);
}

function yes(){
  next(5);
  fireworks();
}

function fireworks(){
  for(let i=0;i<120;i++){
    let f=document.createElement("div");
    f.className="firework";
    f.style.left=Math.random()*100+"vw";
    f.style.top=Math.random()*100+"vh";
    f.style.setProperty("--x",(Math.random()*300-150)+"px");
    f.style.setProperty("--y",(Math.random()*300-150)+"px");
    document.body.appendChild(f);
    setTimeout(()=>f.remove(),1500);
  }
}

// Floating hearts
setInterval(()=>{
  let h=document.createElement("div");
  h.className="heart";
  h.innerHTML="❤️";
  h.style.left=Math.random()*100+"vw";
  h.style.fontSize=Math.random()*20+20+"px";
  document.body.appendChild(h);
  setTimeout(()=>h.remove(),6000);
},250);
</script>

</body>
</html>
