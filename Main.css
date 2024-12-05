const products = [
    { id: 1, name: "Apples", price: 3.99, img: "https://i.pinimg.com/736x/1e/fe/06/1efe0654537adf9efa4bbdcec5eb433c.jpg" },
    { id: 2, name: "Bananas", price: 1.49, img: "https://i.pinimg.com/736x/a3/37/0b/a3370bfbc03bc8de595f417f08f7fa5e.jpg" },
    { id: 3, name: "Carrots", price: 2.99, img: "https://i.pinimg.com/736x/8b/dd/4b/8bdd4b8429f34fadc73a2db1f22c7bd2.jpg" },
    { id: 4, name: "Detergent", price: 7.99, img: "https://i.pinimg.com/736x/03/3e/07/033e0706dee82fe8b7912dcf28b49423.jpg" },
    { id: 5, name: "Milk", price: 4.49, img: "https://i.pinimg.com/736x/03/1f/dc/031fdcbced2bd23207537f74f8bc6d81.jpg" },
    { id: 6, name: "Eggs", price: 5.99, img: "https://i.pinimg.com/736x/4c/85/fe/4c85feaa9047e6dc3f6b079e3eae171c.jpg" },
  ];
  
  const cart = JSON.parse(localStorage.getItem("cart")) || [];
  const wishlist = JSON.parse(localStorage.getItem("wishlist")) || [];
  
  function renderProducts() {
    const productList = document.getElementById("product-list");
    productList.innerHTML = "";
    products.forEach((product) => {
      const productDiv = document.createElement("div");
      productDiv.className = "product";
      productDiv.innerHTML = `
        <img src="${product.img}" alt="${product.name}">
        <h2>${product.name}</h2>
        <p>$${product.price.toFixed(2)}</p>
        <button onclick="addToCart(${product.id})">Add to Cart</button>
        <button onclick="addToWishlist(${product.id})">Add to Wishlist</button>
      `;
      productList.appendChild(productDiv);
    });
  }
  
  function addToCart(productId) {
    const product = products.find((p) => p.id === productId);
    if (!cart.find((item) => item.id === productId)) {
      cart.push(product);
      localStorage.setItem("cart", JSON.stringify(cart));
      alert(${product.name} added to cart!);
    } else {
      alert(${product.name} is already in your cart!);
    }
  }
  
  function addToWishlist(productId) {
    const product = products.find((p) => p.id === productId);
    if (!wishlist.find((item) => item.id === productId)) {
      wishlist.push(product);
      localStorage.setItem("wishlist", JSON.stringify(wishlist));
      alert(${product.name} added to wishlist!);
    } else {
      alert(${product.name} is already in your wishlist!);
    }
  }
  
  function renderCart() {
    const cartList = document.getElementById("cart");
    cartList.innerHTML = "";
    if (cart.length === 0) {
      cartList.innerHTML = "<p>Your cart is empty!</p>";
      return;
    }
    cart.forEach((item) => {
      const cartDiv = document.createElement("div");
      cartDiv.className = "cart-item";
      cartDiv.innerHTML = `
        <img src="${item.img}" alt="${item.name}" style="width: 100px; height: 100px;">
        <h2>${item.name}</h2>
        <p>$${item.price.toFixed(2)}</p>
        <button onclick="removeFromCart(${item.id})">Remove</button>
      `;
      cartList.appendChild(cartDiv);
    });
  }
  
  function removeFromCart(productId) {
    const index = cart.findIndex((item) => item.id === productId);
    if (index !== -1) {
      cart.splice(index, 1);
      localStorage.setItem("cart", JSON.stringify(cart));
      alert("Item removed from cart!");
      renderCart();
    }
  }
    function renderWishlist() {
    const wishlistList = document.getElementById("wishlist");
    wishlistList.innerHTML = "";
    if (wishlist.length === 0) {
      wishlistList.innerHTML = "<p>Your wishlist is empty!</p>";
      return;
    }
    wishlist.forEach((item) => {
      const wishlistDiv = document.createElement("div");
      wishlistDiv.className = "wishlist-item";
      wishlistDiv.innerHTML = `
        <img src="${item.img}" alt="${item.name}">
        <h2>${item.name}</h2>
        <p>$${item.price.toFixed(2)}</p>
      `;
      wishlistList.appendChild(wishlistDiv);
    });
  }
  
  if (document.getElementById("product-list")) renderProducts();
  if (document.getElementById("cart")) renderCart();
  if (document.getElementById("wishlist")) renderWishlist();