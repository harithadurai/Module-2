# 🔺 Looping(Patterns)-Pascal's Triangle Generator in Python

This project demonstrates a simple Python program to generate **Pascal’s Triangle**, where the number of rows is provided by the user.

---

## 🎯 Aim

To write a Python program that generates **Pascal's Triangle** using numbers. The number of rows is accepted from the user.

---

## 🧠 Algorithm

1. Start the program.
2. Input the number of rows from the user.
3. Loop from 0 to the number of rows.
4. For each row:
   - Print appropriate spaces to shape the triangle.
   - Compute values using the formula:  
     \[
     C(n, k) = \frac{n!}{k!(n-k)!}
     \]
5. Print all rows of Pascal’s Triangle.
6. End the program.

---

## 🧪 Program
```
def generate_pascals_triangle(n):
    triangle = []

    for i in range(n):
        row = [1]  # First element is always 1
        if i > 0:
            last_row = triangle[i-1]
            # Generate middle elements
            for j in range(1, i):
                row.append(last_row[j-1] + last_row[j])
            row.append(1)  # Last element is always 1
        triangle.append(row)
    return triangle
rows = int(input("Enter number of rows for Pascal's Triangle: "))
triangle = generate_pascals_triangle(rows)
for row in triangle:
    print(' '.join(map(str, row)).center(rows*2))
```

## Sample Output
   <img width="521" height="547" alt="image" src="https://github.com/user-attachments/assets/36271a7d-2343-4609-b0b8-044d9c5391f7" />

## Result
Thus the project demonstrates a simple Python program to generate **Pascal’s Triangle**, where the number of rows is provided by the user is verified successfully.
