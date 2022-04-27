# critica_peliculas
el link del rpositorio es el siguiente(https://github.com/Barroso03/critica_peliculas.git) 


Rubén te voy a explicar aqui todo lo que he hecho pero hay cosas que no me salen y llevo todo el dia intentando.
esta es la clase para hallar todos los calculos

´´´
#importa pandas para trabajar con dataframes
import pandas as pd
from statistics import *
#importa matplotlib para graficar
import matplotlib.pyplot as plt
# importa math para trabajar con funciones matematicas
from math import *
#Crea la clase resultadosestadisticos
class resultadosestadisticos:
    datos = pd.read_csv("C:/critica_peliculas/criticapelicula.csv")
    # crea el constructor
    def __init__(self,datos,media_aritmetica):
        self.datos = datos
        datos = pd.read_csv("C:/critica_peliculas/criticapelicula.csv")
        self.media_aritmetica = media_aritmetica
    # importa la funcion media_aritmetica
    def media_aritmetica(self,media_aritmetica,datos):
        # obtiene la media aritmetica
        self.media_aritmetica = media_aritmetica
        media_aritmetica = list(datos["Opiniones(xi)"])*list(datos["Cantidad_votantes(ni)"])/sum(datos["Cantidad_votantes(ni)"])
        # retorna la media aritmetica
        return media_aritmetica
    # importa la funcion varianza
    def varianza(self,varianza,datos):
        # obtiene la varianza
        self.varianza = varianza
        varianza = sum(datos["Opiniones(xi)"]**2)*sum(datos["Cantidad_votantes(ni)"])/sum(datos["Cantidad_votantes(ni)"])
        # retorna la varianza
        return varianza
    # importa la funcion desviacion_típica
    def desviacion_tipica(self,desviacion_tipica,datos):
        # obtiene la desviacion tipica
        self.desviacion_tipica = desviacion_tipica
        desviacion_tipica = sqrt(self.varianza)
        # retorna la desviacion tipica
        return desviacion_tipica
    # importa la funcion percentiles y calcula los percentiles 68, 95 y 99
    def percentiles(self,percentiles,datos):
        # obtiene los percentiles
        self.percentiles = percentiles
        percentiles = [0.68,0.95,0.99]
        # retorna los percentiles
        return percentiles
    def  gráfico(self,grafico,datos):
        # obtiene el gráfico
        self.grafico = grafico
        grafico = plt.hist(datos["Opiniones(xi)"],bins=20)
        # retorna el gráfico
        return grafico
        
# printea la clase resultadosestadisticos
print(resultadosestadisticos.media_aritmetica("media_aritmetica",'datos'))
print(resultadosestadisticos.varianza("varianza",'datos'))
print(resultadosestadisticos.desviacion_tipica("desviacion_tipica",'datos'))
print(resultadosestadisticos.percentiles("percentiles",'datos'))
´´´
despues de esto haria un lanzador en el cual haria una clase en la cual hiciese todos los calculos y luego en el main importaria el lanzador para terminar.
El csv que he escogido es el del portal de la asignatura aunque no tenga muchos datos.
El archivo esta en un commit

Se que el trabajo esta un poco mal porque no funciona y eso pero he aprendido bastante.



 


