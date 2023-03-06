# ActividadIntegradora

## Descripción de la problematica
El problema a resolver es poder generar una simulacion de la propagación de un virus, en este caso el COVID-19, para ver su comprtamiento.

## Descripcion de los agentes y modelos

## **Agentes**
En este caso solo existe un agente, que representa un humano en esta situación. Este humano representado por una celda puede estar Viva y Sana (color Verde), Viva e infectada (color Morado) o Muerta (color rojo).

#### Acciones
Este agente puede hacer las siguientes cosas con respecto a como este su entorno:
* Infectarse
* Morirse
* Nacer
<br>
Claro nada de esto puede hacer sin antes percibir su entorno, lo cual al final de cuentas dicta sus acciones. La relacion de las acciones y percepciones con como un set de reglas.

#### Percepciones
En este caso como el sistema que queremos modelar es la propagación de un virus que puedes obtener por lo que te rodea, las percepciones del agente se basan en recorrer cada uno de sus vecinos para saber que hacer. Las interacciones entre estos agentes son entre ellos mismos, dependiendo de sus estados que mencionamos al inicio.
<br>
* Si la celda esta en estado vivo y sano (verde) y mas de 3 personas (o vecinos incluyendo diagonales), esta celda se infecta y por lo tanto puede **infectar (accion)** a otros si se cumple esta condicion en otra parte. cambia su estado de viva-sana a viva-infectada verde->morado.
* Si la celda esta viva e infectada y le rodean mas de 2 personas (vecinos) que tambien estan infectadas, esta celda se **muere (accion)**, es decir cambia su estado de viva-infectada a muerta. morada -> roja.
* Si la celda esta muerta pero existen 3 personas o mas (vecinos), esta puede **nacer (acción)**. Pasa su estado de muerta a viva-sana, rojo->verde.

## **El entorno**
El entorno o modelo en este caso estan puestos en un tablero/matriz. Cada uno de los espacios de este modelo representan una persona (agente) y no existen espacios vacíos, o espacios donde no exista un agente con un estado.
<br>
Al inicio de la simulacion, se colocan las personas(agentes) con estados aleatorios, lo cual es indicativo en una propagacion de un virus, por ejemplo en un aeropuerto, que no se sabe con certeza la cantidad de infectados que puede haber. Cada step (o en otras palabras fraccion de tiempo de la simulacion) los agentes perciben y actuan para actualizar su estado con las reglas descritas anteriormente.

#### Variables
En este modelo, existen variables significativas que determinan el funcionamiento del sistema de manera grande.
* **moore = True**. Esta variable nos indica que al checar por vecinos, tambien tome en cuenta los diagonales, algo que afecta grandemente si no se toma en cuenta. Si esto fuera en false, la propagacion del virus, seria con menos frecuencia.
* Existen variables como: **total_live_agentes, total_infect_agents y total_die_agents** que son variables que existen para contabilizar y realizar un analisis para los resultados. Estos se usan para recolectar datos despues.

#### Parámetros
En este modelo no hay tantos parametros, ya que es una simulación simple. Pero si se toma en cuenta en los agentes(personas) un unique_id que se representa por su posición en la matriz para identificarlo.
* **self.width y self.height**. Estas variables indican el tamaño del modelo y por ende la cantidad de agentes y la escala de la simulacón que sirven de parametros de entrada a la hora de crear el modelo.

## Resultados
Usando la visualizacion de mesa podemos visualizar la propagación del virus usando grid de mesa y usando colores diferentes para los diferentes estados de los agentes. De esta manera se puede visuzaliar cada step que se realizo en la simulación y ver su comportamiento.

Los resultados se presentan por medio de gráficas. Anteriormente vimos como algunas variables almacenaban información sobre los agentes y el modelo. Usando el mesa.datacollection importando DataCollector, podemos fácilmente desplegar la informacion que colectamos en gráficas, que muestran lo sigueinte:
* Para la simulación visualizada se puede ver una gráfica indicando la cantidad de celdas que estan vivas, muertas, infectadas y sanas representadas por sus colores respectivos: verde, rojo, morado y azul.
* La gráfica de en medio describe el tiempo promedio que una persona vive antes de morirse.
* Existe otra grafica que representa el promedio de los números antes mencionados, pero con respecto a muchas simulaciónes llevadas a cabo para conocer su tendencia/comportamiento en promedio.


