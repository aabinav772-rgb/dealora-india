<html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Dealora India - Smart Shopping</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial,sans-serif;background:#f5f8f7;color:#17251f}
header{background:#101e19;color:white;padding:20px 7%;display:flex;justify-content:space-between;align-items:center}
.logo{font-size:27px;font-weight:900;color:#55dda0}
.hero{background:#10251d;color:white;padding:65px 8%;text-align:center}
.hero h1{font-size:42px;margin:10px}
.hero h1 span{color:#55dda0}
.hero p{color:#c7d8d0;line-height:1.7}
button{background:#159e67;color:white;border:0;padding:13px 20px;border-radius:8px;font-weight:bold;cursor:pointer}
section{padding:35px 7%}
h2{font-size:27px}
.tools,.deals{display:grid;grid-template-columns:repeat(auto-fit,minmax(230px,1fr));gap:16px}
.card{background:white;border:1px solid #e3ebe6;border-radius:13px;padding:20px;box-shadow:0 5px 18px #14251a08}
input{width:100%;padding:12px;border:1px solid #dce5df;border-radius:7px;margin:8px 0 15px}
.result{color:#128653;font-weight:bold;line-height:1.6}
.tag{color:#138c5b;font-size:12px;font-weight:bold}
footer{background:#10251d;color:white;padding:30px;text-align:center}
small{color:#a8b9b0}
</style>
</head>
<body>
<header><div class="logo">DEALORA.</div><span>INDIA</span></header>
<div class="hero">
<div class="tag">SMART SHOPPING STARTS HERE</div>
<h1>Find Better Deals.<br><span>Save More Money.</span></h1>
<p>Discover savings, compare prices and make smarter shopping decisions.</p>
<button onclick="document.getElementById('tools').scrollIntoView()">Explore Free Tools</button>
</div>
<section id="tools">
<h2>Free Savings Calculators</h2>
<div class="tools">
<div class="card">
<h3>Discount Calculator</h3>
<label>Original price (₹)</label>
<input id="price" type="number" placeholder="Enter MRP">
<label>Discount (%)</label>
<input id="discount" type="number" placeholder="Enter discount">
<button onclick="calculate()">Calculate</button>
<p class="result" id="answer">Your savings will appear here.</p>
</div>
<div class="card">
<h3>Profit Calculator</h3>
<label>Purchase price (₹)</label>
<input id="cost" type="number" placeholder="Purchase price">
<label>Selling price (₹)</label>
<input id="selling" type="number" placeholder="Selling price">
<button onclick="profit()">Calculate profit</button>
<p class="result" id="profitAnswer">Your profit will appear here.</p>
</div>
</div>
</section>
<section>
<h2>Shopping Deals</h2>
<p>Useful offers and savings ideas. We are adding verified deals soon.</p>
<div class="deals">
<div class="card"><div class="tag">SHOP SMART</div><h3>Compare product prices</h3><p>Compare pack sizes and find the better unit price.</p></div>
<div class="card"><div class="tag">SAVE MONEY</div><h3>Understand discounts</h3><p>Calculate the actual price after an offer.</p></div>
<div class="card"><div class="tag">COMING SOON</div><h3>India's shopping deals</h3><p>Verified deals and useful shopping offers will appear here.</p></div>
</div>
</section>
<footer>
<h2>DEALORA INDIA</h2>
<p>Find Deals. Know Your Savings.</p>
<small>Independent shopping information website. Always verify prices with sellers.</small>
</footer>
<script>
function calculate(){
let p=Number(document.getElementById('price').value);
let d=Number(document.getElementById('discount').value);
if(p<=0||d<0||d>100||!Number.isFinite(d)){document.getElementById('answer').innerText='Enter a valid price and discount.';return}
let save=p*d/100;
document.getElementById('answer').innerText='You save ₹'+save.toFixed(2)+'. Final price: ₹'+(p-save).toFixed(2);
}
function profit(){
let c=Number(document.getElementById('cost').value);
let s=Number(document.getElementById('selling').value);
if(c<=0||s<0){document.getElementById('profitAnswer').innerText='Enter valid prices.';return}
let p=s-c;
document.getElementById('profitAnswer').innerText='Profit/loss: ₹'+p.toFixed(2)+' | Margin: '+(p/s*100||0).toFixed(2)+'%';
}
</script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="description" content="Dealora India helps you discover shopping savings, compare prices and calculate discounts.">
<title>Dealora India | Discover. Compare. Save.</title>
<style>
:root{--green:#16a36a;--dark:#101d19;--muted:#68756f;--bg:#f5f8f6;--line:#e6ece8}
*{box-sizing:border-box}
body{margin:0;font-family:Arial,sans-serif;color:var(--dark);background:white}
a{text-decoration:none;color:inherit}
header{height:75px;padding:0 7%;display:flex;align-items:center;justify-content:space-between;border-bottom:1px solid var(--line)}
.logo{font-size:27px;font-weight:900;letter-spacing:-1px}
.logo span{color:var(--green)}
nav{display:flex;gap:25px;font-size:14px;color:#58645e}
nav a:hover{color:var(--green)}
.header-btn,.btn{padding:12px 19px;border-radius:8px;background:var(--green);color:white;font-weight:bold;font-size:13px;border:0;cursor:pointer}
.hero{background:var(--dark);color:white;padding:85px 8%;display:grid;grid-template-columns:1.2fr .8fr;gap:40px;align-items:center}
.eyebrow{font-size:11px;letter-spacing:2px;color:#65dba6;font-weight:bold}
.hero h1{font-size:clamp(40px,5vw,65px);line-height:1.08;letter-spacing:-2px;margin:20px 0}
.hero h1 span{color:#65dba6}
.hero p{color:#c0cec6;line-height:1.8;max-width:490px}
.hero .btn{display:inline-block;margin-top:20px}
.hero-card{background:white;color:var(--dark);padding:28px;border-radius:17px;max-width:390px}
.hero-card .number{font-size:48px;font-weight:900;color:var(--green);margin:20px 0}
.hero-card p{color:var(--muted);font-size:13px}
.hero-card .line{border-top:1px solid var(--line);padding:13px 0;font-size:13px}
section{padding:65px 7%}
.heading{margin-bottom:25px}
.heading small{color:var(--green);font-weight:bold;letter-spacing:2px}
.heading h2{font-size:31px;letter-spacing:-1px;margin:10px 0}
.heading p{color:var(--muted);font-size:14px}
.search{display:flex;gap:10px;margin:25px 0}
.search input{flex:1}
input,select{padding:13px;border:1px solid #dce5df;border-radius:8px;width:100%;font-size:14px}
.categories{display:flex;gap:10px;flex-wrap:wrap;margin:20px 0}
.categories button{border:1px solid var(--line);background:white;padding:10px 16px;border-radius:30px;cursor:pointer}
.categories button.active,.categories button:hover{background:#e9f7f0;color:var(--green);border-color:#b8e5ce}
.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:17px}
.card{border:1px solid var(--line);padding:22px;border-radius:13px;background:white}
.card-icon{font-size:32px;background:#f0f6f2;width:58px;height:58px;border-radius:12px;display:grid;place-items:center}
.card h3{font-size:17px;margin:18px 0 8px}
.card p{font-size:13px;color:var(--muted);line-height:1.6}
.card small{color:#b07b20;font-size:11px}
.tools{background:var(--bg)}
.tool-grid{display:grid;grid-template-columns:1fr 1fr;gap:20px}
.tool{background:white;border:1px solid var(--line);border-radius:13px;padding:25px}
.tool h3{margin-top:0}
.tool label{display:block;font-size:12px;font-weight:bold;margin:15px 0 7px}
.result{margin-top:15px;padding:14px;background:#eaf7f0;color:#13784e;border-radius:8px;font-size:14px;line-height:1.7;min-height:45px}
.compare{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.banner{background:var(--dark);color:white;border-radius:16px;padding:40px;margin:50px 7%;display:flex;justify-content:space-between;align-items:center;gap:20px}
.banner p{color:#bdcec4;line-height:1.6}
footer{background:#101d19;color:white;padding:40px 7%;text-align:center}
footer p{color:#aabbb1;font-size:12px;line-height:1.8}
footer a{color:#65dba6;font-size:12px;margin:10px}
.notice{font-size:12px;background:#fff8e8;color:#795a1c;padding:13px;border-radius:8px;line-height:1.6}
@media(max-width:750px){
header{padding:0 5%}nav{display:none}
.hero{grid-template-columns:1fr;padding:55px 6%}
.grid{grid-template-columns:1fr 1fr}
.tool-grid{grid-template-columns:1fr}
.banner{margin:30px 5%;padding:27px;display:block}
}
@media(max-width:480px){.grid{grid-template-columns:1fr}section{padding:45px 5%}.hero h1{font-size:43px}}
</style>
</head>
<body>

<header>
<a href="#" class="logo">DEAL<span>ORA</span>.</a>
<nav>
<a href="#deals">Deals</a>
<a href="#categories">Categories</a>
<a href="#tools">Calculators</a>
<a href="#about">About</a>
</nav>
<a class="header-btn" href="#deals">Explore Deals ↗</a>
</header>

<div class="hero">
<div>
<div class="eyebrow">WELCOME TO DEALORA INDIA</div>
<h1>Shop Smart.<br><span>Save More.</span></h1>
<p>Discover useful shopping deals, compare product prices and calculate your savings. Make every shopping decision smarter.</p>
<a href="#deals" class="btn">Discover Deals →</a>
</div>
<div class="hero-card">
<div class="eyebrow">YOUR SMART SHOPPING DESTINATION</div>
<div class="number">₹ SAVE</div>
<h3>Every rupee matters.</h3>
<p>Find better value with our free shopping and savings tools.</p>
<div class="line">✓ Free discount calculator</div>
<div class="line">✓ Product price comparison</div>
<div class="line">✓ Shopping tips and guides</div>
</div>
</div>

<section id="deals">
<div class="heading">
<small>DISCOVER MORE</small>
<h2>Explore Shopping Deals</h2>
<p>Find useful offers and make smarter buying decisions.</p>
</div>
<div class="notice">We are building our verified deals collection. No live offers are advertised yet. Check retailer websites for current prices and availability.</div>
<div class="search">
<input id="search" placeholder="Search electronics, fashion, grocery..." oninput="filterDeals()">
</div>
<div class="categories" id="categories">
<button class="active" onclick="choose('All',this)">All</button>
<button onclick="choose('Electronics',this)">Electronics</button>
<button onclick="choose('Fashion',this)">Fashion</button>
<button onclick="choose('Home',this)">Home</button>
<button onclick="choose('Grocery',this)">Grocery</button>
</div>
<div class="grid" id="dealGrid">
<article class="card" data-category="Electronics"><div class="card-icon">📱</div><h3>Electronics Deals</h3><p>Discover value in mobiles, accessories and gadgets.</p><small>DEALS COLLECTION COMING SOON</small></article>
<article class="card" data-category="Fashion"><div class="card-icon">👕</div><h3>Fashion Deals</h3><p>Explore clothing, footwear and everyday style.</p><small>DEALS COLLECTION COMING SOON</small></article>
<article class="card" data-category="Home"><div class="card-icon">🏠</div><h3>Home & Kitchen</h3><p>Find useful products for your home.</p><small>DEALS COLLECTION COMING SOON</small></article>
<article class="card" data-category="Grocery"><div class="card-icon">🛒</div><h3>Grocery Savings</h3><p>Compare everyday essentials and pack prices.</p><small>DEALS COLLECTION COMING SOON</small></article>
</div>
</section>

<section class="tools" id="tools">
<div class="heading">
<small>FREE ONLINE TOOLS</small>
<h2>Calculate Your Savings</h2>
<p>Simple tools to help you shop smarter.</p>
</div>
<div class="tool-grid">
<div class="tool">
<h3>Discount Calculator</h3>
<p>Calculate the final price after discount.</p>
<label>Original price (₹)</label>
<input id="price" type="number" placeholder="Example: 1000">
<label>Discount percentage (%)</label>
<input id="discount" type="number" placeholder="Example: 30">
<button class="btn" onclick="discountCalc()">Calculate</button>
<div class="result" id="discountResult">Your result will appear here.</div>
</div>
<div class="tool">
<h3>Price Comparison</h3>
<p>Find which pack offers better value.</p>
<div class="compare">
<div><label>Pack A price (₹)</label><input id="aPrice" type="number" placeholder="80"></div>
<div><label>Pack A quantity</label><input id="aQty" type="number" placeholder="500"></div>
<div><label>Pack B price (₹)</label><input id="bPrice" type="number" placeholder="145"></div>
<div><label>Pack B quantity</label><input id="bQty" type="number" placeholder="1000"></div>
</div>
<button class="btn" onclick="compareCalc()">Compare</button>
<div class="result" id="compareResult">Enter quantities in the same unit.</div>
</div>
</div>
</section>

<div class="banner" id="about">
<div><div class="eyebrow">ABOUT DEALORA</div><h2>Better choices. Better savings.</h2><p>Our mission is to make shopping information simple and useful for everyone in India.</p></div>
<a class="btn" href="#tools">Try Free Tools →</a>
</div>

<footer>
<div class="logo">DEAL<span>ORA</span>.</div>
<p>Find Deals. Know Your Savings.</p>
<p>Dealora is an independent shopping information project and is not affiliated with retailers.</p>
<p>Prices and offers can change. Always verify details with the seller.</p>
<p><a href="privacy.html">Privacy</a> <a href="disclosure.html">Affiliate Disclosure</a></p>
<p>© 2026 Dealora India</p>
</footer>

<script>
let category='All';
function choose(c,button){
category=c;
document.querySelectorAll('.categories button').forEach(b=>b.classList.remove('active'));
button.classList.add('active');
filterDeals();
}
function filterDeals(){
let q=document.getElementById('search').value.toLowerCase();
document.querySelectorAll('#dealGrid .card').forEach(card=>{
let matchCategory=category==='All'||card.dataset.category===category;
let matchText=card.innerText.toLowerCase().includes(q);
card.style.display=matchCategory&&matchText?'block':'none';
});
}
function discountCalc(){
let p=Number(document.getElementById('price').value);
let d=Number(document.getElementById('discount').value);
let out=document.getElementById('discountResult');
if(p<=0||d<0||d>100||!Number.isFinite(d)){out.innerText='Enter a valid price and discount between 0 and 100.';return;}
let saving=p*d/100;
out.innerHTML='You save <b>₹'+saving.toFixed(2)+'</b><br>Final price: <b>₹'+(p-saving).toFixed(2)+'</b>';
}
function compareCalc(){
let p1=Number(document.getElementById('aPrice').value),q1=Number(document.getElementById('aQty').value);
let p2=Number(document.getElementById('bPrice').value),q2=Number(document.getElementById('bQty').value);
let out=document.getElementById('compareResult');
if(p1<=0||p2<=0||q1<=0||q2<=0){out.innerText='Enter all four values above zero. Use the same unit for both quantities.';return;}
let a=p1/q1,b=p2/q2;
out.innerHTML='Pack A: ₹'+a.toFixed(4)+' per unit<br>Pack B: ₹'+b.toFixed(4)+' per unit<br><b>'+(a<b?'Pack A is better value.':a>b?'Pack B is better value.':'Both have equal unit prices.')+'</b>';
}
</script>
</body>
</html>
