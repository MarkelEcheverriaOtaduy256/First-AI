# First-AI
Code of a BASIC AI that transforms Celsious into fhrenheit 
"Una IA con una unica red neurinal muy básica, la misión sera convertir grados celsious en fahrenheit "

#Importamos desde el servidor diferentes redes neuronales

import tensorflow as ts     
import numpy as np
import matplotlib.pyplot as plt

#vamos a introducir una serie de datos celsious y fahrenheit 

celsious =np.array ([-40, -10, 0, 8, 15, 22, 38], dtype=float)
fahrenheit =np.array ([-40, 14, 32, 46, 59, 72, 100], dtype=float)

#Ahora voy a crear mi red neuronal de una sola neurona de imput con un único output

capa = tf.keras.layers.Dense(unit=1, input_shape= 1)
modelo= tf.keras.Sequential([capa])

#Voy a crear ahora la formula para darle un margen de error

modelo.compile(optimizer= tf.keras.optimizer.Adam (0.03), loss = "mean_squeared_error")

print ("Modelo Entrenado!!")

#Ahora vamos a generar una grafica donde nos explique como evoluciona el entrenamiento X e Y normal

ptl.xlabel("ciclo") #Nombre del eje X
ptl.Ylabel("error") #Nombre del eje Y
ptl.plot (historial.history [loss]) #Lo que deseo mostrar en la grafica
ptlshow()#MOstrar la grafica una vez que se acaba 

resultado = modelo.predict(np.array([134.0]))
print("El resultado es" + str(resultado[0][0]) + "Grados Fahrenheit")

