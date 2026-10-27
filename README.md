# Bilet-2
#Практична робота
#Білет 2 банківський переказ 
balans=float(input ("Введіть баланс карти: "))
vik=int(input("Введіть вік: "))
if vik>=18:
  dostyp=0
  print("Карта розблокована")
else:
  dostyp=1
  print("Карта заблокована")
  raise ValueError("Доступ заборонено: вік менше 18 років.")
perekaz=float(input("Введіть суму переказу: "))          
if perekaz<0:
  print("Сума переказу має бути більша за 0")
  raise ValueError("Сума переказу менше 0")
zaliwok=balans-perekaz
if balans >= perekaz:
  print("Кошти надіслані")
else:
  print("Недостатньо коштів на балансі")
  raise ValueError("Недостатньо коштів")
zaliwok=balans-perekaz
print("Залишок на рахунку: ", zaliwok)
print("Переказ успішний")
