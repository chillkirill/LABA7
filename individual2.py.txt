# Ввод списка вещественных чисел
A = list(map(float, input("Введите вещественные числа через пробел: ").split()))

# 1. Произведение отрицательных элементов списка
negative_elements = [x for x in A if x < 0]
product_of_negatives = 1
for num in negative_elements:
    product_of_negatives *= num if num != 0 else 1  # Учитываем, что произведение на 0 будет 0

# 2. Сумма положительных элементов до максимального элемента
max_element = max(A)
max_index = A.index(max_element)

positive_elements_before_max = [x for x in A[:max_index] if x > 0]
sum_of_positives_before_max = sum(positive_elements_before_max)

# 3. Изменяем порядок следования элементов в списке на обратный
A.reverse()

# Вывод результатов
print(f"Произведение отрицательных элементов: {product_of_negatives}")
print(f"Сумма положительных элементов до максимального элемента: {sum_of_positives_before_max}")
print(f"Список в обратном порядке: {A}")
