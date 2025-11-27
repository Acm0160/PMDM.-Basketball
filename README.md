README – Basketball Score App
Este proyecto consiste en una aplicación sencilla para Android que permite llevar el marcador de un partido de baloncesto. La he programado en Java y he utilizado dos pantallas: una para manejar el marcador en tiempo real y otra para mostrar el resultado final del partido cuando termina.

Pantalla Principal (MainActivity)
En la pantalla principal he colocado dos marcadores: uno para el equipo local y otro para el visitante. Debajo de cada marcador he añadido botones para sumar puntos (+1 y +2) y otro para restar (-1), siempre evitando que el marcador pueda bajar de cero.

También incluí un botón de reinicio que devuelve ambos marcadores a cero, y otro botón que permite pasar a la siguiente pantalla para ver el resultado final.

En el centro de la pantalla puse una imagen de una pelota de baloncesto (basketball.png) para que la interfaz fuera más visual y adecuada al tema del proyecto.

– Pantalla principal con los marcadores y la imagen
<img width="398" height="887" alt="image" src="https://github.com/user-attachments/assets/743e79be-04fb-4390-86c3-68d7a5443bab" />


– Suma y resta de puntos en funcionamiento
<img width="398" height="307" alt="image" src="https://github.com/user-attachments/assets/83f4adf3-d83e-40bf-a31e-f2f45113813d" />


Pantalla de Resultado (ScoreActivity)
Cuando se pulsa el botón para ver los resultados, la aplicación abre una segunda pantalla donde se muestra el marcador final. Además, determina automáticamente si ha ganado el equipo local, el visitante o si ha habido empate.

– Pantalla de resultado final
<img width="246" height="149" alt="image" src="https://github.com/user-attachments/assets/b9c5f23a-2b57-4099-914a-86f29fa93b9a" />


Implementación del Data Binding
En este proyecto he usado Data Binding para poder acceder a los elementos del layout directamente desde el código Java sin necesidad de usar findViewById. Para ello activé Data Binding en el archivo build.gradle y utilicé las clases generadas automáticamente, como ActivityMainBinding y ActivityScoreBinding.

Gracias a esto, el código queda más limpio y es más fácil trabajar con la interfaz.

Paso de datos entre Activities
Para enviar el marcador a la pantalla final, utilicé un Intent. Antes de abrir la segunda actividad, guardo las puntuaciones con putExtra, y en la segunda pantalla recupero esos valores con getIntExtra.

Este paso es el que permite que ScoreActivity reciba los puntos que se han ido sumando en MainActivity y muestre el resultado real del partido junto con el ganador.
