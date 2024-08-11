# Clases
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tienda de Cuentas de Streaming</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #333;
            color: white;
            padding: 10px 0;
            text-align: center;
        }
        .container {
            width: 80%;
            margin: 20px auto;
        }
        .product {
            border: 1px solid #ddd;
            background-color: white;
            padding: 10px;
            margin-bottom: 20px;
            border-radius: 5px;
        }
        .product img {
            width: 100%;
            height: auto;
        }
        .product h2 {
            font-size: 1.5em;
        }
        .product p {
            font-size: 1.2em;
        }
        form {
            margin-top: 20px;
        }
        form input, form button {
            padding: 10px;
            font-size: 1em;
        }
        form input[type="text"] {
            width: calc(100% - 22px);
        }
        form button {
            background-color: #333;
            color: white;
            border: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <h1>Tienda de Cuentas de Streaming</h1>
    </header>
    <div class="container">
        <div class="product">
            <img src="netflix.jpg" alt="Netflix">
            <h2>Cuenta de Netflix</h2>
            <p>Precio: $10</p>
            <button onclick="buyProduct('Netflix')">Comprar</button>
        </div>
        <div class="product">
            <img src="hulu.jpg" alt="Hulu">
            <h2>Cuenta de Hulu</h2>
            <p>Precio: $8</p>
            <button onclick="buyProduct('Hulu')">Comprar</button>
        </div>
        <div class="product">
            <img src="disney.jpg" alt="Disney+">
            <h2>Cuenta de Disney+</h2>
            <p>Precio: $12</p>
            <button onclick="buyProduct('Disney+')">Comprar</button>
        </div>

        <form id="purchaseForm">
            <input type="text" id="email" placeholder="Introduce tu email" required>
            <button type="button" onclick="submitForm()">Confirmar Compra</button>
        </form>
    </div>

    <script>
        function buyProduct(product) {
            alert('Producto: ' + product);
        }

        function submitForm() {
            const email = document.getElementById('email').value;
            if (email) {
                alert('Compra confirmada. Te hemos enviado un email a: ' + email);
                document.getElementById('email').value = '';
            } else {
                alert('Por favor, introduce tu email.');
            }
        }
    </script>
</body>
</html>
