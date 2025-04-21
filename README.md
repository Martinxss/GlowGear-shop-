<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>GlowGear - Glow Hard or Go Home</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;800&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      padding: 0;
      background: #fff7f0;
      color: #333;
      scroll-behavior: smooth;
    }

    header {
      background: linear-gradient(90deg, #ff6f61, #ff9472);
      color: #fff;
      padding: 20px;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }

    nav a {
      margin: 0 15px;
      color: #fff;
      text-decoration: none;
      font-weight: 600;
    }

    .hero {
      background: url('https://images.unsplash.com/photo-1612454371192-437d6f170cb2?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
      color: white;
      text-shadow: 1px 1px 5px #000;
      text-align: center;
      padding: 100px 5%;
    }

    .hero h2 {
      font-size: 3rem;
    }

    .hero button {
      margin-top: 20px;
      padding: 12px 28px;
      background: #fff;
      color: #ff6f61;
      border: none;
      border-radius: 50px;
      font-weight: bold;
      font-size: 16px;
      cursor: pointer;
      transition: all 0.3s;
    }

    .hero button:hover {
      background: #ff9472;
      color: #fff;
    }

    section {
      padding: 60px 5%;
      animation: fadeIn 1.5s ease-in-out;
    }

    h2 {
      text-align: center;
      color: #ff6f61;
    }

    .shop-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
      max-width: 1200px;
      margin: auto;
    }

    .shop-item {
      background: #fff;
      border-radius: 12px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.1);
      overflow: hidden;
      transition: transform 0.3s ease;
      position: relative;
    }

    .shop-item:hover {
      transform: scale(1.02);
    }

    .shop-item img {
      width: 100%;
    }

    .badge {
      position: absolute;
      top: 10px;
      left: 10px;
      background: #ff6f61;
      color: white;
      padding: 5px 10px;
      border-radius: 8px;
      font-size: 14px;
    }

    .color-swatches {
      display: flex;
      gap: 8px;
      margin-top: 10px;
    }

    .swatch {
      width: 20px;
      height: 20px;
      border-radius: 50%;
      border: 2px solid #ccc;
      cursor: pointer;
    }

    .shop-details {
      padding: 20px;
    }

    .buy-button {
      background-color: #ff6f61;
      color: #fff;
      padding: 10px 18px;
      border: none;
      cursor: pointer;
      font-size: 16px;
      border-radius: 8px;
      margin-top: 10px;
      transition: background 0.3s;
    }

    .buy-button:hover {
      background-color: #e85a50;
    }

    .insta-gallery {
      display: flex;
      gap: 10px;
      overflow-x: auto;
      margin-top: 40px;
      padding: 0 5%;
    }

    .insta-gallery img {
      width: 150px;
      height: 150px;
      border-radius: 12px;
      object-fit: cover;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    footer {
      background-color: #ff6f61;
      color: #fff;
      text-align: center;
      padding: 20px;
      font-size: 14px;
    }
  </style>
</head>
<body>

<header>
  <h1>GlowGear</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#shop">Shop</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<section id="home" class="hero">
  <h2>Glow Hard or Go Home</h2>
  <p>Power up your glow game with our elite collection.</p>
  <button>Shop Now</button>
</section>

<section id="about">
  <h2>About GlowGear</h2>
  <p style="max-width: 800px; margin: auto; text-align: center;">
    At GlowGear, we don't do average. Our premium grooming and self-care tools are made for kings and queens ready to dominate. Because glow isn't optional—it's your signature.
  </p>
</section>

<section id="shop">
  <h2>🔥 Featured Products</h2>
  <div class="shop-grid">
    <div class="shop-item">
      <span class="badge">🔥 Hot</span>
      <img src="https://m.media-amazon.com/images/I/61oe0XccCoL._AC_SL1500_.jpg" alt="LED Mask">
      <div class="shop-details">
        <h3>LED Face Mask</h3>
        <p>Multi-light therapy for flawless glow.</p>
        <p><strong>€49.99</strong></p>
        <div class="color-swatches">
          <div class="swatch" style="background:pink;"></div>
          <div class="swatch" style="background:blue;"></div>
          <div class="swatch" style="background:black;"></div>
        </div>
        <button class="buy-button">Add to Cart</button>
      </div>
    </div>

    <div class="shop-item">
      <span class="badge">💎 Premium</span>
      <img src="https://m.media-amazon.com/images/I/81FA7H2XwXL._AC_SL1500_.jpg" alt="Beard Kit">
      <div class="shop-details">
        <h3>Beard Grooming Kit</h3>
        <p>Everything your beard ever wanted.</p>
        <p><strong>€29.99</strong></p>
        <div class="color-swatches">
          <div class="swatch" style="background:#333;"></div>
          <div class="swatch" style="background:brown;"></div>
        </div>
        <button class="buy-button">Add to Cart</button>
      </div>
    </div>
  </div>
</section>

<section class="insta-gallery">
  <img src="https://images.unsplash.com/photo-1596464716121-d4bbf38af8b1?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=&ixlib=rb-4.0.3&q=80&w=400" />
  <img src="https://images.unsplash.com/photo-1588776814546-79cfb2505564?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=&ixlib=rb-4.0.3&q=80&w=400" />
  <img src="https://images.unsplash.com/photo-1594824476967-48c8f010d31a?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=&ixlib=rb-4.0.3&q=80&w=400" />
</section>

<section id="contact">
  <h2>📞 Contact</h2>
  <p style="text-align:center;">Phone: +371 27301085</p>
  <p style="text-align:center;">Email: <a href="mailto:lvtavamamma0@gmail.com">lvtavamamma0@gmail.com</a></p>
</section>

<footer>
  <p>&copy; 2025 GlowGear. Built with vibes, coded with love 💅</p>
</footer>

</body>
</html>
