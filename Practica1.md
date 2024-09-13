# Práctica 1
## Integrantes:
- Dante Mejía Silva
- Atzin Morales Alejandre
## Introducción
La primera práctica del laboratorio de robótica consiste en la instalación del programa Epson RC+ y visualizar mediante ella los primeros movimientos con el robot. 

Epson es líder mundial en automatización industrial y ofrece una impresionante combinación de alto rendimiento y simplicidad. Respaldados por una reputación mundial por su fiabilidad y soporte excepcionales, los robots industriales Epson están proporcionando sistemas de fabricación automatizada y altamente productiva a un conjunto cada vez más amplio de sectores industriales en todo el mundo. [1]
## Instrucciones
### 1.- Instalar el programa EpsonRC+ correctamente
Primeramente, se descargó el archivo comprimido que contenía los archivos necesarios para instalar el programa.

![image](https://github.com/user-attachments/assets/230541df-64ae-4f64-868e-cd82b81694c4)

Posterior a ello se descomprimió la carpeta y se ejecutó como administrador el ejecutable con extensión .exe
.
![image](https://github.com/user-attachments/assets/71a3a9d1-0fb9-4116-bb29-97b562d4b2ee)

Se sigue con el proceso de instalación de manera sencilla y se ejecuta el programa.

![image](https://github.com/user-attachments/assets/e41732f1-5d29-4d7f-817f-90524a33c1e8)

Una vez dentro y antes de conectar al robot físico se indagó de manera curiosa en el simulador que proporciona el programa mediante los siguientes atajos.

![image](https://github.com/user-attachments/assets/ad588d89-646d-48f4-be4e-a3cee811ecce)

![image](https://github.com/user-attachments/assets/1384e36a-bbad-455f-9886-a23b88b702de)

![image](https://github.com/user-attachments/assets/247ad65c-ff8d-419a-8d4d-08b008016da9)

Una vez seleccionado lo anterior se mostrarán las siguientes pestañas.

![image](https://github.com/user-attachments/assets/5df4c270-9c72-4099-9c27-759405a59edd)

Prendemos el motor.

![image](https://github.com/user-attachments/assets/fc96d669-527a-437b-81fd-956026d2500d)

En el apartado de Jog & Teach se podrá visualizar botones que representan las articulaciones del robot y que al presionarlos mueven al mismo. 

![image](https://github.com/user-attachments/assets/e0a0d600-6570-489a-80d5-9896263f1f3f)

### 2.- Conexión al Robot Epson C4
Para conectar nuestra laptop y el programa al robot físico se necesita primero conectar el cable USB a nuestro dispositivo.

![image](https://github.com/user-attachments/assets/7333fc0b-15e4-422a-bf1c-8f562e39c8fa)

Posteriormente se selecciona en el programa el tipo de conexión USB.

![image](https://github.com/user-attachments/assets/a9c81205-a08d-40e4-a02a-2e016d66b24e)

Luego simplemente volvemos a correr el Robot Manager y empezamos a jugar con los joysticks.

### 3.- Conocer las partes del robot

El diseño del C4 de Epson es líder en los robots de 6 ejes compactos y posee una exclusiva altura de muñeca compacta y un diseño delgado del codo. Los robots C4 de Epson tienen excelente flexibilidad y fueron hechos para realizar grandes trabajos en espacios pequeños. Funciona con cargas útiles de hasta 4 kg mientras mantiene rápidas velocidades y tiempo de ciclo. [2]

La base es la parte inferior del robot que proporciona soporte estructural y estabilidad. Contiene la fuente de alimentación y los componentes electrónicos necesarios para el funcionamiento del robot.

Dicho robot cuenta con 6 articulaciones (J1, J2, J3, J4, J5 y J6) las cuales mueven en todo sentido al brazo de manera que le permite realizar diversas tareas.

![image](https://github.com/user-attachments/assets/a49bc19f-3910-4490-b92a-ff2ccb3fe3a1)

Cabe destacar su última articulación, la cual es una pinza impulsada por aire presurizado el cual pasa a través de los tubos azules conectados.

![image](https://github.com/user-attachments/assets/9c65a0a8-6715-4828-ba38-90613f25db90)

El aire es proporcionado de esta llave tipo palanca la cual para ser activada debe estar alineada con la manguera roja.

![image](https://github.com/user-attachments/assets/3a01b89b-bbd8-4953-a3c3-85a6f97d59a4)

El robot esta adentro de una cabina que sirve principalmente para proteger los componentes internos del robot como el polvo, humedad y otros contaminantes, además de evitar que los operadores entren en contacto accidental con partes móviles.

![image](https://github.com/user-attachments/assets/c4a09651-b7cc-4132-87d2-d1931fdc50ac)

Cuenta con 3 botones de para de emergencia en caso de cualquier posible accidente.

![image](https://github.com/user-attachments/assets/55473435-7762-45e9-8db2-7d2ccd8170e8)

El robot cuenta con diversos tipos de sensores entre ellos de posición, velocidad y aceleración en las articulaciones. También pueden incluir sensores de proximidad, cámaras de visión artificial, y sensores de fuerza y torque para detectar la interacción con objetos y adaptarse a cambios en el entorno.

La cabina cuanta con una unidad HMI para interactuar con posibles PLCs SIEMENS

![image](https://github.com/user-attachments/assets/8ee3cbd8-bd48-43a3-b26d-3fbc57a37350)

Para encender el motor se debe girar la pieza mostrada de color rojo.

![image](https://github.com/user-attachments/assets/f32bc5f9-7d77-4da1-b795-6f8a2b080afe)

El motor se alimenta con 220V mediante un tipo de enchufe especial.

![image](https://github.com/user-attachments/assets/3f131ee0-a510-45b7-9870-c633e883cd38)

### 3.- Movimiento del robot en world y joint
"World" y "Joint," son dos diferentes modos de mover el brazo robótico.

1.	Movimiento "World" (o cartesiano): En este modo, el movimiento del brazo robótico se especifica en términos de un sistema de coordenadas cartesiano, que se refiere a la posición del brazo en el espacio. En el modo "World" se puede mover el brazo en línea recta a lo largo de los ejes X, Y y Z del sistema de coordenadas. Esto es útil para tareas que requieren un movimiento lineal y preciso del efector final a través del espacio.

2.	Movimiento "Joint": En este modo el movimiento se controla a nivel de cada articulación individual del brazo robótico. En lugar de especificar posiciones en un espacio tridimensional aquí se controla directamente los ángulos de cada una de las articulaciones del brazo.
### 4.- Análisis de las Diferencias
•	Sistema de Control:

La principal diferencia entre los modos "World" y "Joint" radica en cómo se controla el movimiento del brazo robótico. El modo "World" utiliza coordenadas cartesianas para definir la posición y orientación del efector final en el espacio, mientras que el modo "Joint" controla el movimiento a través de los ángulos de cada una de las articulariones (J1-J6).

En el modo "World", las trayectorias al ser lineales podrían ser más fáciles de planificar porque están basadas en coordenadas. En el modo "Joint", las trayectorias al depender de la rotación de cada articulación puede resultar en movimientos más fluidos, pero más difíciles de planificar, especialmente si el robot tiene muchas articulaciones, sin embargo este modo puede ser útil para evitar colisiones que se podrían producir al emplear el modo “World”.
## Conclusiones
***Atzin Morales Alejandre:*** En esta primera se logró la instalación y configuración del software Epson RC+ y se exploraron los conceptos fundamentales del control de un brazo robótico, específicamente a través de los modos de movimiento "World" y "Joint". Además, esto permitió la familiarización con parte de la interfaz del software, así como con las capacidades del simulador antes de interactuar con el robot físico.

A través de la exploración práctica de los modos "World" y "Joint", se pudo comprender cómo estos diferentes enfoques de control ofrecen diversas ventajas según las necesidades de la tarea. El modo "World" proporciona un control sencillo y directo en un espacio cartesiano, ideal para movimientos lineales precisos. Por otro lado, el modo "Joint" permite un control más detallado a nivel de cada articulación, proporcionando mayor flexibilidad en entornos complejos o cuando se requiere evitar obstáculos.

Ambos modos de operación son esenciales para obtener mejores resultados en diferentes aplicaciones industriales. Esta práctica permitió sentar las bases para un entendimiento más profundo de las técnicas de programación y control en robótica que se verán a lo largo del curso así como preparación para desafíos más avanzados en futuras prácticas.

***Dante Mejía Silva:*** En esta primera fase del proyecto, se completó exitosamente la instalación y configuración del software Epson RC+, lo cual permitió adentrarse en los principios fundamentales del control de brazos robóticos. Se hizo un enfoque particular en los modos de movimiento "World" y "Joint", que son esenciales para el control preciso y eficiente del robot. La familiarización con la interfaz del software y las funcionalidades del simulador sentó las bases para una comprensión más profunda de estos conceptos antes de interactuar con el robot físico.

El análisis práctico de los modos de control evidenció cómo "World" facilita movimientos lineales y precisos en un espacio cartesiano, mientras que "Joint" ofrece un control detallado de cada articulación, lo que resulta útil en entornos más complejos. Este conocimiento no solo es fundamental para la programación y operación de robots en aplicaciones industriales, sino que también prepara a los participantes para enfrentar desafíos más avanzados en futuras sesiones prácticas.
## Referencias Bibliográficas 

[1] 	EpsonCompany, «Especialistas en automatización industrial». 2024, https://www.epson.es/es_ES/robots

[2] 	EpsonCompany, «Robot Epson C4 de 6 ejes compactos». 2024, https://epson.com.mx/Para-el-trabajo/Rob%C3%B3tica/6-Ejes/Robot-Epson-C4-de-6-ejes-compactos/p/RC4-A601ST75
