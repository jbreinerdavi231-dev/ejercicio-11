# ejercicio-11
import random

print("JUEGO DE ADIVINANZA")
print("1. Fácil: número de 1 a 20, 6 intentos")
print("2. Intermedio: número de 1 a 50, 5 intentos")
print("3. Difícil: número de 1 a 100, 4 intentos")

opcion = int(input("Seleccione el nivel: "))

if opcion == 1:
    numero_secreto = random.randint(1, 20)
    intentos = 6

elif opcion == 2:
    numero_secreto = random.randint(1, 50)
    intentos = 5

elif opcion == 3:
    numero_secreto = random.randint(1, 100)
    intentos = 4

else:
    print("Opción no válida")
    intentos = 0

while intentos > 0:
    numero = int(input("Adivine el número secreto: "))
    intentos = intentos - 1

    if numero == numero_secreto:
        print("Número correcto")
        puntaje = intentos * 20
        print("Su puntaje es:", puntaje)
        break

    elif numero < numero_secreto:
        print("El número secreto es mayor")

    else:
        print("El número secreto es menor")

    print("Intentos restantes:", intentos)

if intentos == 0 and numero != numero_secreto:
    print("Se acabaron los intentos")
    print("El número secreto era:", numero_secreto)
    print("Su puntaje es: 0")
