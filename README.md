# ActividadIntegradora

## Descripción de la problematica
El problema a resolver es poder generar una simulacion de la propagación de un virus, en este caso el COVID-19, para ver su comprtamiento.

## Descripcion de los agentes y modelos

### **Agentes**
<br/>
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

### **El entorno**
<br/>
El entorno o modelo en este caso estan puestos en un tablero/matriz. Cada uno de los espacios de este modelo representan una persona (agente) y no existen espacios vacíos, o espacios donde no exista un agente con un estado.
<br>
Al inicio de la simulacion, se colocan las personas(agentes) con estados aleatorios, lo cual es indicativo en una propagacion de un virus, por ejemplo en un aeropuerto, que no se sabe con certeza la cantidad de infectados que puede haber. Cada step (o en otras palabras fraccion de tiempo de la simulacion) los agentes perciben y actuan para actualizar su estado con las reglas descritas anteriormente.

#### Variables
Las variables significativas

#### Parámetros
Los parametros significativos

### Resultados
Los resultados representan


e.	Identifica las variables y los parámetros que determinan el funcionamiento del sistema.
f.	Describe el proceso de simulación
g.	Discute clara y concisamente los resultados obtenidos
h.	Agrega el link al repositorio.
5.	Actualiza el repositorio y verifica que todo lo anterior esté cargado.
6.	Descarga el repositorio en .ZIP y súbelo a tu portafolio de eLumen.


