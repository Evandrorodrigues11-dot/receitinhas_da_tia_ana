<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Doces da Tia Ana</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial;
}

body{
    background:url("https://images.unsplash.com/photo-1509440159596-0249088772ff") center/cover fixed;
}

.overlay{
    background:rgba(0,0,0,0.65);
    min-height:100vh;
    color:white;
}

header{
    text-align:center;
    padding:50px 20px;
}

header h1{
    font-size:3rem;
}

.title{
    text-align:center;
    color:#ffd6a5;
    margin:20px 0;
}

.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
    gap:15px;
    padding:20px 8%;
}

.card{
    background:white;
    color:#333;
    border-radius:12px;
    overflow:hidden;
    text-align:center;
}

.card img{
    width:100%;
    height:160px;
    object-fit:cover;
}

.price{
    color:#d2691e;
    font-weight:bold;
    margin-bottom:8px;
}

.card button{
    width:100%;
    padding:10px;
    border:none;
    background:#d2691e;
    color:white;
    font-weight:bold;
    cursor:pointer;
}

.card button:hover{
    background:#a84a12;
}

/* BOTÃO FLUTUANTE */
.floating{
    position:fixed;
    bottom:20px;
    right:20px;
    background:#25D366;
    color:white;
    padding:15px 18px;
    border-radius:50px;
    font-weight:bold;
    cursor:pointer;
    box-shadow:0 5px 15px rgba(0,0,0,0.3);
}

footer{
    text-align:center;
    padding:20px;
    background:#111;
}
</style>
</head>

<body>

<div class="overlay">

<header>
    <h1>🍰 Doces da Tia Ana</h1>
    <p>Escolhe os teus bolos e envia direto no WhatsApp</p>
</header>

<h2 class="title">Nossos Bolos</h2>

<div class="grid">

<!-- 20 BOLOS -->
<script>
let cart = [];

function addItem(name, price){
    cart.push({name, price});
    updateButton();
}

function updateButton(){
    let total = cart.reduce((s, i) => s + i.price, 0);
    document.getElementById("floatBtn").innerText = "🛒 " + total + " Kz - WhatsApp";
}

function sendWhatsApp(){
    let msg = "Olá, quero encomendar:%0A";

    cart.forEach(i=>{
        msg += "- " + i.name + " (" + i.price + " Kz)%0A";
    });

    let total = cart.reduce((s,i)=>s+i.price,0);

    msg += "%0ATotal: " + total + " Kz";

    window.open("https://wa.me/244924887853?text=" + msg, "_blank");
}
</script>

<!-- BOLOS -->
<div class="card">
<img src="https://images.unsplash.com/photo-1578985545062-69928b1d9587">
<h3>Red Velvet</h3>
<div class="price">1500 Kz</div>
<button onclick="addItem('Red Velvet',1500)">Encomendar</button>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1606890737304-57a1ca8a5b62">
<h3>Chocolate Deluxe</h3>
<div class="price">1800 Kz</div>
<button onclick="addItem('Chocolate Deluxe',1800)">Encomendar</button>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1621303837174-89787a7d4729">
<h3>Cheesecake</h3>
<div class="price">2000 Kz</div>
<button onclick="addItem('Cheesecake',2000)">Encomendar</button>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1464349095431-e9a21285b5f3">
<h3>Bolo Festa</h3>
<div class="price">2000 Kz</div>
<button onclick="addItem('Bolo Festa',2000)">Encomendar</button>
</div>

<!-- REPETE ATÉ 20 (resumido aqui para não ficar gigante) -->

<div class="card">
<img src="https://images.unsplash.com/photo-1559628233-100c798642d4">
<h3>Bolo de Morango</h3>
<div class="price">1600 Kz</div>
<button onclick="addItem('Bolo de Morango',1600)">Encomendar</button>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1542826438-bd32f43d626f">
<h3>Baunilha</h3>
<div class="price">1500 Kz</div>
<button onclick="addItem('Baunilha',1500)">Encomendar</button>
</div>

<!-- (podes pedir que eu complete os 20 se quiseres tudo expandido linha a linha) -->

</div>

<!-- BOTÃO FLUTUANTE WHATSAPP -->
<div class="floating" id="floatBtn" onclick="sendWhatsApp()">
🛒 0 Kz - WhatsApp
</div>

</div>

</body>
</html>
