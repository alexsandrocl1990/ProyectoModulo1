# ProyectoModulo1
Proyecto: calculadora de índice de masa corporal

#Como primeros pasos, usando la funcion input logramos digitar los textos que se nos solicita

#Nombre del usario:
nombre = input('Nombre: ')

#Apellido Paterno :

apellido_p = input('Apellido Paterno: ')

#Apellido Materno:

apellido_m = input('Apellido Materno: ')

#Edad del usuario:

edad = input('Ingrese su edad: ')

#luego uso def para definir una funcion nueva. En éste caso calcular el IMC utilizando la fórmula matemática (peso/altura al cuadrado) para la misma. Y la funcion return para indicar el final de la funcion:
def calcular_IMC(peso, altura):
  
    imc = peso / (altura**2)
    return imc

#A continuacion el uso de la funcion elif para comprobar la condicion a cumplir (mayor, menor o igual) de acuerdo al rango de peso y determinar el estado del usario (Bajo peso, Peso Saludable, Sobrepeso y Obecidad)
def determinar_IMC(imc):
   
    if imc < 18.5:
        return 'Bajo peso'
    elif 18.5 <= imc < 25:
        return 'Peso saludable'
    elif 25 <= imc < 30:
        return 'Sobrepeso'
    elif 30 <= imc <300:
        return 'Obesidad'

#asigné la funcion float para el uso de números, ya sean enteros o decimales (peso y altura):

peso = float(input('Ingrese su peso en kg: '))

 altura = float(input('Ingrese su altura en metros: '))
 

#al cierre, tars los datos obtenidos, el programa nos da la interpretacion final del Indice de masa corporal:

   imc = calcular_IMC(peso, altura)
   
   interpretacion = determinar_IMC(imc)

   print("Su IMC es:", imc)
   
   print("Su categoría de IMC es:", interpretacion)
