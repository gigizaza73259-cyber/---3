practice-task-3
n = int(input("Введите размер массива: "))

a = list(map(int, input("Введите элементы массива через пробел: ").split()))

max_index = a.index(max(a))
min_index = a.index(min(a))

start = min(max_index, min_index) + 1
end = max(max_index, min_index)

sum_negative = 0

for i in range(start, end):
    if a[i] < 0:
        sum_negative += a[i]

print("Сумма отрицательных элементов:", sum_negative)
