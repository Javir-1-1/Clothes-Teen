# Clothes-Teen
<!doctype html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="ClothesTeen: Moda juvenil a tu alcance. Encuentra lo último en tendencias para hombres y mujeres.">
    <meta name="keywords" content="moda juvenil, ropa, hombres, mujeres, tienda de ropa">
    <title>ClothesTeen</title>
    <link rel="stylesheet" href="ClothesTeen.css">
</head>
<body id="mainBody" style="overflow: auto;">
    <header>
        <center><h1>ClothesTeen</h1></center>
        <center>
            <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Logo de Clothes Teen.png" alt="Logotipo de ClothesTeen" width="200" title="Nuestro Logo">
        </center>
        <nav>
            <ul>
                <li><a href="Men.html">Hombre</a></li>
                <li><a href="Women.html">Mujer</a></li>
            </ul>
        </nav>
    </header>

    <hr>

    <div class="filter-container">
        <button class="filter-button" onclick="filterCategory('all')">Todos</button>
        <button class="filter-button" onclick="filterCategory('ropa')">Ropa</button>
        <button class="filter-button" onclick="filterCategory('zapatos')">Zapatos</button>
        <button class="filter-button" onclick="filterCategory('accesorios')">Accesorios</button>
    </div>

    <center>
        <div class="search-container">
            <label for="searchBar" hidden>Buscar productos:</label>
            <input type="text" id="searchBar" class="search-bar" placeholder="Buscar productos..." oninput="showSuggestions()">
            <div id="suggestions" class="suggestions-box"></div>
            <button class="search-button" onclick="searchProducts()">Buscar</button>
        </div>
    </center>

    <div class="cart-container">
        <button class="cart-button" onclick="toggleCart()">
            <i class="fas fa-shopping-cart"></i> 🛒Carrito (<span id="cartCount">0</span>)
        </button>
        <div id="cartDropdown" class="cart-dropdown">
            <p id="cartContent">Tu carrito está vacío.</p>
            <button class="filter-button" onclick="clearCart()">Vaciar carrito</button>
            <button class="filter-button" onclick="goToCart()">Ir a comprar</button>
        </div>
    </div>

    <hr>

    <section class="products-container">
        <h3>Productos disponibles</h3>
        <div id="products" class="product-list">
            <div class="product zapatos">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Zapatos deportivos.png" alt="Camisa Azul" width="165">
                <p>Zapatos runner - $85</p>
                <p>Tallas: 39, 40, 42</p>
                <button class="filter-button" onclick="addToCart('Zapatos runner', 25)">Agregar al carrito</button>
            </div>
            
            <div class="product zapatos">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Zapatos de Futbol.png" alt="Camisa Verde" width="165">
                <p>Zapatos de futbol - $70</p>
                <p>Tallas: 39, 40, 42</p>
                <button class="filter-button" onclick="addToCart('Zapatos de futbol', 30)">Agregar al carrito</button>
            </div>
            
            <div class="product zapatos">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Zapatos de Baloncesto.png" alt="Zapatos Deportivos" width="250">
                <p>Zapatos de baloncesto - $80</p>
                <p>Tallas: 39, 40, 42</p>
                <button class="filter-button" onclick="addToCart('Zapatos de baloncesto', 45)">Agregar al carrito</button>
            </div>
            <div class="product zapatos">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Zapato.png" alt="Chaqueta de Cuero" width="275">
                <p>Zapato - $90</p>
                <p>Tallas: 39, 40, 42</p>
                <button class="filter-button" onclick="addToCart('Zapato', 120)">Agregar al carrito</button>
            </div>
			
			            <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Pantalon 1.png" alt="Camisa Azul" width="165">
                <p>Pantalon - $35</p>
                <p>Tallas: S, M, L</p>
                <p>Colores: Negro</p>
                <button class="filter-button" onclick="addToCart('Pantalon', 35)">Agregar al carrito</button>
            </div>
            
            <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Pantalon 2.png" alt="Camisa Verde" width="165">
                <p>Pantalon Jeans - $25</p>
                <p>Tallas: M, L</p>
                <p>Colores: Azul y Negro</p>
                <button class="filter-button" onclick="addToCart('Pantalon Jeans', 25)">Agregar al carrito</button>
            </div>
            
            <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Pantalon 3.png" alt="Zapatos Deportivos" width="95">
                <p>Pantalon Jogger - $35</p>
                <p>Tallas: 39, 40, 42</p>
                <p>Colores: Caqui y Gris</p>
                <button class="filter-button" onclick="addToCart('Pantalon Jogger', 35)">Agregar al carrito</button>
            </div>

            <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Pantalon 4.png" alt="Chaqueta de Cuero" width="165">
                <p>Pantalon Casual - $40</p>
                <p>Tallas: M, L, XL</p>
                <p>Colores: Corinto y Blanco</p>
                <button class="filter-button" onclick="addToCart('Pantalon Casual', 40)">Agregar al carrito</button>
            </div>
      <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Hoodie 1.png" alt="Camisa Azul" width="165">
                <p>Hoodie CAT - $35</p>
                <p>Tallas: S, M, L</p>
                <p>Colores: Negro</p>
                <button class="filter-button" onclick="addToCart('Hoodie CAT', 35)">Agregar al carrito</button>
            </div>
            
            <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Hoodie 2.png" alt="Camisa Verde" width="125">
                <p>Hoodie - $25</p>
                <p>Tallas: M, L</p>
                <p>Colores: Azul y Negro</p>
                <button class="filter-button" onclick="addToCart('Hoodie', 25)">Agregar al carrito</button>
            </div>
            
            <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Hoodie 3.png" alt="Zapatos Deportivos" width="120">
                <p>Hoodie Adidas - $35</p>
                <p>Tallas: 39, 40, 42</p>
                <p>Colores: Caqui y Gris</p>
                <button class="filter-button" onclick="addToCart('Hoodie Adidas', 35)">Agregar al carrito</button>
            </div>

            <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Hoodie 4.png" alt="Chaqueta de Cuero" width="125">
                <p>Hoodie Calvin Klein - $40</p>
                <p>Tallas: M, L, XL</p>
                <p>Colores: Corinto y Blanco</p>
                <button class="filter-button" onclick="addToCart('Hoodie Calvin Klein', 40)">Agregar al carrito</button>
            </div>
			
			     <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Camisa 1.png" alt="Camisa Azul" width="165">
                <p>Camisa Psycho Bunny - $85</p>
                <p>Tallas: S, M, L</p>
                <p>Colores: Azul</p>
                <button class="filter-button" onclick="addToCart('Camisa Psycho Bunny', 25)">Agregar al carrito</button>
            </div>
            
            <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Camisa 2.png" alt="Camisa Verde" width="160">
                <p>Camisa Boss - $70</p>
                <p>Tallas: M, L</p>
                <p>Colores: Verde, Negro</p>
                <button class="filter-button" onclick="addToCart('Camisa Boss', 30)">Agregar al carrito</button>
            </div>
            
            <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Camisa 3.png" alt="Zapatos Deportivos" width="215">
                <p>Playera Nike - $80</p>
                <p>Tallas: 39, 40, 42</p>
                <p>Colores: Blanco, Gris</p>
                <button class="filter-button" onclick="addToCart('Playera Nike', 45)">Agregar al carrito</button>
            </div>

            <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Camisa 4.png" alt="Chaqueta de Cuero" width="215">
                <p>Playera Adidas - $90</p>
                <p>Tallas: M, L, XL</p>
                <p>Colores: Negro, Marrón</p>
                <button class="filter-button" onclick="addToCart('Camisa Adidas', 120)">Agregar al carrito</button>
            </div>


        </div>
    </section>

    <div id="notification"></div>

    <footer>
        <div class="contact-info">
            <p>Teléfono de contacto: 5973-5460</p>
        </div>
        <div class="social-media">
            <a  href="ClothesTeen.html"><img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Instagram.png" width="50"></a> 
			<a href="#"><img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Facebook.png" width="50"></a> 
			<a href="#"><img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\X.png" width="50"></a>
        </div>
		
		<p>&copy; 2024 ClothesTeen. Todos los derechos reservados.</p>
		<br>
		   <center>
            <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Logo de ClothesTeen en negro.png" alt="Logotipo de ClothesTeen" width="200" title="Nuestro Logo">
        </center>
    </footer>

    <script>
        let cart = JSON.parse(localStorage.getItem('cart')) || [];
        let reviews = JSON.parse(localStorage.getItem('reviews')) || [];

        function toggleCart() {
            let cartDropdown = document.getElementById('cartDropdown');
            cartDropdown.style.display = (cartDropdown.style.display === 'block') ? 'none' : 'block';
        }

        function clearCart() {
            cart = [];
            updateCart();
        }

        function goToCart() {
            window.location.href = "carrito.html";
        }

        function updateCart() {
            localStorage.setItem('cart', JSON.stringify(cart));
            let cartCount = document.getElementById('cartCount');
            let cartContent = document.getElementById('cartContent');
            cartCount.innerText = cart.length;
            cartContent.innerHTML = cart.length === 0 ? "Tu carrito está vacío." : cart.map(item => `${item.name} - $${item.price}`).join('<br>');
        }

        function addToCart(productName, productPrice) {
            cart.push({ name: productName, price: productPrice });
            updateCart();
        }

        function filterCategory(category) {
            let products = document.getElementsByClassName('product');
            for (let i = 0; i < products.length; i++) {
                if (category === 'all' || products[i].classList.contains(category)) {
                    products[i].style.display = 'block';
                } else {
                    products[i].style.display = 'none';
                }
            }
        }

        function showSuggestions() {
            let input = document.getElementById('searchBar').value.toLowerCase();
            let suggestions = document.getElementById('suggestions');
            let products = document.getElementsByClassName('product');
            suggestions.innerHTML = '';
            for (let i = 0; i < products.length; i++) {
                let productName = products[i].querySelector('p').innerText.toLowerCase();
                if (productName.includes(input)) {
                    let suggestion = document.createElement('div');
                    suggestion.className = 'suggestion';
                    suggestion.innerText = productName;
                    suggestion.onclick = function () {
                        searchBar.value = productName;
                        searchProducts();
                    };
                    suggestions.appendChild(suggestion);
                }
            }
        }

        function searchProducts() {
            let input = document.getElementById('searchBar').value.toLowerCase();
            let products = document.getElementsByClassName('product');
            for (let i = 0; i < products.length; i++) {
                let productName = products[i].querySelector('p').innerText.toLowerCase();
                products[i].style.display = productName.includes(input) ? 'block' : 'none';
            }
        }

        updateCart();
    </script>
</body>
</html>
