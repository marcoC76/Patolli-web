Patolli
Adaptación digital del Patolli, juego mesoamericano de azar y estrategia. El proyecto permite jugar en el navegador con un tablero interactivo, tiradas animadas, registro de jugadas y diferentes modalidades.
> **Nota:** Este proyecto presenta una adaptación de reglas para jugar. Las modalidades y reglas descritas aquí corresponden a esta implementación y no deben interpretarse como una reconstrucción histórica definitiva de todas las variantes del Patolli.
Contenido
Descripción
Características
Modos de juego
Reglas del juego
Modo clásico
Modo arqueológico
Reto de Macuilxóchitl
Cómo jugar
Controles e interfaz
Instalación y ejecución
Tecnologías
Estructura del proyecto
Descripción
El Patolli es uno de los juegos más antiguos de Mesoamérica. Se asocia con distintas culturas mesoamericanas y combina azar y estrategia. En esta adaptación, los jugadores recorren un camino dispuesto en forma de cruz diagonal, utilizando frijoles o elementos equivalentes como dados.
El objetivo general es ser el primero en completar el recorrido con todas las fichas y sacarlas del tablero. Las condiciones específicas dependen del modo seleccionado.
Características
Tablero interactivo dibujado en un elemento `canvas`.
Interfaz adaptable a pantallas de escritorio y dispositivos móviles.
Tres modalidades: Clásico, Arqueológico y Solo Dados.
Partidas de 1 jugador contra la IA, de 2 a 4 jugadores o simulación de 4 IA.
Selección de dificultad de la IA (fácil o difícil) cuando se juega contra ella.
Tiradas animadas de frijoles o dados especiales.
Movimiento y captura de fichas.
Indicadores de zonas seguras, puntas y panteones.
Registro de jugadas durante la partida.
Efectos de sonido que pueden activarse o desactivarse.
Guardado local de la partida y opción para continuarla.
Reto opcional de Macuilxóchitl en el modo Arqueológico.
Modos de juego
Al iniciar, selecciona una modalidad:
Modalidad	Elementos de azar	Uso
Clásico (Patolli)	5 frijoles	Partida con las reglas del modo clásico.
Arqueológico (Zoom)	4 dados o tablitas especiales	Partida con reglas avanzadas y eventos especiales.
Solo Dados	4 elementos especiales	Utiliza el simulador de tiradas junto con un tablero físico.
En el modo Arqueológico puedes seleccionar la apariencia de los elementos de tirada: tablitas de madera, frijoles, cañas o palitos.
Reglas del juego
Elementos
Tablero: camino de casillas con forma de cruz diagonal o aspa.
Fichas: cada jugador utiliza fichas de un color.
Dados: frijoles, tablitas, cañas o palitos con una cara marcada y otra lisa, según la modalidad.
Modo clásico
Fichas y recorrido
Cada jugador cuenta con 6 fichas.
El recorrido tiene 52 casillas.
Las fichas avanzan en sentido horario.
En cada turno puedes elegir qué ficha mover, siempre que el movimiento sea válido.
No puedes terminar el movimiento en una casilla ocupada por una ficha propia.
Tirada
Se utilizan 5 frijoles, cada uno marcado con un punto blanco en una de sus caras.
Lanza los cinco frijoles.
Cuenta cuántos muestran el punto blanco hacia arriba.
Ese número determina el avance: de 0 a 5 casillas.
Si los cinco caen con la cara lisa hacia arriba, el resultado es 0 y pierdes el turno.
Ingreso y movimiento
Para ingresar una ficha necesitas obtener un resultado mayor que 0.
La ficha entra en la casilla correspondiente al valor de la tirada de su recorrido.
Después puedes elegir qué ficha mover en cada turno, siempre que el movimiento sea válido.
Captura
Si una ficha termina exactamente en una casilla ocupada por una ficha rival, la captura. La ficha capturada se retira del tablero y debe comenzar de nuevo.
Zonas seguras
Las casillas especiales marcadas con símbolos —generalmente triángulos o aspas— son zonas seguras. Una ficha situada en ellas no puede ser capturada.
Salida
Una ficha debe completar el recorrido de 52 casillas. En esta modalidad no es necesario obtener el número exacto: cualquier tirada que lleve a la ficha más allá de la última casilla permite sacarla.
Modo arqueológico
Esta modalidad incorpora reglas adicionales de movimiento, nacimiento de fichas y casillas especiales.
Fichas y recorrido
Cada jugador cuenta con 3 fichas.
El recorrido tiene 40 casillas.
Tirada de los cuatro dados especiales
Se utilizan cuatro elementos. Cada uno tiene una cara lisa y otra marcada con 1, 2, 3 o 4 puntos, respectivamente.
Resultado	Valor	Explicación
Las cuatro caras lisas	0	Pierdes el turno.
Solo el dado de 1 punto marcado	1	Una cara marcada y tres lisas.
Solo el dado de 2 puntos marcado	10	Una cara marcada y tres lisas.
Solo el dado de 3 puntos marcado	15	Una cara marcada y tres lisas.
Solo el dado de 4 puntos marcado	20	Una cara marcada y tres lisas.
Dos dados marcados y dos lisos	2	No importa cuáles sean los dados marcados.
Tres dados marcados y uno liso	3	No importa cuál sea el dado liso.
Los cuatro dados marcados	5	El valor máximo regular es 5.
Nacimiento de fichas
Para ingresar una ficha debes obtener 1, 2 o 3.
Primera ficha: si todavía no tienes fichas en el tablero y obtienes 1, 2 o 3, tu primera ficha nace directamente en la casilla 5, la primera medialuna de tu recorrido.
Segunda y tercera fichas: para ingresar una ficha adicional, la ficha anterior debe haber superado la zona central del tablero (casilla 7). Las fichas de refuerzo nacen en la casilla 1.
En tu turno puedes elegir entre avanzar una ficha que ya esté en el tablero o hacer nacer otra, siempre que cumplas las condiciones de nacimiento.
Orden de movimiento
En el primer tiro del turno, si decides avanzar una ficha que ya está en el tablero, debes mover la ficha más adelantada.
Si obtienes tiros adicionales por ser Grande o por caer en una casilla de Punta, puedes repartir esos movimientos y elegir la ficha que prefieras.
Ser Grande
Un jugador se convierte en Grande cuando consigue:
Introducir una ficha en la Zona Final, que comprende las últimas 13 casillas del recorrido; o
Sacar una ficha del tablero.
Mientras seas Grande, tienes 3 tiros por turno en lugar de 1.
Puntas y panteones
Puntas de la estrella: si una ficha cae exactamente en una de las casillas de las puntas de la cruz, obtienes un tiro extra.
Panteones: si una ficha está detenida en un Panteón y obtienes una tirada gigante (10, 15 o 20), esa tirada se anula y vale 0.
Zona Final: el cansancio
Las últimas 13 casillas antes de la salida forman la Zona Final. Si una ficha está en esta zona y obtienes una tirada gigante (10, 15 o 20), el resultado se reduce a 1.
Regla del Puerco
Para sacar una ficha en el modo Arqueológico necesitas obtener el número exacto de casillas que le faltan para salir.
Si obtienes un número mayor y te pasas de la salida, la ficha se convierte en Puerco y debe recorrer una vuelta completa adicional: se agregan 40 casillas a su recorrido.
Reto de Macuilxóchitl (opcional)
En el modo Arqueológico puedes activar el reto de Macuilxóchitl, dios asociado con las flores, los juegos y el azar. En esta variante funciona como una fuerza que recorre el tablero y amenaza a las fichas.
Nacimiento: despierta y entra al tablero en una medialuna cuando el primer jugador ingresa su primera ficha.
Movimiento: se mueve antes que el jugador en turno y avanza el doble del valor de la tirada del jugador.
Recorrido: su movimiento es cíclico y no tiene un final.
Captura divina: si cae en la misma casilla que una ficha, la devora. La ficha debe volver a nacer desde fuera del tablero.
Debilidad: si cae exactamente en una medialuna (los extremos de la cruz), en su siguiente movimiento solo avanza 1 casilla, sin importar el resultado de la tirada del jugador.
Consejos de estrategia
Aprovecha las zonas seguras: úsalas como refugio para reducir el riesgo de captura.
Planea la salida: en el modo Arqueológico necesitas un resultado exacto; una tirada demasiado alta puede convertir tu ficha en Puerco.
Consigue el estado Grande: entrar en la Zona Final o sacar una ficha te permite realizar tres tiros por turno.
Ten presentes los panteones: si una ficha está detenida en uno de ellos, una tirada de 10, 15 o 20 se anula.
Administra tus nacimientos: en el modo Arqueológico, avanzar la primera ficha más allá de la zona central habilita el ingreso de las siguientes.
Cómo jugar
Abre la aplicación en el navegador.
Selecciona el modo de juego.
Elige el número de jugadores:
1 jugador vs IA: juegas contra un oponente controlado por la computadora.
2, 3 o 4 jugadores: partida multijugador local por turnos.
4 IA: simulación de una partida entre cuatro jugadores controlados por la computadora.
Si juegas contra la IA, selecciona su dificultad.
En el modo Arqueológico, decide si activar el reto de Macuilxóchitl y selecciona el estilo visual de los dados.
Pulsa Iniciar partida.
Pulsa el botón de tirada para lanzar los elementos de azar.
Sigue las indicaciones en pantalla y selecciona la ficha o acción disponible.
Consulta el registro de jugadas para revisar los acontecimientos de la partida.
Modalidad Solo Dados
Selecciona Solo Dados para utilizar la aplicación como lanzador de los cuatro elementos de azar mientras juegas con un tablero físico. Esta modalidad no inicia una partida de tablero dentro de la aplicación.
Controles e interfaz
Tirar Frijoles: realiza la tirada correspondiente al modo seleccionado.
Tablero: selecciona una ficha o casilla para realizar las acciones disponibles.
Sonido: ON/OFF: activa o silencia los efectos de sonido.
Registro de Jugadas: muestra los eventos y movimientos de la partida.
Salir de la partida: permite regresar al menú; la aplicación indica que el progreso se guardará automáticamente.
Cargar Partida: aparece cuando existe una partida guardada en el navegador.
Manual de reglas: abre `reglas.html` en una pestaña nueva.
Instalación y ejecución
Opción 1: abrir localmente
Descarga o clona el repositorio.
Conserva juntos los archivos del proyecto.
Abre `index.html` en un navegador moderno.
Para probar correctamente las funciones de aplicación web progresiva y el registro del service worker, es recomendable ejecutar el proyecto mediante un servidor local o publicarlo en un servicio de alojamiento estático.
Opción 2: publicar en GitHub Pages
Crea o abre un repositorio en GitHub.
Sube los archivos del proyecto respetando sus nombres y rutas.
En la configuración del repositorio, entra en Pages.
Selecciona la rama y la carpeta desde donde se publicará el sitio.
Guarda los cambios y espera a que GitHub Pages genere la dirección pública.
Abre la dirección publicada desde el navegador.
Archivos complementarios
El archivo principal contiene referencias a los siguientes recursos. Si se utilizan en la versión publicada, deben estar disponibles en las rutas indicadas:
`reglas.html`: manual de reglas que se abre desde la interfaz.
`manifest.webmanifest`: metadatos para la instalación como aplicación web.
`apple-touch-icon.png`: icono para dispositivos Apple.
`sw.js`: service worker registrado por la aplicación.
La partida se guarda en el almacenamiento local (`localStorage`) del navegador. Por ello, el guardado pertenece al navegador y dispositivo donde se juega; no es una sincronización en la nube.
Tecnologías
HTML5: estructura de la aplicación.
CSS3: diseño visual adaptable, paneles, animaciones y presentación de los elementos.
JavaScript: lógica del juego, turnos, tiradas, movimientos, capturas y comportamiento de la interfaz.
Canvas API: representación gráfica del tablero y las fichas.
Web Audio API: generación de efectos de sonido.
Local Storage: persistencia local de las partidas.
Service Worker y Web App Manifest: soporte de características de aplicación web progresiva, mediante los archivos complementarios correspondientes.
No se requiere un proceso de compilación para el archivo `index.html`.
Estructura del proyecto
Una estructura sugerida para publicar el proyecto es:
```text
patolli/
├── index.html
├── reglas.html
├── manifest.webmanifest
├── apple-touch-icon.png
└── sw.js
```
`index.html` es el punto de entrada de la aplicación. Los demás archivos son recursos complementarios referenciados por el documento principal.
---
Patolli — una adaptación digital para explorar el azar, la estrategia y las variantes de este juego mesoamericano.
