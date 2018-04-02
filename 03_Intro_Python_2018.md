

<img src="images/utfsm.png" alt="" width="200px" align="right"/>

<br/>

# IWI131 Programación
Introducción a Python<br/>
Cristopher Arenas<br/>
cristopher.arenas@usm.cl<br/>

<br/>
Paralelo 200<br/>
Campus San Joaquin

# Tipos de Datos

## Números enteros
Tipo `int` (integer)


```python
1
```




    1




```python
+135
```




    135




```python
-124
```




    -124



## Números Reales
Tipo `float` (punto flotante)


```python
0.36
```




    0.36




```python
1.
```




    1.0




```python
6.02e23
```




    6.02e+23



## Valores Lógicos
Tipo `bool`


```python
True
```




    True




```python
False
```




    False



## Texto
Tipo `str` (strings)


```python
"hola"
```




    'hola'




```python
'hola'
```




    'hola'




```python
"Let's Go!"
```




    "Let's Go!"




```python
'Ella dijo "Hola"'
```




    'Ella dijo "Hola"'



# Expresiones y operadores

**Expresión:** combinación de valores que pueden ser evaluados y entregan un resultado.

Pueden estar formados por:
- **valores literales**
- **variables**
- **operadores**
- **llamadas a funciones**

**Operador:** símbolo en una expresión que representa una operación aplicada a los valores sobre los que actúa.

## Operadores Aritméticos
Operan sobre valores numéricos y entregan un valor numérico como resultado.

**Operadores binarios**
- Suma (`+`)
- Resta (`-`)
- Multiplicación (`*`)
- División (`/`)
- Módulo (`%`)
- Potencia (`**`)


```python
3+2
```




    5




```python
8-5
```




    3




```python
8-5.0
```




    3.0




```python
1/2
```




    0




```python
1./2
```




    0.5




```python
7%3
```




    1



**Operadores unarios**
- Positivo (`+`)
- Negativo (`-`)


```python
+3
```




    3




```python
-5.0
```




    -5.0



## Operadores relacionales
Comparan valores. Operandos pueden ser cualquier expresión que pueda ser comparado. Resultado siempre es un valor lógico.

- igual a (`==`)
- distinto a (`!=`)
- mayor que (`>`)
- menor que (`<`)
- mayor o igual que (`>=`)
- menor o igual que (`<=`)


```python
5 == 3
```




    False




```python
4 > 7
```




    False




```python
4 != 3
```




    True




```python
"casa" == 'casa'
```




    True




```python
3 > 3
```




    False




```python
"a" < "z"
```




    True



## Operadores lógicos
Tienen operandos y resultado de tipo lógico.

- conjunción lógica `and`
- disyunción lógica `or`
- negación lógica `not`


```python
3 == 5 and False
```




    False




```python
3!=5 or False
```




    True




```python
not True
```




    False



## Operadores de Texto
Operan sobre strings. Operandos no son necesariamente todos strings.

- Concatenación de strings (`+`)
- Repetición de strings (`*`)
- Obtener i-ésimo caracter de un string
- Comparar strings alfabéticamente
- Verificar si un string está contenido dentro de otro


```python
"Hola" + "Mundo"
```




    'HolaMundo'




```python
"Waka"*3
```




    'WakaWakaWaka'




```python
"perico"[2]
```




    'r'




```python
"auto" > "avion"
```




    False




```python
"pollo" in "repollos"
```




    True




```python
"pollo" in "gallinero"
```




    False



## Llamados a funciones


```python
len("10")
```




    2




```python
abs(4-5)
```




    1




```python
round(1./3,2)
```




    0.33



# Asignación de variables

- Una asignación de variables tiene la forma: 
<center>
`variable = expresion`
</center>

- Primero se evalúa la expresión a la derecha del signo igual.
- El resultado de la evaluación es asignado a la variable a la derecha del signo igual.

¿Qué valor tienen las siguiente variables?


```python
a = 4 + 5
b = a + 4
a = 2 
d = a - 3
e = e + 1
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-56-9c013495dc5f> in <module>()
          3 a = 2
          4 d = a - 3
    ----> 5 e = e + 1
    

    NameError: name 'e' is not defined


# Entrada de datos


```python
nombre = raw_input("Ingrese su nombre: ")
```

    Ingrese su nombre: Cristopher


¿Qué tipo de dato es la variable `nombre`?


```python
nombre
```




    'Cristopher'



# Salida de datos


```python
print "Hola mundo"
```

    Hola' mundo



```python
a = 6
x = a**2
```


```python
print a, 'al cuadrado es', x
```

    6 al cuadrado es 36



```python
print str(a)+" al cuadrado es "+str(x)
```

    6 al cuadrado es 36



```python
print a, 
print x
```

    6 36



```python
print a
print x
```

    6
    36


# Transformaciones entre tipos de datos


```python
int(3.5)
```




    3




```python
float(1)
```




    1.0




```python
str(25)
```




    '25'




```python
bool(2)
```




    True



# Ejemplo


```python
f = float(raw_input('Temp. en Farenheit: '))
c = (f-32.0) * (5.0/9.0)
print 'El equivalente en Celsius es:',round(c,2)
```

    Temp. en Farenheit: kukgk



    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-82-79a3f1b4a041> in <module>()
    ----> 1 f = float(raw_input('Temp. en Farenheit: '))
          2 c = (f-32.0) * (5.0/9.0)
          3 print 'El equivalente en Celsius es:',round(c,2)


    ValueError: could not convert string to float: kukgk


# Comentarios
- Son segmentos de código ignorados por el intérprete
- Sirven para explicar en código
- Se escriben a la derecha del caracter `#`


```python
#El siguiente codigo muestra la suma de 2 + 2 en pantalla
print 2 + 2
```

    4



```python
print "#",5 # +2
```

    # 5


# Algunos errores


```python
n = 8
m = 0
print 'Listo'
print n/m
```

    Listo



    ---------------------------------------------------------------------------

    ZeroDivisionError                         Traceback (most recent call last)

    <ipython-input-89-27c1d5e042d2> in <module>()
          2 m = 0
          3 print 'Listo'
    ----> 4 print n/m
    

    ZeroDivisionError: integer division or modulo by zero



```python
2*(3+4))
```


      File "<ipython-input-90-93a067e50f9d>", line 1
        2*(3+4))
               ^
    SyntaxError: invalid syntax




```python
n = 6
n + 2 = 7
```


      File "<ipython-input-91-900a1c563d6b>", line 2
        n + 2 = 7
    SyntaxError: can't assign to operator




```python
x = 20
5*x
```




    100




```python
5 * y
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-93-ca87293f5d2d> in <module>()
    ----> 1 5 * y
    

    NameError: name 'y' is not defined



```python
hola = 56
len(hola)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-94-80bc2cd2ab28> in <module>()
          1 hola = 56
    ----> 2 len(hola)
    

    TypeError: object of type 'int' has no len()



```python
"a"*3.0
```
