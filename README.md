<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TransparEyes Boutique</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 20px;
    }
    .product {
      display: inline-block;
      margin: 20px;
      border: 1px solid #ddd;
      border-radius: 10px;
      padding: 15px;
      width: 200px;
    }
    .product img {
      width: 100%;
      height: auto;
      border-radius: 10px;
    }
    .btn {
      background-color: #007BFF;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 5px;
      cursor: pointer;
    }
    .btn:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>
  <h1>Bienvenue sur TransparEyes Boutique</h1>
  <div id="product-list"></div>

  <script>
    // Dynamically render product cards
    const products = [
      { name: "Lunettes Transparentes Modèle 1", price: 49.99, image: "https://via.placeholder.com/200" },
      { name: "Lunettes Transparentes Modèle 2", price: 59.99, image: "https://via.placeholder.com/200" },
      { name: "Lunettes Transparentes Modèle 3", price: 39.99, image: "https://via.placeholder.com/200" }
    ];

    const productList = document.getElementById('product-list');

    products.forEach(product => {
      const productCard = `
        <div class="product">
          <img src="${product.image}" alt="${product.name}">
          <h2>${product.name}</h2>
          <p>Prix : €${product.price}</p>
          <button class="btn">Acheter</button>
        </div>
      `;
      productList.innerHTML += productCard;
    });
  </script>
</body>
</html>
