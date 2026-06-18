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

practice-task-4

n = int(input("Введите количество голов драконьей стаи: "))

dp = [0] * (n + 1)
dp[0] = 1

for i in range(1, n + 1):
      for heads in range(1, min(7, i) + 1):
             dp[i] = max(dp[i], heads * dp[i - heads])
             
print("Максимальная сила стаи:", dp[n])
