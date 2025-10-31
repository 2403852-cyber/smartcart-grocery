<!DOCTYPE html>
<html>
<head>
<title>SmartCart Grocery Store</title>
<style>
body{font-family:Arial;background:#f7f7f7;margin:0}
header{background:#2ecc71;color:white;text-align:center;padding:15px}
nav{background:#27ae60;padding:10px;text-align:center}
nav a{color:white;margin:10px;text-decoration:none;font-weight:bold;cursor:pointer}
section{display:none;padding:20px}
.active{display:block}
.card{background:white;padding:20px;border-radius:8px;box-shadow:0 2px 5px rgba(0,0,0,0.2);margin-bottom:20px}
.table{width:100%;background:white;border-collapse:collapse}
.table th,.table td{padding:10px;border:1px solid #ddd}
button{background:#27ae60;color:white;padding:10px;border:none;border-radius:5px;cursor:pointer;margin-top:8px}
button:hover{background:#1f8f4b}
input,select{width:100%;padding:10px;margin-bottom:10px;border:1px solid #ccc;border-radius:5px}
</style>
<script>
function showPage(page){
document.querySelectorAll("section").forEach(x=>x.classList.remove("active"));
document.getElementById(page).classList.add("active");
}
</script>
</head>

<body>
<header><h1>SmartCart Groceries</h1></header>

<nav>
<a onclick="showPage('home')">Home</a>
<a onclick="showPage('products')">Products</a>
<a onclick="showPage('cart')">Cart</a>
<a onclick="showPage('checkout')">Checkout</a>
</nav>

<!-- HOME -->
<section id="home" class="active">
<div class="card">
<h2>Fresh Groceries Delivered</h2>
<p>Convenient shopping & fast delivery.</p>
<input type="text" placeholder="Search groceries...">
<p><b>Free delivery for orders above KES 1,000!</b></p>
<button onclick="showPage('products')">Shop Now</button>
</div>
</section>

<!-- PRODUCTS -->
<section id="products">
<div class="card"><h2>Our Products</h2>
<p>Browse and add to cart</p>

<div class="card"><h3>Apples 1kg</h3><p>KES 200</p><button>Add to Cart</button></div>
<div class="card"><h3>Rice 5kg</h3><p>KES 650</p><button>Add to Cart</button></div>
<div class="card"><h3>Milk 1L</h3><p>KES 65</p><button>Add to Cart</button></div>
<div class="card"><h3>Bread</h3><p>KES 80</p><button>Add to Cart</button></div>

</div>
</section>

<!-- CART -->
<section id="cart">
<div class="card"><h2>Your Cart</h2>
<table class="table">
<tr><th>Item</th><th>Qty</th><th>Price</th><th>Total</th></tr>
<tr><td>Apples</td><td>2</td><td>200</td><td>400</td></tr>
<tr><td>Bread</td><td>1</td><td>80</td><td>80</td></tr>
</table>
<p><b>Total: KES 480</b></p>
<button onclick="showPage('checkout')">Proceed to Checkout</button>
</div>
</section>

<!-- CHECKOUT -->
<section id="checkout">
<div class="card"><h2>Checkout</h2>
<input type="text" placeholder="Full Name">
<input type="text" placeholder="Phone Number">
<input type="text" placeholder="Delivery Address">
<select>
<option>M-Pesa</option>
<option>Credit/Debit Card</option>
<option>Cash on Delivery</option>
</select>
<button>Place Order</button>
</div>
</section>

</body>
</html>
