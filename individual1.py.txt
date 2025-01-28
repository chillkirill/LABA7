# Ввод списка A из 10 элементов
A = [int(input(f"Введите элемент {i+1}: ")) for i in range(10)]

# Находим сумму положительных элементов, кратных 5, и их количество
positive_multiples_of_5 = [x for x in A if x > 0 and x % 5 == 0]

# Результаты
sum_of_elements = sum(positive_multiples_of_5)
count_of_elements = len(positive_multiples_of_5)

# Выводим результаты
print(f"Сумма положительных элементов, кратных 5: {sum_of_elements}")
print(f"Количество положительных элементов, кратных 5: {count_of_elements}")
