# waseemmahnoor7606.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy 20th Birthday Hazeem!</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

body{
background:linear-gradient(135deg,#a7d8ff,#ffffff,#ffb3c1);
overflow-x:hidden;
color:#1e3a5f;
}

section{
min-height:100vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
padding:40px 20px;
text-align:center;
}

.hero{
position:relative;
}

.hero h1{
font-size:4rem;
margin-bottom:10px;
}

.hero h2{
font-size:2rem;
font-weight:400;
margin-bottom:25px;
}

.hero button{
padding:15px 35px;
border:none;
border-radius:40px;
background:#ff8fa3;
color:white;
font-size:1.1rem;
cursor:pointer;
transition:.3s;
}

.hero button:hover{
transform:scale(1.08);
}

.web{
position:absolute;
width:200px;
opacity:.25;
}

.web.left{
left:0;
top:0;
}

.web.right{
right:0;
top:0;
transform:scaleX(-1);
}

.gallery-title{
font-size:3rem;
margin-bottom:40px;
}

.gallery{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
width:90%;
max-width:1000px;
}

.gallery img{
width:100%;
height:300px;
object-fit:cover;
border-radius:20px;
box-shadow:0 8px 20px rgba(0,0,0,.15);
transition:.4s;
}

.gallery img:hover{
transform:scale(1.05);
}

.note-box{
background:white;
padding:30px;
border-radius:25px;
max-width:800px;
width:90%;
box-shadow:0 10px 25px rgba(0,0,0,.1);
}

.note-box h2{
margin-bottom:20px;
}

.note{
border:2px dashed #a7d8ff;
padding:20px;
border-radius:15px;
min-height:250px;
text-align:left;
line-height:1.8;
}

.final h1{
font-size:3.5rem;
margin-bottom:20px;
}

.final p{
font-size:1.2rem;
max-width:700px;
}

.floating{
position:fixed;
pointer-events:none;
font-size:24px;
animation:floatUp linear forwards;
}

@keyframes floatUp{
0%{
transform:translateY(100vh);
opacity:1;
}
100%{
transform:translateY(-120vh);
opacity:0;
}
}

.spider{
font-size:60px;
animation:swing 3s ease-in-out infinite;
transform-origin:top center;
}

@keyframes swing{
0%{transform:rotate(12deg);}
50%{transform:rotate(-12deg);}
100%{transform:rotate(12deg);}
}

.music-btn{
margin-top:20px;
padding:12px 25px;
border:none;
background:#a7d8ff;
border-radius:30px;
cursor:pointer;
}

@media(max-width:768px){
.hero h1{
font-size:2.6rem;
}
.hero h2{
font-size:1.4rem;
}
}
</style>
</head>

<body>

<section class="hero">
<div class="web left">🕸️</div>
<div class="web right">🕸️</div>

<div class="spider">🕷️</div>

<h1>Happy 20th Birthday</h1>
<h2>Hazeem 🎂</h2>

<p style="max-width:650px;margin-bottom:25px;">
Welcome to your little birthday surprise.
A collection of memories, wishes and smiles created just for you.
</p>

<button onclick="startSurprise()">
Open Your Surprise
</button>

<br>

<button class="music-btn" onclick="toggleMusic()">
🎵 Play Music
</button>

<audio id="music" loop>
<source src="until-i-found-you.mp3" type="audio/mpeg">
</audio>
</section>

<section>
<h1 class="gallery-title">📸 Our Memories</h1>

<div class="gallery">
<img src="photo1.jpg" alt="">
<img src="photo2.jpg" alt="">
<img src="photo3.jpg" alt="">
<img src="photo4.jpg" alt="">
</div>
</section>

<section>
<div class="note-box">
<h2>💌 A Note For You</h2>

<div class="note" contenteditable="true">

Dear Hazeem,

Write your birthday message here...

You can edit this section directly and make it as long or as short as you'd like.

Happy 20th Birthday ❤️

</div>
</div>
</section>

<section class="final">
<div class="spider">🕷️</div>

<h1>Happy Birthday, Hazeem ❤️</h1>

<p>
May your 20th year bring amazing adventures,
great memories, endless laughter and all the happiness you deserve.

Thank you for being you.
</p>

<br><br>

<h2>🎂 20 Looks Good On You 🎂</h2>
</section>

<script>
function startSurprise(){
window.scrollTo({
top:window.innerHeight,
behavior:'smooth'
});
createConfetti();
}

function toggleMusic(){
const music=document.getElementById('music');

if(music.paused){
music.play();
}
else{
music.pause();
}
}

function createConfetti(){

for(let i=0;i<40;i++){

let item=document.createElement('div');

item.className='floating';

const symbols=['🕷️','⭐','❤️','🎉','✨'];

item.innerHTML=symbols[Math.floor(Math.random()*symbols.length)];

item.style.left=Math.random()*100+'vw';

item.style.animationDuration=
(Math.random()*4+4)+'s';

document.body.appendChild(item);

setTimeout(()=>{
item.remove();
},8000);
}
}

setInterval(createConfetti,6000);
</script>

</body>
</html>
