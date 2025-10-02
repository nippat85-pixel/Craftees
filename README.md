<html>
  <body>
  <header>
    <h1>🖌️ Craftees</h1>
    <p>Unique block-printed shirts — all proceeds go to the Children's Hospital ❤️</p>
  </header>

  <section class="products" aria-label="Available Shirts for Sale">

    <div class="product" role="region" aria-labelledby="product1-title">
      <img src="https://via.placeholder.com/200x200?text=Sun+Design" alt="Sunburst block-printed shirt" />
      <h3 id="product1-title">Sunburst Tee</h3>
      <p>$4.00</p>

      <label for="size1">Size:</label>
      <select id="size1" class="size-select" aria-describedby="size-desc1">
        <option value="S">Small</option>
        <option value="M" selected>Medium</option>
        <option value="L">Large</option>
      </select>
      <small id="size-desc1">Select your shirt size</small>

      <button>Buy Now</button>
    </div>

    <div class="product" role="region" aria-labelledby="product2-title">
      <img src="https://via.placeholder.com/200x200?text=Moon+Design" alt="Midnight Moon block-printed shirt" />
      <h3 id="product2-title">Midnight Moon Tee</h3>
      <p>$5.00</p>

      <label for="size2">Size:</label>
      <select id="size2" class="size-select" aria-describedby="size-desc2">
        <option value="S">Small</option>
        <option value="M" selected>Medium</option>
        <option value="L">Large</option>
      </select>
      <small id="size-desc2">Select your shirt size</small>

      <button>Buy Now</button>
    </div>

    <div class="product" role="region" aria-labelledby="product3-title">
      <img src="https://via.placeholder.com/200x200?text=Custom+Design" alt="Custom block-printed shirt" />
      <h3 id="product3-title">Custom Print Tee</h3>
      <p>$5.50</p>

      <label for="size3">Size:</label>
      <select id="size3" class="size-select" aria-describedby="size-desc3">
        <option value="S">Small</option>
        <option value="M" selected>Medium</option>
        <option value="L">Large</option>
      </select>
      <small id="size-desc3">Select your shirt size</small>

      <button>Buy Now</button>
    </div>

  </section>

  <section class="about" aria-label="About CraftTees">
    <h2>💬 About CraftTees</h2>
    <p>Hi! I'm Rithi, a passionate artist who hand-block prints every shirt. I started CraftTees to raise money for the Children's Hospital and share my art. Each shirt is unique — just like the kids we’re helping 💖</p>
  </section>

/* Reset some basic styles */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

/* Body and fonts */
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #fffaf9;  /* soft off-white */
  color: #333;
  line-height: 1.6;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

/* Header */
header {
  background-color: #f9c5d1; /* gentle pink */
  color: #4a2c2a; /* dark brown-ish */
  text-align: center;
  padding: 2.5rem 1rem;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}

header h1 {
  font-size: 2.5rem;
  margin-bottom: 0.5rem;
}

header p {
  font-size: 1.2rem;
  font-weight: 500;
}

/* Main products section */
.products {
  flex: 1;
  padding: 2rem 1rem;
  max-width: 960px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  justify-content: center;
}

/* Each product card */
.product {
  background-color: #fff;
  border-radius: 12px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.08);
  width: 220px;
  padding: 1rem;
  text-align: center;
  transition: transform 0.2s ease;
  cursor: default;
}

.product:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 16px rgba(0,0,0,0.15);
}

/* Product image */
.product img {
  width: 100%;
  border-radius: 8px;
  margin-bottom: 1rem;
}

/* Product title */
.product h3 {
  font-size: 1.25rem;
  color: #4a2c2a;
  margin-bottom: 0.5rem;
}

/* Price */
.product p {
  font-weight: 600;
  color: #b85c68;  /* rosy red */
  margin-bottom: 1rem;
  font-size: 1.1rem;
}

/* Buy Now button */
button {
  background-color: #f67280;  /* bright raspberry */
  color: white;
  border: none;
  padding: 0.65rem 1.5rem;
  border-radius: 6px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #d95869;
}

/* About section */
.about {
  background-color: #fff;
  max-width: 700px;
  margin: 3rem auto;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.05);
  text-align: center;
  color: #4a2c2a;
}

.about h2 {
  font-size: 1.8rem;
  margin-bottom: 1rem;
}

.about p {
  font-size: 1.1rem;
  line-height: 1.5;
}

/* Footer */
footer {
  background-color: #f9c5d1;
  color: #4a2c2a;
  text-align: center;
  padding: 1.5rem 1rem;
  font-size: 0.9rem;
  box-shadow: 0 -2px 6px rgba(0,0,0,0.1);
}

footer a {
  color: #4a2c2a;
  text-decoration: underline;
}

footer a:hover {
  color: #f67280;
}

/* Responsive tweaks */
@media (max-width: 600px) {
  .products {
    flex-direction: column;
    align-items: center;
  }

  .product {
    width: 90%;
  }
}
// For each product card, handle button click and size selection
document.querySelectorAll(".product").forEach(product => {
  const button = product.querySelector("button");
  const sizeSelect = product.querySelector(".size-select");

  button.addEventListener("click", () => {
    const size = sizeSelect ? sizeSelect.value : "N/A";
    const productName = product.querySelector("h3").innerText;
    alert(`Thanks for buying the ${productName} (Size: ${size})! ❤️ All funds go to the Children's Hospital.`);
  });
});
