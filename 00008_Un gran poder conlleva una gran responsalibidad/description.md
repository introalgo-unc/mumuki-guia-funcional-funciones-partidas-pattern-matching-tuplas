Ahora que aprendimos a como deconstruir una tupla vamos a querer, como siempre, utilizarlo en todos lados, **pero eso no siempre es conveniente**.

El chiste de la tupla es que no voy a querer siempre tratar los valores que la componen por separado, sino no tendría sentido agruparlos.

Para dar un ejemplo aprovechemos la tupla que habíamos creado para representar un soldado en el ejercicio anterior. Dijimos que la tupla estaba compuesta por el nombre, la fuerza y la destreza, ahora queremos una función `soldadoLeGanaA\2` que recibe dos tuplas de este tipo, o mejor dicho dos soldados, y devuelve si el primero tiene mayor poder que el segundo:

```
soldadoLeGanaA ganador perdedor = poderSoldado ganador > poderSoldado perdedor
```

Como vemos a la función `soldadoLeGanaA\2` no le interesa deconstruir o saber como está compuesta la tupla del soldado, sino que usa al soldado como una [abstracción](http://uqbar-wiki.org/index.php?title=Abstracci%C3%B3n), y es la función `poderSoldado\1` la que al si utilizará los valores que contiene para poder calcular el poder.

Además el día de mañana si cambiamos nuestro sistema y agregamos un valor más a la tupla (por ejemplo la salud del soldado) no vamos a necesitar cambiar aquellas funciones que como `soldadoLeGanaA\2` no trabajan con sus valores internos, sino solo con aquellas que sí deconstruyen a la tupla como `poderSoldado\1`.