
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>PANDA TECH | Tecnología al alcance de todos</title>
<style>
*{box-sizing:border-box}
body{margin:0;background:#020916;color:white;font-family:Arial,sans-serif}
a{color:inherit;text-decoration:none}
.top{background:#010713;padding:12px;text-align:center;color:#00c8ff;font-size:12px;border-bottom:1px solid #087bff}
header{padding:15px;background:#020b1b;display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap;border-bottom:2px solid #008cff}
.brand{display:flex;align-items:center;gap:10px;font-size:27px;font-weight:900;font-style:italic}
.brand img{width:75px;height:75px;object-fit:cover;border-radius:50%;border:2px solid #00aaff;box-shadow:0 0 15px #008cff}
.brand span{color:#00baff}
.search{flex:1;min-width:180px;padding:15px;border-radius:30px;border:2px solid #008cff;font-size:15px}
.cart-btn{background:#006dff;color:white;padding:13px;border:0;border-radius:25px;font-weight:bold}
nav{display:flex;justify-content:space-around;gap:12px;padding:16px 5px;background:#061a35;border-bottom:2px solid #008cff;flex-wrap:wrap}
nav a{font-weight:bold;font-size:14px}
nav a:hover{color:#00c8ff}
.hero{margin:12px;padding:25px 20px;min-height:330px;border:2px solid #008cff;border-radius:18px;background:radial-gradient(circle at 75%,#064c9d,#020817 65%);display:flex;align-items:center;justify-content:space-between;gap:10px;overflow:hidden}
.hero-text{max-width:55%}
.hero h1{font-size:clamp(42px,8vw,75px);line-height:.9;margin:0;font-style:italic}
.hero h1 span{color:#00baff}
.hero h3{font-size:20px}
.hero p{line-height:1.5}
.hero img{width:43%;max-width:390px;object-fit:contain;filter:drop-shadow(0 0 18px #008cff)}
.btn{background:#007bff;color:white;border:0;padding:13px 20px;border-radius:25px;font-weight:bold;cursor:pointer;box-shadow:0 0 12px #007bff}
.btn:hover{background:#00aaff}
h2{margin:28px 15px 12px;border-left:5px solid #00baff;padding-left:12px}
.categories{display:grid;grid-template-columns:repeat(6,1fr);gap:10px;padding:12px}
.cat{background:#07182e;border:2px solid #008cff;border-radius:12px;padding:18px 5px;text-align:center;font-size:13px;font-weight:bold;box-shadow:0 0 10px #005bba;cursor:pointer}
.cat b{display:block;font-size:30px;margin-bottom:8px}
.cat:hover{background:#073d78}
.products{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:12px;padding:12px}
.product{background:#071529;border:1px solid #087bff;border-radius:14px;padding:12px;text-align:center;overflow:hidden}
.product .pic{height:125px;display:flex;align-items:center;justify-content:center;font-size:75px;background:radial-gradient(circle,#12345b,#071529);border-radius:10px}
.product h3{font-size:14px;min-height:35px}
.price{color:#00caff;font-size:21px;font-weight:bold}
.old{color:#999;text-decoration:line-through;font-size:12px}
.product button{width:100%;margin-top:12px}
.promo{margin:15px;padding:30px;text-align:center;background:linear-gradient(110deg,#003e91,#020817);border:2px solid #087bff;border-radius:15px;font-size:22px;font-weight:bold}
.promo span{color:#00caff}
.benefits{display:flex;justify-content:space-around;gap:10px;flex-wrap:wrap;background:#06162c;padding:20px;color:#00caff;text-align:center}
footer{text-align:center;background:#010713;padding:25px;color:#aaa;font-size:13px}
.whatsapp{position:fixed;right:15px;bottom:18px;background:#08bd65;color:white;padding:15px;border-radius:30px;font-weight:bold;box-shadow:0 0 15px #08bd65;z-index:3}
#cartBox{display:none;position:fixed;inset:5%;background:#07172d;border:2px solid #008cff;border-radius:15px;padding:20px;overflow:auto;z-index:10;box-shadow:0 0 30px #008cff}
#cartBox h2{margin-top:10px}
.cart-item{border-bottom:1px solid #234;padding:10px 0}
.remove{background:#a22;color:white;border:0;border-radius:8px;padding:5px 10px}
@media(max-width:700px){
 .hero{min-height:230px;padding:15px}
 .hero h1{font-size:43px}
 .hero img{width:43%}
 .hero-text{max-width:58%}
 .hero h3{font-size:15px}
 .hero p{font-size:12px}
 .categories{grid-template-columns:repeat(3,1fr)}
 .products{grid-template-columns:repeat(2,minmax(0,1fr))}
 .brand{font-size:23px}
 .brand img{width:58px;height:58px}
 nav{font-size:12px}
}
</style>
</head>
<body>

<div class="top">
🚚 ENVÍOS A TODO EL PAÍS | 🛡️ COMPRA SEGURA | 💳 MEDIOS DE PAGO
</div>

<header>
 <div class="brand">
  <img src="panda-tech.png" alt="Panda gamer">
  <div>PANDA<br><span>TECH</span></div>
 </div>
 <input class="search" id="search" placeholder="🔎 Buscar productos..." oninput="buscar()">
 <button class="cart-btn" onclick="mostrarCarrito()">🛒 <span id="cantidad">0</span></button>
</header>

<nav>
 <a href="#">🏠 Inicio</a>
 <a href="#categorias">▦ Categorías</a>
 <a href="#productos">🔥 Ofertas</a>
 <a href="#productos">⭐ Más vendidos</a>
 <a href="#contacto">🎧 Contacto</a>
</nav>

<section class="hero">
 <div class="hero-text">
  <h1>PANDA<br><span>TECH</span></h1>
  <h3>Tecnología al alcance de todos</h3>
  <p>Encontrá los mejores productos, con la mejor atención y precios increíbles.</p>
  <button class="btn" onclick="document.getElementById('productos').scrollIntoView()">🛒 Comprar ahora →</button>
 </div>
 <img src="panda-tech.png" alt="Panda Tech gamer">
</section>

<h2 id="categorias">Nuestras categorías</h2>

<section class="categories">
 <div class="cat" onclick="filtrar('celulares')"><b>📱</b>Celulares</div>
 <div class="cat" onclick="filtrar('informatica')"><b>💻</b>Informática</div>
 <div class="cat" onclick="filtrar('gaming')"><b>🎮</b>Gaming</div>
 <div class="cat" onclick="filtrar('audio')"><b>🎧</b>Audio</div>
 <div class="cat" onclick="filtrar('tv')"><b>📺</b>TV y Video</div>
 <div class="cat" onclick="filtrar('todos')"><b>✨</b>Otros</div>
</section>

<h2 id="productos">🔥 Productos destacados</h2>

<section class="products" id="lista">

 <div class="product" data-name="auriculares bluetooth" data-cat="audio">
  <div class="pic">🎧</div>
  <h3>Auriculares Bluetooth</h3>
  <div class="price">$24.999</div>
  <div class="old">$34.999</div>
  <button class="btn" onclick="agregar('Auriculares Bluetooth',24999)">🛒 Agregar</button>
 </div>

 <div class="product" data-name="mouse gamer rgb" data-cat="gaming">
  <div class="pic">🖱️</div>
  <h3>Mouse Gamer RGB</h3>
  <div class="price">$19.999</div>
  <div class="old">$29.999</div>
  <button class="btn" onclick="agregar('Mouse Gamer RGB',19999)">🛒 Agregar</button>
 </div>

 <div class="product" data-name="teclado mecanico gamer" data-cat="gaming">
  <div class="pic">⌨️</div>
  <h3>Teclado Mecánico Gamer</h3>
  <div class="price">$44.999</div>
  <div class="old">$59.999</div>
  <button class="btn" onclick="agregar('Teclado Mecánico Gamer',44999)">🛒 Agregar</button>
 </div>

 <div class="product" data-name="auriculares gamer rgb" data-cat="audio">
  <div class="pic">🎮</div>
  <h3>Auriculares Gamer RGB</h3>
  <div class="price">$29.999</div>
  <div class="old">$39.999</div>
  <button class="btn" onclick="agregar('Auriculares Gamer RGB',29999)">🛒 Agregar</button>
 </div>

 <div class="product" data-name="celular smartphone" data-cat="celulares">
  <div class="pic">📱</div>
  <h3>Celular Smartphone</h3>
  <div class="price">Consultar</div>
  <button class="btn" onclick="agregar('Celular Smartphone',0)">Consultar</button>
 </div>

 <div class="product" data-name="notebook computadora" data-cat="informatica">
  <div class="pic">💻</div>
  <h3>Notebook</h3>
  <div class="price">Consultar</div>
  <button class="btn" onclick="agregar('Notebook',0)">Consultar</button>
 </div>

 <div class="product" data-name="smart tv television" data-cat="tv">
  <div class="pic">📺</div>
  <h3>Smart TV</h3>
  <div class="price">Consultar</div>
  <button class="btn" onclick="agregar('Smart TV',0)">Consultar</button>
 </div>

 <div class="product" data-name="consola videojuegos" data-cat="gaming">
  <div class="pic">🎮</div>
  <h3>Consola de videojuegos</h3>
  <div class="price">Consultar</div>
  <button class="btn" onclick="agregar('Consola de videojuegos',0)">Consultar</button>
 </div>

</section>

<div class="promo">
 🎮 Llevá tu experiencia<br>al siguiente <span>nivel</span><br>
 🐼 PANDA TECH
</div>

<div class="benefits">
 <div>🛡️ Compra segura</div>
 <div>🚚 Envíos a todo el país</div>
 <div>🎧 Atención personalizada</div>
</div>

<footer id="contacto">
 <h2>PANDA TECH 🐼</h2>
 Tecnología al alcance de todos.<br><br>
 Consultanos por nuestros productos y ofertas.<br><br>
 © 2026 PANDA TECH
</footer>

<a class="whatsapp" href="https://wa.me/549XXXXXXXXXX" target="_blank">🟢 WhatsApp</a>

<div id="cartBox">
 <h2>🛒 Mi carrito</h2>
 <div id="items"></div>
 <h3 id="total">Total: $0</h3>
 <button class="btn" onclick="comprar()">Comprar por WhatsApp</button>
 <button class="btn" onclick="cerrarCarrito()">Cerrar</button>
</div>

<script>
let carrito=[];

function agregar(nombre,precio){
 carrito.push({nombre,precio});
 document.getElementById('cantidad').textContent=carrito.length;
 alert('Producto agregado al carrito');
}

function mostrarCarrito(){
 document.getElementById('cartBox').style.display='block';
 let total=0;
 document.getElementById('items').innerHTML=carrito.map((p,i)=>{
 total+=p.precio;
 return `<div class="cart-item">${p.nombre} - ${p.precio? '$'+p.precio.toLocaleString('es-AR'):'Consultar'} <button class="remove" onclick="eliminar(${i})">Quitar</button></div>`;
 }).join('')||'Tu carrito está vacío';
 document.getElementById('total').textContent='Total: $'+total.toLocaleString('es-AR');
}

function eliminar(i){
 carrito.splice(i,1);
 document.getElementById('cantidad').textContent=carrito.length;
 mostrarCarrito();
}

function cerrarCarrito(){
 document.getElementById('cartBox').style.display='none';
}

function comprar(){
 if(!carrito.length){alert('Tu carrito está vacío');return;}
 let mensaje='Hola Panda Tech! Quiero consultar por:%0A';
 carrito.forEach(p=>mensaje+=p.nombre+' - '+(p.precio?'$'+p.precio:'Consultar')+'%0A');
 let total=carrito.reduce((s,p)=>s+p.precio,0);
 mensaje+='Total: $'+total.toLocaleString('es-AR');
 window.open('https://wa.me/549XXXXXXXXXX?text='+mensaje,'_blank');
}

function buscar(){
 let q=document.getElementById('search').value.toLowerCase();
 document.querySelectorAll('.product').forEach(p=>{
 p.style.display=p.dataset.name.includes(q)?'block':'none';
 });
}

function filtrar(cat){
 document.querySelectorAll('.product').forEach(p=>{
 p.style.display=(cat==='todos'||p.dataset.cat===cat)?'block':'none';
 });
 document.getElementById('productos').scrollIntoView();
}
</script>

</body>
</html>

