# Ember Quest: El secreto de la mansión ardiente
Objetivos del juego:

En busca de la Mansión Ardiente, Aiden dominará la magia del fuego para vencer a criaturas y guardianes en su camino. Enfrentándose a obstáculos llameantes, empleará sus habilidades mágicas estratégicamente para acceder al pergamino secreto. Mientras recolecta y usa sabiamente las pociones dispersas, se asegurará de mantener su vitalidad para enfrentar desafíos cruciales. Navegar con astucia entre trampas y desafíos será esencial para desentrañar el enigma resguardado en la cámara del Enigma Papyrus.

Pasos para el desarrollo de nuestro juego:

1.	Creación del terreno:
   
-	La creación del terreno se apoyó en el paquete de assets Flooded Grounds de Unity, fundamental para construir la imponente Mansión.
  
![Sin título](https://github.com/krivera65/ProyectoFinal/assets/143332773/8d4bd544-fe6d-44d6-b3ec-be19ad0040a5)

-	Para los árboles secos, se configuró un prefab utilizando el shader simple lit de Universal Render Pipeline, ajustando la frecuencia y el radio en el primer branch para generar varios árboles a partir del mismo prefab. Además, se añadió otro conjunto de ramificaciones y se posicionaron en un nivel alto para simular una búsqueda de luz solar natural y crear una atmósfera más siniestra.
  
![Sin título](https://github.com/krivera65/ProyectoFinal/assets/143332773/7e32ab53-ee56-4ecf-8cc3-4950da2e374b)

-	El aspecto visual de los árboles se logró descargando texturas de internet, creando materiales y asignándolos al mapa base de los árboles. Por otro lado, para los árboles que se encuentran a ambos lados del camino, se siguió un proceso similar, pero con ramas de mayor longitud y frecuencia en las hojas, generando así una sensación de bosque más denso y oscuro.

  ![Sin título](https://github.com/krivera65/ProyectoFinal/assets/143332773/e97aef01-0a15-4999-a872-af18e659fd36)

-	Para lograr una atmósfera nocturna, nublada y tenebrosa, se ajustó la temperatura de la luz direccional del objeto de juego, pasando de un tono cálido a uno frío.
  
![Sin título](https://github.com/krivera65/ProyectoFinal/assets/143332773/1a362d5d-c8ae-4a65-bda5-7454da6b9f63)

-	El terreno adquirió un aspecto negro con detalles de fuego gracias a la inclusión de una textura de roca de Unity y la descarga de imágenes de internet para pintar los detalles de fuego en la textura del terreno.

-	En relación con la simulación de lava, el efecto se logró al modificar el material water utilizado en clase a través del shader graph. La textura de agua fue reemplazada por una de lava obtenida en línea, ajustando sus parámetros para generar un movimiento más discreto, disminuyendo las olas y aumentando el valor de alfa para intensificar el color. Además, se alteró la velocidad de la textura para desacelerar el flujo aparente de la lava en el entorno, logrando así una representación más realista y evocativa del elemento en la escena de la mansión.

  ![Sin título](https://github.com/krivera65/ProyectoFinal/assets/143332773/4c048994-5c2b-4eca-9dc7-a4d5d3ad9452)

  
2.	Creación de personajes:
 	
-	Personaje principal (Aiden)


      El personaje principal, un mago modelado a partir de un personaje de Mixamo llamado Abe, fue dotado de funcionalidades            mediante una serie de scripts. Implementamos el script ShooterMovInput, permitiendo el disparo y el salto del personaje,          junto con el script ForwardMovement para asegurar su movimiento constante hacia adelante. Además, incorporamos la acción          dash, activada por las teclas A y D para moverse lateralmente, permitiendo al jugador sortear obstáculos que obstaculicen         su camino.

  ![IMG_3393](https://github.com/krivera65/ProyectoFinal/assets/143332773/cfb4bbfe-d780-4940-a9fb-c9819aaf891d)


![IMG_3378](https://github.com/krivera65/ProyectoFinal/assets/143332773/b3cc6071-2aa6-46bc-ac20-ee96848e7d7d)
![IMG_3379](https://github.com/krivera65/ProyectoFinal/assets/143332773/c7cbcaf3-49d2-4981-8a0a-acbb7c33696b)

Para transformar los disparos en bolas de fuego, ajustamos el color de las balas utilizando la misma textura empleada para        representar la lava. Modificamos el shader de las balas al shader de fireball, obtenido del efecto visual (VFX) de                agua/lava, logrando así el aspecto visual de fuego en las balas.

Para mantener siempre al personaje mirando hacia adelante, la cámara se posicionó detrás de él utilizando el shot point, lo       que crea la ilusión de que la cámara sigue sus movimientos. Esto asegura una perspectiva constante y dirigida hacia               adelante para el jugador.
  
-	Personajes secundarios (Enemigos)
Para lograr crear estos dos enemigos, tomamos los prefab de los respectivos enemigos y luego a cada uno se les añadieron los Script ForwardMovement, Life y ScoreOnDeath. La única diferencia entre ambos enemigos fue que al prefab del lobo se le dio una veocidad más rápida que al prefab del esqueleto.

        Lobos
 	![IMG_3392](https://github.com/krivera65/ProyectoFinal/assets/143332773/2b13fa9a-755f-4314-8637-ab9398b1d27b)

 	     Esqueletos
   ![IMG _3391](https://github.com/krivera65/ProyectoFinal/assets/143332773/87dc2bab-4383-4a74-a54c-c8e1012871fb)



3.	Llegada al objetivo final

    Cuando Aiden llegue a la cámara que alberga el enigma papyrus y lo toque, se desplegará una pantalla que indicará la           victoria. En este momento se activará el script de win or lose (Life y ScoreOnDeath), marcando el logro del objetivo y dando      fin al desafío, reconociendo el éxito del jugador al completar la tarea principal del juego.


   Demo de nuestro juego:
