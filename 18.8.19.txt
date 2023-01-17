price = 0
billets = int(input(f'Введите цифрами необходимое количество билетов, для участия в мероприятии: '))
for i in range(billets):
    i += 1
    age_for_billets = int(input(f'Введите цифрами возраст посетителя, билет № {i} : '))
    if age_for_billets < 18:
            print(f'Билет бесплатный')
    elif 18 <= age_for_billets < 25:
            price += 990
            print(f'Стоимость билета - 990 руб.')
    else:
            price += 1390
            print(f'Стоимость билета - 1390 руб.')

if billets > 3:
    price -= 0.1 * price
    print(f'Всего к оплате, с учетом 10 % скидки, при приобретении более 3-х билетов - {price} руб. ')
else:
    print(f'Сумма к оплате - {price} руб.')