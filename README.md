# CiberSegurança
Trabalho para bruxelas
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />

<title> CiberSegurança</title>
<link rel="icon" href="https://cdn-icons-png.flaticon.com/512/3064/3064197.png">

<link href="https://fonts.googleapis.com/css?family=Poppins" rel="stylesheet" />

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

/* FUNDO */
body{
min-height:100vh;
background:linear-gradient(to top,#3a86ff,#141E30);
display:flex;
justify-content:center;
align-items:center;
padding-top:80px;
}

/* ================= MENU ================= */

header{
position:fixed;
top:0;
width:100%;
z-index:999;
}

.navbar{
display:flex;
justify-content:space-between;
align-items:center;
padding:15px 40px;
background:rgba(47, 54, 160, 0.4);
backdrop-filter:blur(10px);
}

/* LOGO */
.logo{
display:flex;
align-items:center;
gap:10px;
color:white;
font-size:20px;
font-weight:600;
}

.logo img{
width:40px;
}

/* MENU LINKS */
.menu{
display:flex;
list-style:none;
gap:30px;
}

.menu a{
color:white;
text-decoration:none;
font-weight:500;
transition:0.3s;
}

.menu a:hover{
color:#00c6ff;
}

/* BOTÃO MENU */
.btn-menu{
padding:10px 25px;
background:#00c6ff;
border-radius:25px;
text-decoration:none;
color:black;
font-weight:600;
transition:0.3s;
}

.btn-menu:hover{
background:#009ac7;
}

/* HAMBURGER */
.hamburger{
display:none;
font-size:28px;
color:white;
cursor:pointer;
}

/* RESPONSIVO */
@media(max-width:768px){

.menu{
position:absolute;
top:70px;
left:0;
width:100%;
flex-direction:column;
background:#141E30;
text-align:center;
padding:20px 0;
display:none;
}

.menu.active{
display:flex;
}

.hamburger{
display:block;
}

.btn-menu{
display:none;
}

}

/* ================= CARD ================= */

.card{
position:relative;
width:700px;
height:500px;
border-radius:16px;
overflow:hidden;
box-shadow:0 5px 50px rgba(0,0,0,0.85);
background:url("https://proximonivel.claro.com.br/wp-content/uploads/2025/09/ciberseguranca-753x425.webp") no-repeat center / cover;
}

.card::before{
content:'';
position:absolute;
inset:0;
background-color:rgba(0,0,0,0.92);
z-index:1;
}

/* IMAGEM DIVIDIDA */
.img{
position:absolute;
inset:0;
display:flex;
z-index:2;
}

.img span{
width:25%;
height:100%;
background-image:url("https://tecnicomais.pt/wp-content/uploads/shutterstock_2137304159-1-scaled-1-1920x910.jpg");
background-size:400% 100%;
transition:0.5s;
}

.img span:nth-child(1){
background-position:0;
transition-delay:0s;
}

.img span:nth-child(2){
background-position:33.333%;
transition-delay:0.1s;
}

.img span:nth-child(3){
background-position:66.666%;
transition-delay:0.2s;
}

.img span:nth-child(4){
background-position:100%;
transition-delay:0.3s;
}

.card:hover .img span{
transform:translateY(-100%);
}

/* CONTEÚDO */
.content{
position:relative;
z-index:3;
width:100%;
height:100%;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
color:white;
padding:20px;
transform:translateY(100%);
transition:1s;
}

.card:hover .content{
transform:translateY(0%);
transition-delay:0.1s;
}

.content h2{
margin-bottom:8px;
font-size:32px;
}

.content p{
font-size:18px;
margin-bottom:20px;
}

/* BOTÃO CARD */
.btn-entrar{
padding:12px 30px;
background-color:#00c6ff;
color:#000;
font-weight:700;
border-radius:30px;
text-decoration:none;
transition:0.3s;
}

.btn-entrar:hover{
background-color:#00a1cc;
}

</style>
</head>

<body>

<!-- MENU -->
<header>
<nav class="navbar">

<div class="logo">

<img src="https://img.icons8.com/?size=100&id=OGGn5T3Iui1B&format=png&color=000000">
  <span>CiberSegurança</span>
</div>

<ul class="menu">

</ul>

<div class="hamburger" onclick="toggleMenu()">☰</div>

</nav>
</header>

<!-- CARD -->
<div class="card">

<div class="img">
<span></span>
<span></span>
<span></span>
<span></span>
</div>

<div class="content">
<h2>CiberSegurança</h2>
<p>Entrar na aplicação</p>
<a href="LOGIN.html" class="btn-entrar">Login</a>
</div>

</div>

<script>
function toggleMenu(){
document.querySelector(".menu").classList.toggle("active");
}
</script>

</body>
</html>
