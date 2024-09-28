# MovieBudget
Problema planteado para la asignatura de Infraestructura Virtual.

## Descripción del problema
Los guionistas o directores de cine _independiente_ que quieren rodar su primera película no tienen referencias de cuánto les puede costar hacerla. Dependiendo del tipo de película que quieran hacer, de su duración, de la cantidad de personajes y localizaciones que tiene, deberán ajustar su presupuesto y analizar si es posible llevarla acabo, y para ello la única posibilidad que tienen es buscar información acerca de películas similares en internet. Sin embargo, este proceso es muy completo y molesto, ya que no siempre van a encontrar toda la información necesaria y, además, puede que lo que quieran sea analizar qué tipo de película podrían hacer dado el presupuesto con el que cuentan, para no comenzar la producción de una película que pueda ser imposible de rodar. Los datos que se manejarán a la hora de analizar películas similares con el objetivo de determinar si se podría llevar a cabo un determinado proyecto (los cuáles se extraerán de una base de datos de dominio público obtenida de la plataforma Kaggle, la cuál contiene los siguientes datos de un total de 4803 películas, que oscilan entre superproducciones de Hollywood hasta películas con un presupuesto nulo) serán: duración en minutos de la película, número de actores, número de trabajadores detrás de cámaras, género de la película, presupuesto, beneficios en taquilla, recepción crítica de la película, número de localizaciones e idioma en el que ha sido rodada.

## Descripción de la solución
Desarrollar un algoritmo que, cuando el usuario introduzca el género de su película, se filtren las películas que pertenezcan a dicho género. Una vez hecho esto, se filtrarán películas que tengan un presupuesto inferior, igual o un poco superior (el porcentaje de presupuesto por el cual las películas analizadas pudieran superar al presupuesto del usuario podría ser determinado por el propio usuario, o ser de manera predeterminada un porcentaje pequeño, no superior, por ejemplo, al 15%). Cuando se haya obtenido el conjunto de películas de género similar y con un presupuesto asumible, se analizarán los beneficios (ajustados al presupuesto de cada película) y la recepción crítica de cada una, y se ordenarán mediante un sistema de ponderación (se asignará un **score** a cada, determinando un 60% de importancia a la recaudación y un 40% a la recepción de la película). Una vez ordenadas se seleccionarán los 5 mejores casos y se analizarán los detalles técnicos que afectan al presupuesto de la película, como la duración de la misma, los actores y trabajadores contratados, etc... Y se establecerá una media para ofrecerle al usuario unos rangos en los cuáles debería trabajar la película para optimizar su presupuesto (en concreto se indicarán **rangos** que oscilen entorno a un 10% de la media obtenida en cada apartado analizado de la película). Una vez hecho esto se establecerán criterios para determinar si una película es **viable** o no, en concreto críticas y beneficios mínimos, y si de la lista de 5 mejores casos de producción 3 de esas películas cumple esos requisitos se considerará que la película que se quiere producir es viable. Si no, el programa se lo hará saber al usuario y hará de nuevo listas de los 5 mejores casos de producción, esta vez de cada uno de los géneros de películas restantes, analizándose de nuevo la viabilidad de cada una, y se extraerá una lista ordenada de los 3 géneros recomendados según el presupuesto de la película que se quiere realizar, la cuál se mostrará al usuario. De esta manera, al terminar el proceso, el usuario recibiría una indicación sobre si su película es viable de realizar, recomendaciones de detalles técnicos para optimizar el presupuesto de la misma y, en caso contrario, recomendaciones de otros géneros de películas a los que poder dedicar el presupuesto del usuario.

## Configuración del repositorio
Se puede observar, a través de los siguientes enlaces, las configuraciones que se han llevado a cabo en el repositorio del proyecto.
- [Asignación de nombre y correo de usuario](./configuracion/nombre_correo.png)
- [Generación de una clave SSH para el establecimiento de una conexión segura con Github](./configuracion/generar_clave.png)
- [Adición de la clave SSH al repositorio de Github](./configuracion/añadir_clave.png) 
