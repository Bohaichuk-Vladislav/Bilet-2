# Bilet-2
# Практична робота 
# Білет №2 
# Тема: Логічні оператори та порівняння 

# 1. Введення даних 
name = input("Ім'я клієнта: ") 
balance = float(input("Баланс: ")) 
amount = float(input("Сума переказу: ")) 
age = int(input("Вік: ")) 
blocked = input("Рахунок заблокований (так/ні): ") 

# 2. Логічні перевірки 

# Перевіряємо, чи клієнту виповнилося 18 років 
valid_age = age >= 18 

# Перевіряємо, чи сума переказу більша за нуль 
valid_amount = amount > 0 

# Перевіряємо, чи балансу достатньо для переказу 
enough_money = balance >= amount 

# Перевіряємо, чи рахунок не заблокований 
valid_account = blocked == "ні" 

# Перевіряємо всі умови разом 
can_transfer = ( 
    valid_age 
    and valid_amount 
    and enough_money 
    and valid_account 
) 

# 3. Виведення результатів 
print("Клієнт:", name) 
print("Вік підходить (>=18):", valid_age) 
print("Сума коректна (>0):", valid_amount) 
print("Достатньо коштів:", enough_money) 
print("Рахунок активний:", valid_account) 
print("Можливість переказу:", can_transfer) 

# 4. Додаткові перевірки 

# Перевіряємо, чи переказ понад 10 000 грн 
large_transfer = amount > 10000 

# Перевіряємо, чи баланс менший за 500 грн 
low_balance = balance < 500 

# Перевіряємо, чи переказ у межах від 100 до 5000 грн 
medium_transfer = amount >= 100 and amount <= 5000 

# Перевіряємо, чи сума переказу становить рівно половину балансу 
half_balance_transfer = amount == balance / 2 

# Перевіряємо неможливість виконання переказу 
cannot_transfer = not can_transfer 

print("Переказ понад 10 000 грн:", large_transfer) 
print("Баланс менше 500 грн:", low_balance) 
print("Переказ від 100 до 5000 грн:", medium_transfer) 
print("Переказ рівно половини балансу:", half_balance_transfer) 
print("Неможливість виконання переказу:", cannot_transfer)
