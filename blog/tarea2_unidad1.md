# TAREA 2 -EJERCICIOS UNIDAD 1


# Reto1: simula el comportamiento de la tortuga usando solo print() e input().

Intenta recrear el movimiento de la tortuga únicamente con texto, usando funciones, print() y input() para pedir valores al usuario.

## Definir la posición inicial y la representación de la tortuga
posicion_x = 50
posicion_y = 1
tortuga = 'T'
espacio_vacio = '.'

print("Simulación de tortuga. Comandos: 'arriba', 'abajo', 'izquierda', 'derecha', 'salir'")

while True:
    ## Dibujar el "tablero" o la posición actual (simplificado)
    ## En un entorno real, esto requeriría un bucle anidado para imprimir la cuadrícula completa.
    ## Aquí mostramos un ejemplo simple de cómo podría verse la salida:
    print(f"\nPosición actual: ({posicion_x}, {posicion_y})")
    print(f"Tablero simplificado:")
    
    for y in range(posicion_y, posicion_y + 1):
        fila = ""
        for x in range(posicion_x, posicion_x + 1):
            if x == posicion_x and y == posicion_y:
                fila += tortuga
            else:
                fila += espacio_vacio
        print(fila)

    comando = input("Introduce comando: ").lower()

    if comando == 'arriba':
        posicion_y -= 1
    elif comando == 'abajo':
        posicion_y += 1
    elif comando == 'izquierda':
        posicion_x -= 1
    elif comando == 'derecha':
        posicion_x += 50
    elif comando == 'salir':
        print("Saliendo de la simulación.")


        
# reto 2 ,  Crea el rastro de una tortuga moviéndose hacia abajo usando únicamente print() e input().
La salida esperada es similar a:


 Definimos el carácter para representar la tortuga.
tortuga = 'T' 

 La posición horizontal se ajusta con espacios.
 Ajusta el número de espacios iniciales si quieres que empiece más a la derecha.
espacios_iniciales = '          '

##  --- Simulación del Movimiento ---

## Paso 1
print('Pulsa ENTER para que la tortuga se mueva hacia abajo.')
input()
print('\n' + espacios_iniciales + tortuga)

## Paso 2
input()
print('\n' * 2 + espacios_iniciales + tortuga) # Dos saltos de línea para ir 'más abajo'

## Paso 3
input()
print('\n' * 3 + espacios_iniciales + tortuga) # Tres saltos de línea

## Paso 4
input()
print('\n' * 4 + espacios_iniciales + tortuga) 

## Paso 5
input()
print('\n' * 5 + espacios_iniciales + tortuga)

## Mensaje final
print('\n' * 6 + " Fin del rastro.")




       # Reto 4: Encapsula los comportamientos anteriores usando funciones

Reescribe los retos anteriores creando funciones que representen los movimientos de la tortuga solo con texto.
Usa las siguientes funciones como interfaz:


def adelante(n):
    """
    Dibuja el movimiento hacia la derecha (->) por n pasos.
    Un paso es un guion '-'. El final del movimiento es un '>'.
    """
    # Se usa 'n-1' para los guiones y se agrega el '>' al final
    linea = "-" * n
    print(linea + ">")

def abajo(n):
    """
    Dibuja el movimiento hacia abajo (|) por n pasos.
    Un paso es una barra '|'. El final del movimiento es un 'V'.
    """
    ## Creamos un separador para la alineación
    
    ## Se necesitan al menos 3 espacios para que la línea vertical
    
    ## quede debajo del final de la línea horizontal (el carácter '>')
    separador = "   "

    ## Dibuja la parte vertical (n-1 barras verticales)
    for _ in range(n):
        print(separador + "|")

    ## Dibuja la flecha final
    print(separador + "V")

##   Ejemplo de Ejecución 

print(" Dibujando la 'L'")

adelante(5)  ## Dibuja la línea horizontal de 5 pasos


abajo(3)     ## Dibuja la línea vertical de 3 pasos

print("------------------------")



# Reto 5: La tortuga baja las escalas

Ajusta tus funciones para que la tortuga pueda bajar escalones.
Cada escalón debe conservar la posición horizontal acumulada y dibujar correctamente tanto el tramo horizontal como el vertical.




## Escalón 1 
adelante(5)  # forward(5) -> Horizontal 
abajo(2)     # down(2) -> Vertical 

## Escalón 2 
adelante(5)  ## forward(5) -> Horizontal 
abajo(2)     ## down(2) -> Vertical 

## Escalón 3 
adelante(5)  ## forward(5) -> Horizontal 
abajo(2)     ## down(2) -> Vertical 





### Referencias de IA

https://gemini.google.com/app/eb4fe01278c2b7aa?hl=es

