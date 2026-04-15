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
while True:
    item = input("\nВведите товар (или 'стоп'): ").lower()
    if item == "стоп":
        break
    if item not in products:
        print(" Такого товара нет")
        continue
    try:
        quantity = int(input("Сколько штук: "))
        if quantity <= 0:
            print(" Количество должно быть больше 0")
            continue
    except:
        print(" Введите число")
        continue
    if item in cart:
        cart[item] += quantity
    else:
        cart[item] = quantity
    print(f" Добавлено: {item} x{quantity}")
print("\n Чек:")
total = 0
for item, quantity in cart.items():
    price = products[item]
    cost = price * quantity
    total += cost
    print(f"{item} x{quantity} = {cost} сомиков")

print(f"\n Итого: {total} сомиков")
