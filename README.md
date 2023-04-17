# -13.8.19
Домашнее задание

num_tickets = int(input("Введите количество билетов: "))
ticket_prices = [] # создаем пустой список для сохранения цен на каждый билет

for i in range(num_tickets):
    age = int(input("Введите возраст посетителя билета #" + str(i+1) + ": "))
    if age < 18:
        ticket_prices.append(0) # если посетитель младше 18 лет, билет бесплатный
    elif age >= 18 and age < 25:
        ticket_prices.append(990) # если посетитель от 18 до 24 лет, билет стоит 990 рублей
    else:
        ticket_prices.append(1390) # если посетитель старше 24 лет, билет стоит 1390 рублей

total_cost = sum(ticket_prices) # суммируем все цены на билеты

if num_tickets > 3:
    discount = 0.1 * total_cost # считаем скидку, если число билетов больше 3
else:
    discount = 0

final_cost = total_cost - discount # вычитаем размер скидки из общей суммы
print("Сумма к оплате: ", final_cost, "руб.") # выводим сумму к оплате
