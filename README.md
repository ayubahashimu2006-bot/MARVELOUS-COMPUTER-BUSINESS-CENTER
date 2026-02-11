# MARVELOUS-COMPUTER-BUSINESS-CENTER
Computer Center and Admin potal
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Marvelous Computer Center</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
:root{
  --bg:#f4f6f9;
  --text:#222;
  --card:#fff;
  --main:#0a3cff;
}
.dark{
  --bg:#0f172a;
  --text:#e5e7eb;
  --card:#1e293b;
}
body{
  margin:0;
  font-family:Arial,Helvetica,sans-serif;
  background:var(--bg);
  color:var(--text);
  transition:0.3s;
}
header{
  background:linear-gradient(135deg,#0a3cff,#0ccda3);
  color:#fff;
  padding:40px 20px;
  text-align:center;
}
nav{
  background:#0a2540;
  display:flex;
  justify-content:center;
  flex-wrap:wrap;
}
nav a{
  color:#fff;
  padding:14px 20px;
  text-decoration:none;
}
nav a:hover{background:#0ccda3;color:#000}
.toggle{
  position:fixed;
  top:15px;
  right:15px;
  padding:10px 15px;
  background:#000;
  color:#fff;
  cursor:pointer;
  border-radius:20px;
  font-size:14px;
}
section{
  max-width:1100px;
  margin:auto;
  padding:50px 20px;
}
h2{text-align:center;color:var(--main)}
.services{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
  gap:20px;
}
.card{
  background:var(--card);
  padding:20px;
  border-radius:10px;
  box-shadow:0 10px 25px rgba(0,0,0,0.1);
}
form{
  background:var(--card);
  padding:25px;
  border-radius:10px;
}
form input,form select,form button{
  width:100%;
  padding:12px;
  margin:10px 0;
}
form button{
  background:var(--main);
  color:#fff;
  border:none;
  cursor:pointer;
}
.reviews{overflow:hidden}
.slider{
  display:flex;
  gap:20px;
  animation:slide 20s linear infinite;
}
.review{
  min-width:300px;
  background:var(--card);
  padding:20px;
  border-left:5px solid #0ccda3;
  border-radius:8px;
}
@keyframes slide{
  0%{transform:translateX(0)}
  100%{transform:translateX(-50%)}
}
footer{
  background:#0a2540;
  color:#fff;
  text-align:center;
  padding:20px;
}
</style>
</head>

<body>

<div class="toggle" onclick="toggleDark()">🌙 Dark Mode</div>

<header>
<h1>MARVELOUS COMPUTER CENTER</h1>
<p>Learning Skills & Reliable Services<br><b>Where Knowledge Meets Technology</b></p>
</header>

<nav>
<a href="#services">Services</a>
<a href="#order">Order</a>
<a href="#reviews">Reviews</a>
<a href="#contact">Contact</a>
</nav>

<section id="services">
<h2>Our Services</h2>
<div class="services">
<div class="card"><b>Exam Services</b><br>WAEC, NECO, JAMB, Army Forms</div>
<div class="card"><b>Identity Services</b><br>NIN Slip, BVN Check & Print</div>
<div class="card"><b>Recharge & Data</b><br>VTU, Data Bundles</div>
<div class="card"><b>Office Work</b><br>Typing, Printing, Laminating</div>
</div>
</section>

<section id="order">
<h2>Service Request</h2>
<form onsubmit="sendWhatsApp(); return false;">
<input id="name" placeholder="Full Name" required>
<input id="phone" placeholder="Phone Number" required>
<select id="service">
<option>Select Service</option>
<option>NIN / BVN</option>
<option>Result Check</option>
<option>Recharge / Data</option>
<option>Office Work</option>
</select>
<button type="submit">Send via WhatsApp</button>
</form>
</section>

<section id="reviews">
<h2>Customer Reviews</h2>
<div class="reviews">
<div class="slider">
<div class="review">“Fast and trusted service. Always reliable.”</div>
<div class="review">“Very professional and affordable.”</div>
<div class="review">“Best computer center around here.”</div>
<div class="review">“Good customer care and clean work.”</div>
</div>
</div>
</section>

<section id="contact">
<h2>Contact</h2>
<p style="text-align:center">
📞 08083538664<br>
📧 marvelouscomputerbusinesscente@gmail.com
</p>
</section>

<footer>
© 2026 Marvelous Computer Center — All Rights Reserved
</footer>

<script>
function toggleDark(){
  document.body.classList.toggle("dark");
}
function sendWhatsApp(){
  let name=document.getElementById("name").value;
  let phone=document.getElementById("phone").value;
  let service=document.getElementById("service").value;
  let msg=`Hello, my name is ${name}. Phone: ${phone}. I need: ${service}`;
  window.open("https://wa.me/2348083538664?text="+encodeURIComponent(msg));
}
</script>

</body>
</html>
