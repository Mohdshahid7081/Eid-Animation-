<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Eid Mubarak</title>

<style>

body{
margin:0;
padding:0;
height:100vh;
display:flex;
justify-content:center;
align-items:center;
text-align:center;
font-family:Arial;
overflow:hidden;
color:white;

background:url('https://pin.it/oYbSYDVz7');
background-size:cover;
background-position:center;
background-repeat:no-repeat;
}

.overlay{
background:rgba(0,0,0,0.25);
width:100%;
height:100%;
display:flex;
justify-content:center;
align-items:center;
flex-direction:column;
}

h1{
font-size:55px;
color:gold;
text-shadow:0 0 20px gold;
margin:0;
}

p{
font-size:30px;
font-style:italic;
text-shadow:0 0 10px black;
margin-top:20px;
}

#userName{
font-size:38px;
margin-top:20px;
font-weight:bold;
text-shadow:0 0 10px black;
color:white;
}

input{
padding:12px;
width:220px;
border:none;
border-radius:25px;
font-size:18px;
text-align:center;
outline:none;
margin-top:25px;
}

button{
margin-top:20px;
padding:14px 28px;
border:none;
border-radius:35px;
background:#25D366;
color:white;
font-size:20px;
cursor:pointer;
box-shadow:0 0 20px #25D366;
}

.watermark{
position:fixed;
bottom:10px;
right:15px;
font-size:22px;
color:white;
opacity:0.8;
font-style:italic;
}

</style>
</head>

<body>

<body>

<div class="overlay">

<h1>Eid Mubarak 🌙</h1>

<p>May Allah bless you and your family</p>

<div id="userName"></div>

<input type="text" id="nameInput" placeholder="Naam Likho">

<button onclick="shareWish()">
Share on WhatsApp
</button>

</div>

<div class="watermark">
@itz.dark.soul2026
</div>



<script>

const params = new URLSearchParams(window.location.search);
const name = params.get("name");

if(name){
document.getElementById("userName").innerHTML =
"✨ Eid Mubarak " + name +" ✨";
}

function shareWish(){

let user =
document.getElementById("nameInput").value;

if(user==""){
alert("Naam likho 😊");
return;
}

let url =
window.location.origin +
window.location.pathname +
"?name=" + encodeURIComponent(user);

let text =
"🌙 Eid Mubarak 🌙\n" +
"Open this greeting 👇\n" +
url;

window.open(
"https://wa.me/?text=" +
encodeURIComponent(text),
"_blank"
);

}

</script>

</body>
</html>
