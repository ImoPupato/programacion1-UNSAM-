#### Ejercicio 1.4: Debuguear
*El siguiente fragmento de código está relacionado con el problema del obelisco. Tiene un bug, es decir, un error.*
```R
# obelisco.py

grosor_billete = 0.11 * 0.001 # 0.11 mm en metros
altura_obelisco = 67.5         # altura en metros
num_billetes = 1
dia = 1

while num_billetes * grosor_billete <= altura_obelisco:
    print(dia, num_billetes, num_billetes * grosor_billete)
    dia = dias + 1 #<------------------------El error está aquí, la variable fue nombrada como "dia", no "dias"
    num_billetes = num_billetes * 2

print('Cantidad de días', dia)
print('Cantidad de billetes', num_billetes)
print('Altura final', num_billetes * grosor_billete)
```
#### Ejercicio 1.5: La pelota que rebota
Una pelota de goma es arrojada desde una altura de 100 metros y cada vez que toca el piso salta 3/5 de la altura desde la que cayó.  
*Escribí un programa rebotes.py que imprima una tabla mostrando las alturas que alcanza en cada uno de sus primeros diez rebotes.*
```R
# rebotes.py

altura_inicial = 100  # variable altura inicial
rebote = 5/6         # variable proporción del rebote
num_rebote = 1      # donde inicia el conteo, en el primer rebote
altura_reb=altura_inicial*(rebote**num_rebote) #calculo de la altura

while num_rebote<= 10: # el fial del ciclo es de 10 rebotes
    print(num_rebote,  altura_inicial*(rebote**num_rebote)) # al colocar el print dentro del while, se genera unan tabla con los valores correspondientes a la salida de cada ciclo
    num_rebote = num_rebote + 1 # de este modo el numero de rebotes aumenta de a una vez por ciclo

print('Cantidad de rebotes', num_rebote) # al final de la salida quiero que indique la cantidad total de rebotes
print('Altura final', altura_reb) # al final de la salida quiero que indique la altura final alcanzada
```
#### Ejercicio 1.6: Saludos  
*Escribí un programa llamado saludo.py que pregunte el nombre de le usuarie, imprima un saludo (por ejemplo, "Hola, Juana") y termine.*
```py
nombre=input("Ingresá tu nombre:") # le indico la pregunta para generar el input y la asignación de la variable
print("Tu nombre es", nombre) # lo que veo en la salida
```

#### Ejercicio 1.7: La hipoteca de David
*David solicitó un crédito a 30 años para comprar una vivienda, con una tasa fija nominal anual del 5%. Pidió $500000 al banco y acordó un pago mensual fijo de $2684,11.*
```py
# hipoteca.py
saldo= 500000
tasa=0.05
pago_mensual=2684.11
total_pagado=0
mes=0

while saldo>0:
	if mes<=11:
		saldo= saldo*(1+tasa/12)-pago_mensual
		total_pagado= total_pagado + pago_mensual
		mes=mes+1
	else: 	
		saldo= saldo*(1+tasa/12)-pago_mensual
		total_pagado= total_pagado + pago_mensual
		mes=mes+1
print('Total pagado', round(total_pagado,2))
print('en',mes,'meses')
```

#### Ejercicio 1.8: Adelantos
```py
# hipoteca_adelantos.py
saldo= 500000
tasa=0.05
pago_mensual=2684.11
total_pagado=0
adelanto=1000
mes=0
while saldo>0:
	if mes<=11:
		saldo= saldo*(1+tasa/12)-pago_mensual - adelanto
		total_pagado= total_pagado + pago_mensual+adelanto
		mes=mes+1
	else: 	
		saldo= saldo*(1+tasa/12)-pago_mensual
		total_pagado= total_pagado + pago_mensual
		mes=mes+1
print('Total pagado', round(total_pagado,2))
print('en',mes,'meses')
```
#### Ejercicio 1.9: Calculadora de adelantos
*¿Cuánto pagaría David si agrega $1000 por mes durante cuatro años, comenzando en el sexto año de la hipoteca (es decir, luego de 5 años)?*
```py
# adelantos.py
saldo= 500000
tasa=0.05
pago_mensual=2684.11
total_pagado=0
pago_extra=1000
pago_extra_mes_comienzo=61
pago_extra_mes_fin=108
mes=0

while saldo>0:
	if (mes>=pago_extra_mes_comienzo and mes<=pago_extra_mes_fin):
		mes=mes+1
		saldo= saldo*(1+tasa/12)-pago_mensual - pago_extra
		total_pagado= total_pagado + pago_mensual+pago_extra
		
	else: 	
		mes=mes+1
		saldo= saldo*(1+tasa/12)-pago_mensual
		total_pagado= total_pagado + pago_mensual
		
print('Saldo restante:',round(saldo))
print('Total pagado:', round(total_pagado,2))
print('Meses:',mes)

```
#### Ejercicio 1.10: Tablas
*Modificá tu programa para que imprima una tabla mostrando el mes, el total pagado hasta el momento y el saldo restante.*
```py
#hipotecas_tabla.py
saldo= 500000
tasa=0.05
pago_mensual=2684.11
total_pagado=0
pago_extra=1000
pago_extra_mes_comienzo=61
pago_extra_mes_fin=108
mes=1


while saldo>0:
	if (mes>=pago_extra_mes_comienzo and mes<=pago_extra_mes_fin):
		saldo= saldo*(1+tasa/12)-pago_mensual - pago_extra
		total_pagado= total_pagado + pago_mensual+pago_extra
		mes=mes+1
	else: 	
		saldo= saldo*(1+tasa/12)-pago_mensual
		total_pagado= total_pagado + pago_mensual
		mes=mes+1
	print(round(total_pagado),round(saldo))

print('Total pagado:', round(total_pagado,2))
print('Meses:',mes)
```
#### Ejercicio 1.11: Hipoteca ajustado
*El ejercicio anterior necesita una corrección. David está pagando en el último mes más de lo debido, obteniendo un saldo negativo. Implementá la lógica en el código para poder corregirlo y que David pague solamente lo que debe.*
```py
# hipotecas_ajustado.py
saldo= 500000
tasa=0.05
pago_mensual=2684.11
total_pagado=0
pago_extra=1000
pago_extra_mes_comienzo=61
pago_extra_mes_fin=108
mes=1

while saldo>2684.11:
	if (mes>=pago_extra_mes_comienzo and mes<=pago_extra_mes_fin):
		saldo= saldo*(1+tasa/12)-pago_mensual - pago_extra
		total_pagado= total_pagado + pago_mensual+pago_extra
		mes=mes+1
	else: 	
		saldo= saldo*(1+tasa/12)-pago_mensual
		total_pagado= total_pagado + pago_mensual
		mes=mes+1
	print(round(total_pagado),round(saldo))

print('Total pagado:', round(total_pagado,2))
print('Meses:',mes)
```
