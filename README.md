# ActividadIntegradora

## Descripción de la problematica
El problema a resolver es poder generar una simulacion de la propagación de un virus, en este caso el COVID-19, para ver su comprtamiento.

## Descripcion de los agentes y modelos

### Agentes
En este caso solo existe un agente, que representa un humano en esta situación. Este humano representado por una celda puede estar Viva y Sana (color Verde), Viva e infectada (color Morado) o Muerta (color rojo).

#### Acciones
Este agente puede hacer las siguientes cosas con respecto a como este su entorno:
* Infectarse
* Morirse
* Nacer
Claro nada de esto puede hacer sin antes percibir su entorno, lo cual al final de cuentas dicta sus acciones. La relacion de las acciones y percepciones con como un set de reglas.

#### Percepciones
En este caso como el sistema que queremos modelar es la propagación de un virus que puedes obtener por lo que te rodea, las percepciones del agente se basan en recorrer cada uno de sus vecinos para saber que hacer.
* Si la celda esta en estado vivo y sano (verde) y mas de 3 personas (o vecinos incluyendo diagonales), esta celda se infecta y por lo tanto puede **infectar (accion)** a otros si se cumple esta condicion en otra parte.
* Si Celda esta viva e infectada 

### El entorno
El entorno o modelo

#### Variables
Las variables significativas

#### Parámetros
Los parametros significativos

### Resultados
Los resultados representan



b.	Describe los agentes involucrados así como sus acciones y percepciones
c.	Describe cómo interactúan y se comunican dos o más agentes del mismo 
d.	Describe el entorno
e.	Identifica las variables y los parámetros que determinan el funcionamiento del sistema.
f.	Describe el proceso de simulación
g.	Discute clara y concisamente los resultados obtenidos
h.	Agrega el link al repositorio.
5.	Actualiza el repositorio y verifica que todo lo anterior esté cargado.
6.	Descarga el repositorio en .ZIP y súbelo a tu portafolio de eLumen.


