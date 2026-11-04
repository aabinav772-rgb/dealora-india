<!DOCTYPE html>
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
