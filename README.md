products = {
    "хлеб": 30,
    "молоко": 60,
    "яблоки": 100,
    "бананы": 80,
    "лавандовый раф" : 20,}

cart = {}  

print(" Доступные товары:")
for name, price in products.items():
    print(f"{name} - {price} сом")
