import random

print("Reglas del juego: \n"
" La piedra le gana a la tijera \n"
" El papel le gana a la piedra \n"
" La tijera le gana al papel \n")

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

print("El usuario escogio:" + nombre_opcion)
print("\n Ahora es el turno de la computadora........")

opcion_computadora= random.randint(1,3)
while opcion_computadora==opcion:
  opcion_computadora = random.randint(1,3)

if opcion_computadora==1:
  nombre_opcion_computadora='Piedra'
elif opcion_computadora==2:
  nombre_opcion_computadora='Papel'
else:
    nombre_opcion_computadora='Tijera'

print("La computadora escogio: " + nombre_opcion_computadora)
print(nombre_opcion + " VRS " + nombre_opcion_computadora)

if((opcion==1 and opcion_computadora==2) or
(opcion==2 and opcion_computadora ==1)):
  print("Papel gana => \n", end ="")
  resultado = "Papel"

elif ((opcion==1 and opcion_computadora  ==3) or
  (opcion==3 and opcion_computadora ==1)):
  print("Piedra gana => \n", end = "")
  resultado = "Piedra"

else:
  print("Tijera gana => \n", end = "")
  resultado = "Tijeras"

if resultado==nombre_opcion:
  print("********* El usuario gana *********")

else:
  print ("******** La computadora gano *********")

print("¿Desea jugar otra vez? (SI/NO)")
res= input()

if res== 'NO' or res== 'no' or res== 'No':
  break

print("Muchas gracias por jugar!")
