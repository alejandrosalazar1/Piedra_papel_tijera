import random

print("Reglas del juego: \n"
"Piedra le gana a tijera \n"
"Papel le gana a piedra \n"
"Tijera le gana al papel \n")

print("Seleccione una opcion -\n"
"1. Piedra = 0\n"
"2. Papel = _\n"
"3. Tijera = X \n")

opcion = int(input("Escoga una opcion: "))

while opcion >3 or opcion<1:
  opcion = int(input("Ingrese opcion valida:"))

if opcion==1:
  nombre_opcion = 'Piedra'
elif opcion==2:
  nombre_opcion= 'Papel'
else:
  nombre_opcion= 'Tijera'
