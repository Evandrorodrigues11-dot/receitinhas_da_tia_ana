<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Doces da Tia Ana</title>

<style>
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-image: url('https://images.unsplash.com/photo-1509440159596-0249088772ff');
    background-size: cover;
    background-attachment: fixed;
}

.overlay {
    background: rgba(0,0,0,0.6);
    min-height: 100vh;
    padding: 20px;
    color: white;
}

header {
    text-align: center;
    padding: 20px;
}

h1 {
    font-size: 40px;
    color: #ffcc70;
}

.catalogo {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    margin-top: 20px;
}

.item {
    background: white;
    color: black;
    border-radius: 10px;
    overflow: hidden;
    text-align: center;
}

.item img {
    width: 100%;
    height: 180px;
    object-fit: cover;
}

.item p {
    padding: 10px;
    font-weight: bold;
}

.whatsapp {
    text-align: center;
    margin-top: 30px;
}

.whatsapp a {
    background: green;
    color: white;
    padding: 15px 25px;
    border-radius: 10px;
    text-decoration: none;
    font-size: 18px;
}
</style>
</head>

<body>

<div class="overlay">

<header>
    <h1>Doces da Tia Ana 🍰</h1>
    <p>Os melhores bolos caseiros de Luanda</p>
</header>

<section class="catalogo">

    <div class="item">
        <img src="https://images.unsplash.com/photo-1578985545062-69928b1d9587">
        <p>Bolo de Chocolate</p>
    </div>

    <div class="item">
        <img src="https://images.unsplash.com/photo-1551024506-0bccd828d307">
        <p>Bolo de Morango</p>
    </div>

    <div class="item">
        <img src="https://images.unsplash.com/photo-1562440499-64c9a111f713">
        <p>Bolo de Baunilha</p>
    </div>

</section>

<div class="whatsapp">
    <a href="https://wa.me/244924887853" target="_blank">
        Pedir no WhatsApp 📲
    </a>
</div>

</div>

</body>
</html>
