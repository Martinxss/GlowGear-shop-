<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>GlowGear - Self-Care Store</title>
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
      background: url('glowgear_banner.jpg') no-repeat center center/cover;
      color: white;
      text-shadow: 1px 1px 5px #000;
      text-align: center;
      padding: 100px 5%;
    }

    section {
      padding: 60px 5%;
      animation: fadeIn 1.5s ease-in-out;
    }

    h2 {
      text-align: center;
      color: #ff6f61;
    }

    .shop-item {
      background: #fff;
      border-radius: 12px;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      margin: 30px auto;
      max-width: 900px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.1);
      overflow: hidden;
      transition: transform 0.3s ease;
    }

    .shop-item:hover {
      transform: scale(1.02);
    }

    .shop-item img {
      width: 100%;
      max-width: 300px;
    }

    .shop-details {
      padding: 20px;
      flex: 1;
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

    .cart {
      position: fixed;
      right: 0;
      top: 80px;
      width: 300px;
      background: white;
      box-shadow: -2px 0 10px rgba(0,0,0,0.2);
      padding: 20px;
      display: none;
      z-index: 1001;
    }

    .show-cart {
      display: block;
    }

    .cart-toggle {
      position: fixed;
      right: 20px;
      top: 20px;
      background: #ff9472;
      color: white;
      border: none;
      padding: 12px 20px;
      border-radius: 50px;
      z-index: 1002;
      cursor: pointer;
      font-weight: 600;
      box-shadow: 0 2px 10px rgba(0,0,0,0.2);
    }

    footer {
      background-color: #ff6f61;
      color: #fff;
      text-align: center;
      padding: 20px;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    ul#cart-items {
      padding-left: 18px;
    }

    .cart button {
      background: #eee;
      color: #444;
      border: none;
      padding: 4px 8px;
      margin-left: 8px;
      cursor: pointer;
      font-size: 12px;
    }

    @media (max-width: 768px) {
      .shop-item {
        flex-direction: column;
        text-align: center;
      }
      .shop-item img {
        max-width: 100%;
      }
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

  <button class="cart-toggle" onclick="toggleCart()">Cart (<span id="cart-count">0</span>)</button>

  <div class="cart" id="cart">
    <h3>Your Cart</h3>
    <ul id="cart-items"></ul>
    <p><strong>Total: €<span id="cart-total">0.00</span></strong></p>
  </div>

  <section id="home" class="hero">
    <h2>Glow up with GlowGear</h2>
    <p>High-quality self-care products for men & women. Look good. Feel better.</p>
  </section>

  <section id="about">
    <h2>About GlowGear</h2>
    <p style="max-width: 800px; margin: auto; text-align: center;">
      GlowGear is your destination for premium grooming and skincare tools. We combine style with function to help you feel and look your best. Every product is hand-picked for quality, ease, and aesthetics.
    </p>
    <div style="display:flex; justify-content: center; margin-top: 30px;">
      <img src="glowgear_helper.jpg" alt="Lifestyle Image" style="max-width: 80%; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.2);" />
    </div>
  </section>

  <section id="shop">
    <h2>Shop Products</h2>

    <div class="shop-item">
      <img src="https://via.placeholder.com/300x300.png?text=LED+Face+Mask" alt="LED Face Mask" />
      <div class="shop-details">
        <h3>LED Face Mask</h3>
        <p>Light therapy mask to improve acne, texture and glow.</p>
        <p><strong>€49.99</strong></p>
        <button class="buy-button" onclick="addToCart('LED Face Mask', 49.99)">Add to Cart</button>
      </div>
    </div>

    <div class="shop-item">
      <img src="glowgear_beardkit.png" alt="Beard Grooming Kit" />
      <div class="shop-details">
        <h3>Beard Grooming Kit</h3>
        <p>Includes oil, balm, scissors, comb, wash. Everything for the perfect beard.</p>
        <p><strong>€29.99</strong></p>
        <button class="buy-button" onclick="addToCart('Beard Grooming Kit', 29.99)">Add to Cart</button>
      </div>
    </div>

    <div class="shop-item">
      <img src="https://via.placeholder.com/300x300.png?text=Silk+Hair+Wrap" alt="Silk Hair Wrap" />
      <div class="shop-details">
        <h3>Silk Hair Wrap</h3>
        <p>Protect your curls & shine while sleeping. No more frizz or damage.</p>
        <p><strong>€19.99</strong></p>
        <button class="buy-button" onclick="addToCart('Silk Hair Wrap', 19.99)">Add to Cart</button>
      </div>
    </div>
  </section>

  <section id="contact">
    <h2>Contact Us</h2>
    <p style="text-align:center;">Phone: +371 27301085</p>
    <p style="text-align:center;">Email: <a href="mailto:lvtavamamma0@gmail.com">lvtavamamma0@gmail.com</a></p>
  </section>

  <footer>
    <p>&copy; 2025 GlowGear. Built with self-love and style.</p>
  </footer>

  <script>
    let cartItemsMap = {};

    function addToCart(name, price) {
      if (cartItemsMap[name]) {
        cartItemsMap[name].quantity += 1;
      } else {
        cartItemsMap[name] = { price: price, quantity: 1 };
      }
      updateCart();
    }

    function updateCart() {
      const cartList = document.getElementById('cart-items');
      const totalElement = document.getElementById('cart-total');
      const countElement = document.getElementById('cart-count');
      cartList.innerHTML = '';
      let total = 0;
      let itemCount = 0;

      for (const [name, item] of Object.entries(cartItemsMap)) {
        const li = document.createElement('li');
        li.innerHTML = `
          ${name} (x${item.quantity}) - €${(item.price * item.quantity).toFixed(2)}
          <button onclick="removeFromCart('${name}')">Remove</button>
        `;
        cartList.appendChild(li);
        total += item.price * item.quantity;
        itemCount += item.quantity;
      }

      totalElement.textContent = total.toFixed(2);
      countElement.textContent = itemCount;
    }

    function removeFromCart(name) {
      if (cartItemsMap[name]) {
        cartItemsMap[name].quantity -= 1;
        if (cartItemsMap[name].quantity <= 0) {
          delete cartItemsMap[name];
        }
        updateCart();
      }
    }

    function toggleCart() {
      const cartElement = document.getElementById('cart');
      cartElement.classList.toggle('show-cart');
    }
  </script>

</body>
</html>
