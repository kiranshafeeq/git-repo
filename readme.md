# code Explanation: Exploring user's favorite Numbers

## Step 1 : Taking user input

```python
import math
name=input("Enter your name: ")
num_1=int(input("Enter your first favourite number: "))
num_2=int(input("Enter your second favourite number: "))
num_3=int(input("Enter your third favourite number: "))
print(f"hello, {name}! Lets explore your favourite number:")
```

- This part of the code asks the user for their name and three favorite numbers.

## step 2: creating a list of numbers

```python
numbers = [num_1, num_2, num_3]
```

- This step create a list called 'numbers'.

## Step 3: Identifying even or odd numbers

```python
even_odd_list = [(num, "even" if num % 2 == 0 else "odd") for num in numbers]
for num, kind in even_odd_list:
print(f"The number {num} is {kind}.")
```

- This part check if each number is even ordd.

## step 5: Calculating the sum of the number.

```python

squares = [(num, num ** 2) for num in numbers]
for num, square in squares:
print(f"The square of {num} is ({num},{square}).")

total_sum = sum(numbers)
print(f"\nAmazing! The sum of your favorite numbers is: {total_sum}")
```

- The function() calculate sum and store in total_sum.

## Step: checking if the sum is prime(factorization)

```python

is_prime = True
if total_sum <= 1:
is_prime = False
else:
for i in range(2, int(math.sqrt(total_sum)) + 1):
if total_sum % i == 0:
is_prime = False
break
```

- The check the condition and decide sum is prime or not

## step 8: printing the prime check result

```
- check the result
if is_prime:
print(f"Wow! The sum {total_sum} is a prime number!")
else:
print(f"The sum {total_sum} is not a prime number!.")
```
