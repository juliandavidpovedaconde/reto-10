# reto-10


---

## 1. Suma/Restar de Matrices
```python
f1 = int(input("ingrese el numero de filas de su primera matriz: "))
f2 = int(input("ingrese el numero de filas de su segunda matriz: "))
c1 = int(input("ingrese el numero de columnas de su primera matriz: "))
c2 = int(input("ingrese el numero columnas de su segunda matriz: "))

if f1 == f2 and c1 == c2:
    A = []
    B = []
    c = []

    # Leer primera matriz A
    for i in range(f1):
        filas = []
        for j in range(c1):
            valor = int(input("A[" + str(i+1) + "][" + str(j+1) + "]: "))
            filas.append(valor)
        A.append(filas)

    # Leer segunda matriz B
    for x in range(f2):
        filas = []
        for y in range(c2):
            valores = int(input("B[" + str(x+1) + "][" + str(y+1) + "]: "))
            filas.append(valores)
        B.append(filas)

    # Sumar matrices elemento a elemento
    for a in range(f1):
        fila = []
        for b in range(c1):
            suma = A[a][b] + B[a][b]
            fila.append(suma)
        c.append(fila)

    # Imprimir resultado
    print("La matriz suma/resta es:")
    for fila in c:
        print(fila)
else:
    print("Error: las dimensiones no coinciden para la operación.")
````

---

## 2. Producto de Matrices

```python
m1 = int(input("ingrese la cantidad de filas de su primera matriz A: "))
n1 = int(input("ingrese el numero de columnas de su primera matriz A: "))
m2 = int(input("ingrese el numero de filas de su segunda matriz B: "))
n2 = int(input("ingrese el numero de columnas de su segunda matriz B: "))

if n1 == m2:
    A = []
    B = []
    c = []  # matriz resultado

    # Leer A
    for i in range(m1):
        lista = []
        for j in range(n1):
            valor = int(input("A[" + str(i+1) + "][" + str(j+1) + "]: "))
            lista.append(valor)
        A.append(lista)

    # Leer B
    for x in range(m2):
        lista = []
        for y in range(n2):
            valor = int(input("B[" + str(x+1) + "][" + str(y+1) + "]: "))
            lista.append(valor)
        B.append(lista)

    # Multiplicar A × B
    for a in range(m1):
        lista = []
        for b in range(n2):
            suma = 0
            for k in range(n1):
                suma += A[a][k] * B[k][b]
            lista.append(suma)
        c.append(lista)

    # Imprimir matriz resultado
    print("La matriz producto es:")
    for fila in c:
        print(fila)
else:
    print("Error: columnas de A deben coincidir con filas de B.")
```

---

## 3. Matriz Transpuesta

```python
m = int(input("ingrese el numero de filas de su matriz: "))
n = int(input("ingrese el numero de columnas de su matriz: "))

A = []
for i in range(m):
    lista = []
    for j in range(n):
        valor = int(input("A[" + str(i+1) + "][" + str(j+1) + "]: "))
        lista.append(valor)
    A.append(lista)

T = []
for j in range(n):
    lista = []
    for i in range(m):
        lista.append(A[i][j])
    T.append(lista)

print("La matriz transpuesta es:")
for fila in T:
    print(fila)
```

---

## 4. Suma de elementos de una Columna

```python
m = int(input("ingrese el numero de filas de su matriz: "))
n = int(input("ingrese el numero de columnas de su matriz: "))

A = []
for i in range(m):
    lista = []
    for j in range(n):
        valor = int(input("A[" + str(i+1) + "][" + str(j+1) + "]: "))
        lista.append(valor)
    A.append(lista)

columna = int(input("ingrese el numero de la columna que quiere sumar: "))

if columna > n or columna < 1:
    print("la columna esta fuera de rango")
else:
    suma = 0
    for i in range(m):
        suma = suma + A[i][columna-1]
    print("la suma de la columna " + str(columna) + " es: " + str(suma))
```

---

## 5. Suma de elementos de una Fila

```python
m = int(input("ingrese el numero de filas de su matriz: "))
n = int(input("ingrese el numero de columnas de su matriz: "))

A = []
for i in range(m):
    lista = []
    for j in range(n):
        valor = int(input("A[" + str(i+1) + "][" + str(j+1) + "]: "))
        lista.append(valor)
    A.append(lista)

fila = int(input("ingrese el numero de la fila que qu
```
