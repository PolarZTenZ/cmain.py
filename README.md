# cmain.py
All Codes

print("¡Hola, mundo! Este es mi primer programa en Python.")
# Definiendo variables
nombre = "Juan"
edad = 25
altura = 1.75
es_estudiante = True
pais = "Perú"

# Mostrando información con print()
print("Nombre:", nombre)
print("Edad:", edad)
print("Altura:", altura)
print("¿Es estudiante?", es_estudiante)
print("País:", pais)

print(type(5))

num = 5.9
entero = int(num)
print(entero)  # Salida: 5

entero = int(altura)
print(entero)  #Salida: 1

# Pedir datos al usuario
nombre = input("¿Cómo te llamas? ")
edad = input("¿Cuántos años tienes? ")

# Mostrar los datos en pantalla
print("Hola", nombre + ", tienes " + edad + " años.")

pregunta = input("¿Juegas Valorant? ")
nombre = input("¿Cómo te llamas? ")
edad = input("¿Cuántos años tienes? ")
ciudad = input("¿En que ciudad vives? ")

print("Hola", nombre + " tienes", edad + " años, vives en", ciudad + " y", pregunta + " juegas valorant.")

# Pedir la edad y convertirla a número
edad = input("¿Cuántos años tienes? ")
edad = int(edad)  # Convertimos el texto a número

# Calcular la edad en 5 años
edad_futura = edad + 5

# Mostrar el resultado
print("En 5 años tendrás", edad_futura, "años.")

edad1 = input("Tu edad: ")
edad2 = input("La edad de tu Tío: ")

edad1 = float(edad1)
edad2 = float(edad2)

suma = edad1 + edad2

print(f"La suma de", edad1, "que es tu edad, mas la suma de", edad2, "que es la edad de tu tío; nos da un resultado de:", suma)

# Pedir dos números al usuario
num1 = float(input("Ingresa el primer número: "))
num2 = float(input("Ingresa el segundo número: "))

# Pedir la operación
operacion = input("Elige una operación (+, -, *, /): ")

# Realizar la operación según la elección del usuario
if operacion == "+":
    resultado = num1 + num2
elif operacion == "-":
    resultado = num1 - num2
elif operacion == "*":
    resultado = num1 * num2
elif operacion == "/":
    if num2 != 0:  # Evitar división por cero
        resultado = num1 / num2
    else:
        resultado = "Error: No se puede dividir por cero"
else:
    resultado = "Operación no válida"

# Mostrar el resultado
print("Resultado:", resultado)

num1 = float(input("Ingresa el primer dígito: "))
num2 = float(input("Ingresa el segundo dígito: "))

operacion = input("Elige una operación para resolvertela (+, -, *, /, %): ")

if operacion == "+":
    resultado = num1 + num2
elif operacion == "-":
    resultado = num1 - num2
elif operacion == "*":
    resultado = num1 * num2
elif operacion == "/":
    if num2 != 0:
        resultado = num1 / num2
    else:
        resultado = "Error: No se puede dividir por cero"
elif operacion == "%":
    resultado = num1 % num2
else:
    resultado = "Operación no válida"

print("Rpta:", resultado)

# Función para obtener un número válido
def obtener_numero():
    while True:
        try:
            numero = float(input("Ingresa un dígito: "))
            return numero
        except ValueError:
            print("¡Eso no es un número válido! Reintenta.")

# Función para obtener la operación válida
def obtener_operacion():
    while True:
        operacion = input("Elige una operación (+, -, *, /, %): ")
        if operacion in ["+", "-", "*", "/", "%"]:
            return operacion
        else:
            print("Operación no válida. Elige una de (+, -, *, /, %).")

# Pedir los números al usuario
num1 = obtener_numero()
num2 = obtener_numero()

# Pedir la operación
operacion = obtener_operacion()

# Realizar la operación
if operacion == "+":
    resultado = num1 + num2
elif operacion == "-":
    resultado = num1 - num2
elif operacion == "*":
    resultado = num1 * num2
elif operacion == "/":
    if num2 != 0:  # Evitar división por cero
        resultado = num1 / num2
    else:
        resultado = "Error: No se puede dividir por el valor cero"
elif operacion == "%":
    resultado = num1 % num2

# Mostrar el resultado
print("Rpta:", resultado)

# Función para convertir Celsius a Fahrenheit
def celsius_a_fahrenheit(celsius):
    return (celsius * 9/5) + 32

# Función para convertir Fahrenheit a Celsius
def fahrenheit_a_celsius(fahrenheit):
    return (fahrenheit - 32) * 5/9

# Pedir al usuario la opción de conversión
opcion = input("Elige la conversión (1: Celsius a Fahrenheit, 2: Fahrenheit a Celsius): ")

# Validar la opción
if opcion == "1":
    celsius = float(input("Ingresa la temp en Celsius: "))
    fahrenheit = celsius_a_fahrenheit(celsius)
    print(f"{celsius}° Celsius son {fahrenheit}° Fahrenheit.")
elif opcion == "2":
    fahrenheit = float(input("Ingresa la temp en Fahrenheit: "))
    celsius = fahrenheit_a_celsius(fahrenheit)
    print(f"{fahrenheit}° Fahrenheit son {celsius}° Celsius.")
else:
    print("Opción no correcta. Por favor elige bien 1 o 2.")

    # Pedir al usuario una frase
frase = input("Ingresa una frase o palabra: ")

# Contar la cantidad de caracteres
cantidad_caracteres = len(frase)

# Mostrar la cantidad de caracteres
print(f"La frase o palabra tiene {cantidad_caracteres} caracteres.")

# Pedir al usuario una palabra
palabra = input("Ingresa una palabra o frase: ")

# Pedir la letra que quieres contar
letra = input("Ingresa la letra que deseas contabilizar: ")

palabra = palabra.lower()
letra = letra.lower()

# Contar cuántas veces aparece la letra en la palabra
cantidad_letras = palabra.count(letra)

# Mostrar el resultado
print(f"La letra '{letra}' esta presente {cantidad_letras} veces en la palabra o frase '{palabra}'.")

# Pedir al usuario una cadena de texto
texto = input("Ingresa una cadena de texto: ")

# Invertir la cadena
texto_invertido = texto[::-1]

# Mostrar el resultado
print(f"La cadena invertida es: {texto_invertido}")

# Crear una lista de números
numeros = [1, 2, 3, 4, 5]

# Usar un bucle for para recorrer la lista
for numero in numeros:
    print(numero)

# Pedir al usuario un número
numero = int(input("Ingresa un dígito positivo: "))

# Mientras el número sea negativo o cero, seguir pidiendo
while numero <= 0:
    print("Sección inválida. Inténtalo de nuevo.")
    numero = int(input("Ingresa un dígito positivo: "))

# Mostrar el número correcto
print(f"¡Número válido! Has ingresado: '{numero}'.")

# Crear una lista con tres nombres
nombres = ["Carlos", "María", "Luis"]

# Pedir al usuario un nuevo nombre
nuevo_nombre = input("Ingresa un new nombre: ")

# Agregar el nombre a la lista
nombres.append(nuevo_nombre)

# Mostrar todos los nombres en la lista
print("Listado de nombres:")
for nombre in nombres:
    print(nombre)

# Crear una tupla con tres colores
colores = ("Rojo", "Verde", "Azul")

# Mostrar los colores
print("Colores disponibles:")
for color in colores:
    print(color)

# Intentar modificar un color (esto dará error)
# colores[0] = "Amarillo"  # Descomenta esta línea y prueba

# Crear un diccionario con información de una persona
persona = {
    "nombre": "Carlos",
    "edad": 25,
    "ciudad": "Lima"
}

# Mostrar la información inicial
print("Información de la persona:")
print(f"Nombre: {persona['nombre']}")
print(f"Edad: {persona['edad']}")
print(f"Ciudad: {persona['ciudad']}")

# Pedir al usuario una nueva edad y actualizar el diccionario
nueva_edad = int(input("Ingresa una new edad: "))
persona["edad"] = nueva_edad

# Mostrar la información actualizada
print("\nInformación actualizada:")
print(f"Nombre: {persona['nombre']}")
print(f"Edad: {persona['edad']}")
print(f"Ciudad: {persona['ciudad']}")
