## Hi there 

<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Toko Sederhana</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #f5f5f5;
        }

        header {
            background: #333;
            color: white;
            padding: 20px;
            text-align: center;
            font-size: 24px;
        }

        .container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            padding: 20px;
        }

        .product {
            background: white;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 3px 6px rgba(0,0,0,0.15);
            text-align: center;
        }

        .product img {
            width: 100%;
            border-radius: 10px;
        }

        .product h3 {
            margin: 10px 0 5px;
        }

        .product p {
            color: #666;
        }

        .btn {
            display: inline-block;
            margin-top: 10px;
            padding: 10px 15px;
            background: #2196f3;
            color: white;
            border-radius: 5px;
            text-decoration: none;
        }

        .btn:hover {
            background: #0b7dda;
        }
    </style>
</head>

<body>

<header>Toko Online Sederhana</header>

<div class="container">
    <div class="product">
        <img src="https://via.placeholder.com/250" alt="Produk 1">
        <h3>Produk 1</h3>
        <p>Rp 50.000</p>
        <a class="btn" href="#">Beli</a>
    </div>

    <div class="product">
        <img src="https://via.placeholder.com/250" alt="Produk 2">
        <h3>Produk 2</h3>
        <p>Rp 75.000</p>
        <a class="btn" href="#">Beli</a>
    </div>

    <div class="product">
        <img src="https://via.placeholder.com/250" alt="Produk 3">
        <h3>Produk 3</h3>
        <p>Rp 99.000</p>
        <a class="btn" href="#">Beli</a>
    </div>

</div>

</body>
</html>



