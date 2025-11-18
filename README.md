<!DOCTYPE html><html lang="id">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Toko Online Sederhana</title>
    <style>
        body { font-family: Arial, sans-serif; padding: 20px; background: #f7f7f7; }
        h1 { text-align: center; }
        .product { background: white; padding: 15px; border-radius: 10px; box-shadow: 0 2px 5px rgba(0,0,0,0.1); margin-bottom: 10px; }
        button { padding: 6px 12px; cursor: pointer; border-radius: 6px; border: none; background: #2d89ef; color: white; }
        input { padding: 5px; width: 100px; }
    </style>
</head>
<body>
    <h1>Toko Online – Edit Produk & Harga</h1><div id="product-list"></div>

<h2>Tambah Produk</h2>
<input id="newName" placeholder="Nama produk" />
<input id="newPrice" placeholder="Harga" type="number" />
<button onclick="addProduct()">Tambah</button>

<script>
    let products = [
        { id: 1, name: "Produk A", price: 50000 },
        { id: 2, name: "Produk B", price: 75000 }
    ];

    function renderProducts() {
        const list = document.getElementById("product-list");
        list.innerHTML = "";

        products.forEach(p => {
            const div = document.createElement("div");
            div.className = "product";
            div.innerHTML = `
                <b>${p.name}</b><br>
                Harga: Rp <input type="number" value="${p.price}" onchange="updatePrice(${p.id}, this.value)"> <br><br>
                <button onclick="deleteProduct(${p.id})">Hapus</button>
            `;
            list.appendChild(div);
        });
    }

    function updatePrice(id, newPrice) {
        const product = products.find(p => p.id === id);
        if (product) product.price = parseInt(newPrice);
    }

    function addProduct() {
        const name = document.getElementById("newName").value;
        const price = document.getElementById("newPrice").value;
        if (!name || !price) return alert("Lengkapi nama dan harga!");

        products.push({ id: Date.now(), name, price: parseInt(price) });
        renderProducts();
    }

    function deleteProduct(id) {
        products = products.filter(p => p.id !== id);
        renderProducts();
    }

    renderProducts();
</script>

</body>
</html>



