
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>IronCore Gym</title>

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family:'Segoe UI',sans-serif;
}

body{
  background:#0b0b0b;
  color:#fff;
}

/* NAVBAR */
.navbar{
  display:flex;
  justify-content:space-between;
  align-items:center;
  padding:18px 60px;
  position:fixed;
  width:100%;
  top:0;
  background:rgba(0,0,0,0.9);
  backdrop-filter:blur(6px);
  z-index:1000;
}

.logo{
  font-size:1.9rem;
  font-weight:800;
  letter-spacing:1px;
}

.logo span{color:#e10600;}

.navbar a{
  margin-left:22px;
  text-decoration:none;
  color:#fff;
  font-weight:500;
}

.btn{
  background:#e10600;
  padding:8px 16px;
  border-radius:6px;
}

/* HERO */
.hero{
  height:100vh;
  background:
    linear-gradient(rgba(0,0,0,0.75),rgba(0,0,0,0.9)),
    url("https://images.unsplash.com/photo-1558611848-73f7eb4001a1");
  background-size:cover;
  background-position:center;
  background-attachment:fixed;
  display:flex;
  align-items:center;
  padding-left:60px;
}

.hero-content{max-width:520px;}

.hero h2{
  font-size:4rem;
  font-weight:800;
  text-transform:uppercase;
  line-height:1.1;
  margin-bottom:15px;
}

.hero p{
  font-size:1.3rem;
  color:#ddd;
  margin-bottom:30px;
}

.cta{
  background:linear-gradient(135deg,#e10600,#ff2e2e);
  border:none;
  padding:16px 38px;
  font-size:1.05rem;
  font-weight:600;
  color:#fff;
  cursor:pointer;
  border-radius:30px;
  letter-spacing:.5px;
  box-shadow:0 12px 30px rgba(225,6,0,.6);
  transition:all .3s ease;
}

.cta:hover{
  transform:translateY(-3px);
  box-shadow:0 18px 40px rgba(225,6,0,.85);
}

/* SECTIONS */
.section{
  padding:100px 60px;
  text-align:center;
}

.section h2{
  font-size:2.6rem;
  margin-bottom:50px;
}

.dark{background:#111;}

/* CARDS */
.cards{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:30px;
}

.card,
.price-card{
  position:relative;
  overflow:hidden;
}

/* Glow overlay */
.card::before,
.price-card::before{
  content:"";
  position:absolute;
  inset:0;
  border-radius:inherit;
  background:radial-gradient(circle at top left,
    rgba(225,6,0,0.45),
    transparent 60%);
  opacity:0;
  transition:opacity .3s ease;
  pointer-events:none;
}

.card:hover::before,
.price-card:hover::before{
  opacity:1;
}

.card{
  background:linear-gradient(145deg,#1a1a1a,#222);
  padding:50px 20px;
  border-radius:14px;
  font-size:1.15rem;
  box-shadow:0 12px 28px rgba(0,0,0,.6);
  transition:all .3s ease;
}

.card:hover{
  transform:translateY(-12px) scale(1.02);
  box-shadow:
    0 0 25px rgba(225,6,0,.45),
    0 25px 50px rgba(0,0,0,.9);
}

.card span{
  display:block;
  margin-top:12px;
  font-size:.95rem;
  color:#e10600;
}

/* PRICING */
.pricing{
  display:flex;
  justify-content:center;
  gap:35px;
  flex-wrap:wrap;
}

.price-card{
  background:#1c1c1c;
  padding:45px;
  width:250px;
  border-radius:14px;
  box-shadow:0 15px 35px rgba(0,0,0,.6);
  transition:all .3s ease;
}

.price-card:hover{
  transform:scale(1.08);
  box-shadow:
    0 0 30px rgba(225,6,0,.5),
    0 30px 60px rgba(0,0,0,.9);
}

.price-card h3{
  font-size:1.5rem;
  margin-bottom:10px;
}

.highlight{
  border:2px solid #e10600;
  transform:scale(1.08);
}

/* FOOTER */
footer{
  background:
    linear-gradient(rgba(0,0,0,.85),rgba(0,0,0,.95)),
    url("https://images.unsplash.com/photo-1599058917212-d750089bc07d");
  background-size:cover;
  background-position:center;
  padding:100px 20px;
  text-align:center;
}

footer h2{
  font-size:2.4rem;
  margin-bottom:15px;
}

footer p{
  color:#ccc;
  margin-bottom:25px;
}

/* RESPONSIVE */
@media(max-width:768px){
  .navbar{padding:15px 25px;}
  .hero{
    padding:120px 25px 0;
    text-align:center;
  }
  .hero h2{font-size:2.7rem;}
  .section{padding:80px 25px;}
}
</style>
</head>

<body>

<header class="navbar">
  <div class="logo">IRON<span>CORE</span></div>
  <nav>
    <a href="#programs">Programs</a>
    <a href="#trainers">Trainers</a>
    <a href="#plans">Plans</a>
    <a href="#contact" class="btn">Join Now</a>
  </nav>
</header>

<section class="hero">
  <div class="hero-content">
    <h2>Build Strength<br>Build Discipline</h2>
    <p>Your transformation starts today.</p>
    <button class="cta">Book Free Trial</button>
  </div>
</section>

<section id="programs" class="section">
  <h2>Our Programs</h2>
  <div class="cards">
    <div class="card">Strength Training</div>
    <div class="card">Fat Loss</div>
    <div class="card">CrossFit</div>
    <div class="card">Personal Training</div>
  </div>
</section>

<section id="trainers" class="section dark">
  <h2>Expert Trainers</h2>
  <div class="cards">
    <div class="card">Coach Arjun<span>Strength</span></div>
    <div class="card">Coach Neha<span>Weight Loss</span></div>
    <div class="card">Coach Rahul<span>CrossFit</span></div>
    <div class="card">Coach Priya<span>Yoga</span></div>
  </div>
</section>

<section id="plans" class="section">
  <h2>Membership Plans</h2>
  <div class="pricing">
    <div class="price-card">
      <h3>Basic</h3>
      <p>₹999 / month</p>
      <p>Gym Access</p>
    </div>
    <div class="price-card highlight">
      <h3>Pro</h3>
      <p>₹1999 / month</p>
      <p>Gym + Classes</p>
    </div>
    <div class="price-card">
      <h3>Elite</h3>
      <p>₹2999 / month</p>
      <p>All Access + PT</p>
    </div>
  </div>
</section>

<footer id="contact">
  <h2>Join IronCore Today</h2>
  <p>Train harder. Get stronger. Stay consistent.</p>
  <button class="cta">Contact Us</button>
</footer>

</body>
</html>

