# Raza-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Hassan.com</title>

<style>
*{box-sizing:border-box}

body{
margin:0;
font-family:Arial,sans-serif;
background:#f5f7fb;
color:#172033
}

nav{
position:sticky;
top:0;
background:#fff;
padding:16px 6%;
display:flex;
justify-content:space-between;
align-items:center;
box-shadow:0 2px 12px #0001;
z-index:10
}

.logo{
font-size:24px;
font-weight:800
}

nav a{
margin-left:15px;
text-decoration:none;
color:#172033
}

.hero{
padding:90px 7%;
text-align:center;
background:linear-gradient(135deg,#eef2ff,#fff)
}

.hero h1{
font-size:clamp(42px,8vw,76px);
margin:15px 0
}

.hero h1 span{
color:#315efb
}

.hero p{
max-width:720px;
margin:auto;
color:#596274;
font-size:19px;
line-height:1.7
}

.btn{
display:inline-block;
margin:20px 5px 0;
padding:13px 22px;
border-radius:10px;
text-decoration:none;
font-weight:bold;
border:0;
cursor:pointer
}

.primary{
background:#315efb;
color:#fff
}

.light{
background:#fff;
color:#172033;
border:1px solid #ddd
}

section{
padding:60px 7%;
text-align:center
}

h2{
font-size:34px
}

.muted{
color:#667085
}

.grid{
display:flex;
gap:20px;
justify-content:center;
flex-wrap:wrap
}

.card{
background:#fff;
border:1px solid #e4e7ef;
border-radius:16px;
padding:25px;
width:280px;
box-shadow:0 5px 20px #00000009
}

footer{
padding:28px;
text-align:center;
color:#697386;
background:#fff
}

.wa{
position:fixed;
right:20px;
bottom:20px;
background:#20a35a;
color:#fff;
padding:14px 18px;
border-radius:30px;
text-decoration:none;
font-weight:bold;
z-index:20
}


/* ADMIN PANEL */

#admin{
display:none;
min-height:100vh;
background:#eef1f7;
padding:25px
}

#login{
max-width:420px;
margin:70px auto;
background:#fff;
padding:28px;
border-radius:16px;
box-shadow:0 5px 25px #0002
}

#panel{
max-width:900px;
margin:auto;
background:#fff;
padding:28px;
border-radius:16px
}

input,
textarea{
width:100%;
padding:12px;
margin:7px 0 15px;
border:1px solid #d9deea;
border-radius:9px;
font:inherit
}

textarea{
min-height:90px
}

.adminitem{
border:1px solid #e1e5ed;
padding:15px;
border-radius:12px;
margin:10px 0
}

.hidden{
display:none
}

.top{
display:flex;
justify-content:space-between;
align-items:center;
gap:10px;
flex-wrap:wrap
}

.danger{
background:#c62828;
color:#fff
}

.small{
padding:9px 13px;
margin:3px
}

@media(max-width:600px){

nav{
padding:14px 4%
}

nav div:last-child{
display:none
}

.hero{
padding:65px 20px
}

section{
padding:45px 20px
}

}
</style>
</head>

<body>


<!-- ================= PUBLIC WEBSITE ================= -->

<div id="site">

<nav>

<div class="logo" id="siteName">
Hassan.com
</div>

<div>

<a href="#home">Home</a>

<a href="#about">About</a>

<a href="#services">Services</a>

<a href="#projects">Projects</a>

<a href="#contact">Contact</a>

</div>

</nav>


<header id="home" class="hero">

<p class="muted" id="tagline">
Welcome to my website
</p>

<h1>
Hi, I'm <span id="owner">Hassan</span>
</h1>

<p id="intro">
Welcome to Hassan.com. This is my personal website where I can share my work, services and projects.
</p>

<a class="btn primary" href="#services">
View Services
</a>

<a class="btn light" href="#contact">
Contact Me
</a>

</header>


<section id="about">

<h2>
About Me
</h2>

<p class="muted" id="aboutText">
I am learning web development and building my own projects step by step.
</p>

</section>


<section id="services">

<h2>
Services
</h2>

<div class="grid" id="servicesGrid"></div>

</section>


<section id="projects">

<h2>
Projects
</h2>

<div class="grid" id="projectsGrid"></div>

</section>


<section id="contact">

<h2>
Contact
</h2>

<p class="muted">
Email:
<span id="email">
your@email.com
</span>
</p>

<a class="btn primary"
id="emailBtn"
href="mailto:your@email.com">

Email Me

</a>

</section>


<a class="wa"
id="waBtn"
href="#"
target="_blank">

WhatsApp

</a>


<footer>

© <span id="year"></span>

<span id="footerName">
Hassan.com
</span>

</footer>

</div>



<!-- ================= ADMIN PANEL ================= -->

<div id="admin">


<div id="login">

<h2>
🔐 Hassan.com Admin
</h2>

<p class="muted">
Login to edit your website.
</p>


<input
id="loginUser"
placeholder="Username"
>


<input
id="loginPass"
type="password"
placeholder="Password"
>


<button
class="btn primary"
onclick="login()">

Login

</button>


<p
id="loginError"
style="color:#c62828">

</p>

</div>



<div id="panel" class="hidden">


<div class="top">

<h1>
Admin Panel
</h1>

<button
class="btn danger"
onclick="logout()">

Logout

</button>

</div>


<h2>
Website Information
</h2>


<label>
Website Name
</label>

<input id="aSiteName">


<label>
Your Name
</label>

<input id="aOwner">


<label>
Tagline
</label>

<input id="aTagline">


<label>
Home Introduction
</label>

<textarea id="aIntro"></textarea>


<label>
About Me
</label>

<textarea id="aAbout"></textarea>


<label>
Email
</label>

<input id="aEmail">


<label>
WhatsApp Number
</label>

<input
id="aWhatsapp"
placeholder="923001234567"
>



<h2>
Services
</h2>

<div id="aServices"></div>


<button
class="btn light"
onclick="addService()">

+ Add Service

</button>



<h2>
Projects
</h2>

<div id="aProjects"></div>


<button
class="btn light"
onclick="addProject()">

+ Add Project

</button>


<br>
<br>


<button
class="btn primary"
onclick="save()">

💾 Save All Changes

</button>


<button
class="btn light"
onclick="showSite()">

🌐 View Website

</button>


</div>

</div>



<script>


/* ================= DEFAULT DATA ================= */

const DEFAULT={

siteName:"Hassan.com",

owner:"Hassan",

tagline:"Welcome to my website",

intro:
"Welcome to Hassan.com. This is my personal website where I can share my work, services and projects.",

about:
"I am learning web development and building my own projects step by step.",

email:
"your@email.com",

whatsapp:"",

services:[

[
"💻",
"Web Development",
"Website creation and development."
],

[
"📊",
"Data Entry",
"Typing and data entry services."
],

[
"🎨",
"Design",
"Simple modern website designs."
]

],

projects:[

[
"🚀",
"My Website",
"Hassan.com personal website."
],

[
"📱",
"My Project",
"More projects will be added here."
]

]

};



/* LOAD SAVED DATA */

let data=
JSON.parse(
localStorage.getItem("hassanData")
||"null"
)||DEFAULT;



/* ================= WEBSITE ================= */

function render(){

document.getElementById("siteName").textContent=
data.siteName;

document.getElementById("footerName").textContent=
data.siteName;

document.getElementById("owner").textContent=
data.owner;

document.getElementById("tagline").textContent=
data.tagline;

document.getElementById("intro").textContent=
data.intro;

document.getElementById("aboutText").textContent=
data.about;

document.getElementById("email").textContent=
data.email;

document.getElementById("emailBtn").href=
"mailto:"+data.email;

document.getElementById("year").textContent=
new Date().getFullYear();



document.getElementById("servicesGrid").innerHTML=

data.services.map(function(x){

return `

<div class="card">

<h3>
${x[0]} ${x[1]}
</h3>

<p class="muted">
${x[2]}
</p>

</div>

`;

}).join("");



document.getElementById("projectsGrid").innerHTML=

data.projects.map(function(x){

return `

<div class="card">

<h3>
${x[0]} ${x[1]}
</h3>

<p class="muted">
${x[2]}
</p>

</div>

`;

}).join("");



let n=
data.whatsapp.replace(/\D/g,"");

document.getElementById("waBtn").href=
n
?
"https://wa.me/"+n
:"#";

}



/* ================= ADMIN OPEN ================= */

function openAdmin(){

document.getElementById("site").style.display=
"none";

document.getElementById("admin").style.display=
"block";

window.scrollTo(0,0);

}



/* ================= WEBSITE OPEN ================= */

function showSite(){

document.getElementById("admin").style.display=
"none";

document.getElementById("site").style.display=
"block";

render();

window.scrollTo(0,0);

}



/* ================= LOGIN ================= */

function login(){

let u=
document.getElementById("loginUser").value;

let p=
document.getElementById("loginPass").value;


/*
CHANGE THESE TWO VALUES
BEFORE PUBLISHING
*/

if(
u==="admin"
&&
p==="12345"
){

document.getElementById("login").style.display=
"none";

document
.getElementById("panel")
.classList
.remove("hidden");

loadAdmin();

}

else{

document.getElementById("loginError").textContent=
"Wrong username or password.";

}

}



/* ================= LOGOUT ================= */

function logout(){

showSite();

}



/* ================= LOAD ADMIN ================= */

function loadAdmin(){

document.getElementById("aSiteName").value=
data.siteName;

document.getElementById("aOwner").value=
data.owner;

document.getElementById("aTagline").value=
data.tagline;

document.getElementById("aIntro").value=
data.intro;

document.getElementById("aAbout").value=
data.about;

document.getElementById("aEmail").value=
data.email;

document.getElementById("aWhatsapp").value=
data.whatsapp;



drawAdmin(
"aServices",
data.services,
"Service"
);


drawAdmin(
"aProjects",
data.projects,
"Project"
);

}



/* ================= DRAW SERVICES ================= */

function drawAdmin(
id,
arr,
label
){

document.getElementById(id).innerHTML=

arr.map(function(x,i){

return `

<div class="adminitem">

<input
data-type="${id}"
data-i="${i}"
data-k="0"
value="${x[0]}"
placeholder="Icon"
>


<input
data-type="${id}"
data-i="${i}"
data-k="1"
value="${x[1]}"
placeholder="${label} name"
>


<textarea
data-type="${id}"
data-i="${i}"
data-k="2"
placeholder="Description"
>${x[2]}</textarea>


<button
class="btn danger small"
onclick="this.parentElement.remove()">

Remove

</button>

</div>

`;

}).join("");

}



/* ================= COLLECT DATA ================= 
function collect(id){

let out=[];

document
.querySelectorAll(
`[data-type="${id}"]`
)
.forEach(function(e){

let i=
+e.dataset.i;

let k=
+e.dataset.k;

