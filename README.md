# Ответы на Контрольную работу

## Часть 1

### 1. Работа каких фрагментов кода правильно определяет, чётное или нет число содержится в переменной i?

Б) Этот код правильный. Условие i % 2 == 0 проверяет, делится ли i на 2 без остатка. Если остаток равен нулю, то число четное.

```python
if i % 2 == 0:
 print(i, 'чётное')
else:
 print(i, 'нечётное')
```

Г) Этот код правильный. Условие i % 2 != 0 проверяет, что остаток от деления i на 2 не равен нулю. Если это так, то число нечетное.

```python
if i % 2 != 0:
 print(i, 'нечётное')
else:
 print(i, 'чётное')
```

__Ответ: Б, Г__

### 2. Исправьте ошибку в приведённом коде

```python
num = int(input())
if num == 10:  # исправлено: было одно равно, стало два равно
 print("Число num равно 10")
```

### 3. Заполните таблицу, выбрав True или False

| Логическое выражение       | True | False |
|----------------------------|------|-------|
| a == 2 or b > 2            |  +   |       |
| 6 <= c and a > 3           |      |   +   |
| 1 != b and c != 3          |  +   |       |
| a >= -1 or a <= b          |  +   |       |
| not (a > 2)                |  +   |       |
| not (c <= 10)              |      |   +   |

### 4. Что будет выведено на экран в результате выполнения следующей программы?

```python
num1 = 34
num2 = 81
if num1 // 9 == 0 or num2 % 9 == 0:
    print('число', num1, 'выиграло')
else:
    print('число', num2, 'выиграло')
```

- `num1 // 9 == 0` (34 // 9 == 3, не равно 0)
- `num2 % 9 == 0` (81 % 9 == 0)

Так как `num2 % 9 == 0` верно, программа выведет:
Число 34 выиграло

### 5. Какое значение будет выведено на экран после выполнения следующей программы?

```python
a = 7
if a >= 2 and a <= 17: # условие выполнится
    b = 3
    p = a * a + b * b # p = 7 * 7 + 3 * 3
else:
    b = 5
p = (a + b) * (a + b) # p заново подсчитывается: (7 + 3) * (7 + 3)
print(p)
```

__Ответ: 100__

## Часть 2

### 1. Задача на четность

Решение:

```python
# Чтение входного числа
number = int(input())

# Проверка четности числа
if number % 2 == 0:
    print("Четное")
else:
    print("Нечетное")
```

### 2. Задача про сумму и разность цифр

1-ый способ решения (извлечение чисел через строку):

```python
# Чтение входного числа
num_str = input()

# Извлечение цифр числа
first_digit = int(num_str[0])
second_digit = int(num_str[1])
third_digit = int(num_str[2])
fourth_digit = int(num_str[3])

# Проверка условия
if first_digit + fourth_digit == second_digit - third_digit:
    print("ДА")
else:
    print("НЕТ")
```

2-ой способ решения (извлечение чисел через вычисления):

```python
# Чтение входного числа
number = int(input())

# Извлечение цифр числа
first_digit = number // 1000
second_digit = (number // 100) % 10
third_digit = (number % 100) // 10
fourth_digit = number % 10

# Проверка условия
if first_digit + fourth_digit == second_digit - third_digit:
    print("ДА")
else:
    print("НЕТ")
```

### 3 Задача

```python
# Ввод трех различных чисел
a = int(input("Введите первое число: "))
b = int(input("Введите второе число: "))
c = int(input("Введите третье число: "))

# Проверка, какое число самое большое
if a > b and a > c:
    max_number = a
elif b > a and b > c:
    max_number = b
else:
    max_number = c

# Вывод самого большого числа
print(max_number)
```

### 4 задача

```python
# Ввод двузначного числа
number = int(input())

# Извлечение цифр числа
first_digit = number // 10
second_digit = number % 10

# Вычисление суммы цифр
digits_sum = first_digit + second_digit

# Проверка, является ли сумма цифр двузначным числом
if digits_sum >= 10 and digits_sum <= 99:
    print("да")
else:
    print("нет")
```

### 5 задача

```python
# Ввод трехзначного числа
number = int(input())

# Извлечение цифр числа (можно извлекать через строку, как было во второй задаче)
first_digit = number // 100
second_digit = (number // 10) % 10
third_digit = number % 10

# Инициализация переменной для хранения суммы четных цифр
even_digits_sum = 0

# Проверка каждой цифры на четность и добавление ее к сумме, если она четная
if first_digit % 2 == 0:
    even_digits_sum += first_digit
if second_digit % 2 == 0:
    even_digits_sum += second_digit
if third_digit % 2 == 0:
    even_digits_sum += third_digit

# Вывод суммы четных цифр
print(even_digits_sum)
```
