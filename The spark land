#  THE SPARK LAND<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>متجر الملابس الشبابية</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>متجر الملابس الشبابية</h1>
    </header>
    <main>
        <section id="products">
            <!-- المنتجات سيتم إضافتها هنا عبر JavaScript -->
        </section>
        <section id="cart">
            <h2>عربة التسوق</h2>
            <ul id="cart-items"></ul>
            <button onclick="checkout()">الدفع</button>
        </section>
    </main>
    <script src="app.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    background-color: #0a0a23;
    color: #f0f0f0;
    margin: 0;
    padding: 0;
}

header {
    background-color: #1a1a40;
    padding: 20px;
    text-align: center;
}

main {
    padding: 20px;
}

#products {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
}

.product {
    background-color: #2c2c54;
    padding: 15px;
    border-radius: 10px;
    width: 200px;
    text-align: center;
}

.product button {
    background-color: #ffb142;
    border: none;
    padding: 10px;
    border-radius: 5px;
    cursor: pointer;
}

#cart {
    margin-top: 20px;
}

#cart-items {
    list-style-type: none;
    padding: 0;
}

#cart-items li {
    background-color: #3d3d6b;
    padding: 10px;
    margin: 5px 0;
    border-radius: 5px;
}
const products = [
    { id: 1, name: "تيشيرت أزرق", price: 50 },
    { id: 2, name: "جينز أسود", price: 100 },
    { id: 3, name: "جاكيت ذهبي", price: 150 }
];

const cart = [];

function renderProducts() {
    const productsSection = document.getElementById('products');
    productsSection.innerHTML = '';
    products.forEach(product => {
        const productDiv = document.createElement('div');
        productDiv.className = 'product';
        productDiv.innerHTML = `
            <h3>${product.name}</h3>
            <p>السعر: $${product.price}</p>
            <button onclick="addToCart(${product.id})">إضافة إلى العربة</button>
        `;
        productsSection.appendChild(productDiv);
    });
}

function addToCart(productId) {
    const product = products.find(p => p.id === productId);
    cart.push(product);
    renderCart();
}

function renderCart() {
    const cartItems = document.getElementById('cart-items');
    cartItems.innerHTML = '';
    cart.forEach(item => {
        const li = document.createElement('li');
        li.textContent = `${item.name} - $${item.price}`;
        cartItems.appendChild(li);
    });
}

function checkout() {
    alert('شكرًا لشرائك! سيتم تحويلك إلى صفحة الدفع.');
    // هنا يمكنك إضافة التكامل مع بوابة الدفع
}

document.addEventListener('DOMContentLoaded', renderProducts);
from flask import Flask, jsonify, request

app = Flask(__name__)

products = [
    {"id": 1, "name": "تيشيرت أزرق", "price": 50},
    {"id": 2, "name": "جينز أسود", "price": 100},
    {"id": 3, "name": "جاكيت ذهبي", "price": 150}
]

@app.route('/api/products', methods=['GET'])
def get_products():
    return jsonify(products)

@app.route('/api/checkout', methods=['POST'])
def checkout():
    data = request.json
    # هنا يمكنك إضافة منطق الدفع
    return jsonify({"message": "تمت عملية الدفع بنجاح!"})

if __name__ == '__main__':
    app.run(debug=True)
    git init
     git add .
     git commit -m "Initial commit"
     git branch -M main
     git remote add origin https://github.com/username/youth-clothing-store.git
     git push -u origin mainpython app.py
