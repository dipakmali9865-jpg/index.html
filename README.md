# index.html






<!DOCTYPE html>
<html>
<head>
<title>Paurnima Electricals</title>
<meta name="viewport" content="width=device-width,initial-scale=1">
<style>
*{box-sizing:border-box;font-family:Arial;margin:0;padding:0}
body{background:#f3f5f7}
header{background:#07518c;color:white;text-align:center;padding:18px}
nav{background:#222;text-align:center;padding:7px}
nav button{background:none;color:white;border:0;padding:7px;cursor:pointer}
.page{display:none;padding:25px;min-height:480px}
#home{display:block}
.box,.card,form{background:white;padding:18px;margin:10px auto;
border-radius:7px;box-shadow:0 2px 6px #bbb}
.cards{display:flex;flex-wrap:wrap;justify-content:center;gap:10px}
.card{width:260px;text-align:center}
input,select,textarea{width:100%;padding:9px;margin:5px 0}
textarea{height:70px}
.submit{width:100%;padding:10px;background:#07518c;color:white;border:0}
h2{text-align:center;color:#07518c;margin:15px}
footer{background:#222;color:white;text-align:center;padding:14px}
@media(max-width:600px){nav button{display:block;width:100%}.card{width:100%}}
</style>
</head>
<body>

<header>
<h1>⚡ Paurnima Electricals</h1>
<p>Motor Rewinding Shop</p>
</header>

<nav>
<button onclick="openPage('home')">🏠 Home</button>
<button onclick="openPage('reg')">📝 Registration</button>
<button onclick="openPage('login')">🔐 Login</button>
<button onclick="openPage('shop')">🏢 Shop</button>
<button onclick="openPage('motor')">⚙️ Motors</button>
<button onclick="openPage('service')">🔧 Services</button>
<button onclick="openPage('enq')">📋 Enquiry</button>
<button onclick="openPage('contact')">📞 Contact</button>
</nav>

<!-- HOME -->
<section id="home" class="page">
<h2>🏠 Welcome</h2>
<div class="box">
<h3>Paurnima Electricals and Motor Rewinding Shop</h3>
<p>Quality motor rewinding, repairing and electrical services.</p>
<p>Affordable Price | Fast Service | Customer Satisfaction</p>
</div>
<div class="cards">
<div class="card">🔧 Motor Rewinding</div>
<div class="card">⚙️ Motor Repairing</div>
<div class="card">💧 Pump Repairing</div>
</div>
</section>

<!-- REGISTRATION -->
<section id="reg" class="page">
<h2>📝 Registration</h2>
<form onsubmit="register(event)">
<input id="name" placeholder="Full Name" required>
<input id="mobile" placeholder="Mobile Number" required>
<input id="email" type="email" placeholder="Email" required>
<input id="user" placeholder="Username" required>
<input id="pass" type="password" placeholder="Password" required>
<input id="cpass" type="password" placeholder="Confirm Password" required>
<button class="submit">Register</button>
</form>
</section>

<!-- LOGIN -->
<section id="login" class="page">
<h2>🔐 Login</h2>
<form onsubmit="login(event)">
<input id="lu" placeholder="Username" required>
<input id="lp" type="password" placeholder="Password" required>
<button class="submit">Login</button>
<p>New User?
<button type="button" onclick="openPage('reg')">Register</button></p>
</form>
</section>

<!-- SHOP -->
<section id="shop" class="page">
<h2>🏢 Shop Information</h2>
<div class="box">
<h3>Paurnima Electricals and Motor Rewinding Shop</h3>
<p>Motor rewinding, repairing, pump repairing and maintenance.</p>
<p><b>Aim:</b> Reliable and quality electrical service.</p>
<p><b>Time:</b> Monday-Saturday, 9 AM-7 PM</p>
</div>
</section>

<!-- MOTORS -->
<section id="motor" class="page">
<h2>⚙️ Motor Details</h2>
<div class="cards">
<div class="card"><b>Single Phase Motor</b><p>Home use</p></div>
<div class="card"><b>Three Phase Motor</b><p>Industrial use</p></div>
<div class="card"><b>Submersible Motor</b><p>Water pumping</p></div>
<div class="card"><b>Water Pump Motor</b><p>Farm & Home</p></div>
<div class="card"><b>Industrial Motor</b><p>Heavy machines</p></div>
<div class="card"><b>Fan Motor</b><p>Repairing</p></div>
</div>
</section>

<!-- SERVICES -->
<section id="service" class="page">
<h2>🔧 Services</h2>
<div class="cards">
<div class="card">Motor Rewinding</div>
<div class="card">Motor Repairing</div>
<div class="card">Coil Rewinding</div>
<div class="card">Bearing Replacement</div>
<div class="card">Pump Repairing</div>
<div class="card">Motor Testing</div>
</div>
</section>

<!-- ENQUIRY -->
<section id="enq" class="page">
<h2>📋 Customer Enquiry</h2>
<form onsubmit="enquiry(event)">
<input id="cn" placeholder="Customer Name" required>
<input id="cm" placeholder="Mobile Number" required>
<select id="mt" required>
<option value="">Select Motor</option>
<option>Single Phase</option>
<option>Three Phase</option>
<option>Submersible</option>
<option>Water Pump</option>
<option>Industrial</option>
</select>
<textarea id="problem" placeholder="Motor Problem" required></textarea>
<button class="submit">Submit Enquiry</button>
</form>
</section>

<!-- CONTACT -->
<section id="contact" class="page">
<h2>📞 Contact Details</h2>
<div class="box">
<h3>Paurnima Electricals and Motor Rewinding Shop</h3>
<p>📞 Mobile: +91 9423224588</p>         
<p>📧 Email: paurnimaelectrical@gmail.com</p>
<p>📍 Address: Bhagwa chaufuli ,station road shindkheda </p>
<p>🕘 Time: 9 AM - 7 PM</p>
</div>
</section>

<footer>© 2026 Paurnima Electricals | SYBCA Project</footer>

<script>
function openPage(id){
document.querySelectorAll(".page").forEach(x=>x.style.display="none");
document.getElementById(id).style.display="block";
window.scrollTo(0,0);
}

function register(e){
e.preventDefault();
if(pass.value!=cpass.value){
alert("Password not match!");return;
}
let u={name:name.value,user:user.value,pass:pass.value,
mobile:mobile.value,email:email.value};
localStorage.setItem("user",JSON.stringify(u));
alert("Registration Successful!");
e.target.reset();
openPage("login");
}

function login(e){
e.preventDefault();
let u=JSON.parse(localStorage.getItem("user"));
if(!u){
alert("Please Register First!");
openPage("reg");return;
}
if(lu.value==u.user&&lp.value==u.pass){
alert("Login Successful! Welcome "+u.name);
openPage("home");
}else alert("Invalid Username or Password!");
}

function enquiry(e){
e.preventDefault();
localStorage.setItem("enquiry",JSON.stringify({
name:cn.value,mobile:cm.value,
motor:mt.value,problem:problem.value}));
alert("Enquiry Submitted!");
e.target.reset();
}
</script>
</body>
</html>