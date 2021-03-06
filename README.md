
# Realidad Aumentada con Vuforia

Este práctica ha sido desarrollado en la asignatura de **Interfaces Inteligentes** del itinerario de computación del **_Grado en Ingeniería Informática_** de la **ULL**.

Práctica realizada con **Víctor Hernández Pérez** (alu0100697032) y **José Manuel Hernández Hernández** (alu0100697032).
## Descripción de la práctica

Crear proyecto de Vuforia (**aplicación**) para representar una **_escena 3D sobre una imagen objetivo_**.

Utilización de **Unity 3D**, la cual es una herramienta que nos ayuda a desarrollar videojuegos para diversas plataformas mediante un editor y scripting para crear videojuegos con un acabado profesional.

![Pantalla inicial](https://github.com/gcpmendez/VuforiaArt/blob/master/vuforia4.JPG?raw=true)


## Pasos realizados:
> **NOTA:**  _Al final poseen la URL's a las páginas oficiales de los distintos archivos de descargas nombrados a continuación_    

**1er paso:** Descargamos **_UNITY_** en su versión última o final.   
**2do paso:** Descargamos el **_SDK de Vuforia para Unity_**. _Al final poseen la URL a la página oficial de descargas_   


**3er paso:** Creamos un nuevo proyecto de Unity importando el **_vuforia-unity-5-0-6.unitypackage (33.16 MB)_**. Nos debería quedar algo parecido a la siguiente imagen:

![Project](https://github.com/gcpmendez/VuforiaArt/blob/master/vuforia5.JPG?raw=true)

**4to paso:** Pasamos a crear nuestros objetos, nos vamos a la carpeta de **_Assets>Vuforia>Prefabs_** y arrastramos **ARCamera** hasta la escena, hacemos lo mismo con el **ImageTarget**. Por último añadimos el objeto que queremos que aparezca en 3D, yo he añadido un f16 descargado desde la store de Unity. Quedaría así:

![Project](https://github.com/gcpmendez/VuforiaArt/blob/master/vuforia6.JPG?raw=true)



> **NOTA:** Deberemos escalar y posicionar el objeto 3D descargado. Le he añadido la luz direccional para dar más realismo a la escena.

**5to paso:** Añadida clave de licencia de vuforia al Unity, para ello agregaremos una.
![vuforia developer portal](https://github.com/gcpmendez/VuforiaArt/blob/master/vuforia9.JPG?raw=true)  

Luego la clave generada la introducimos en Unity.
![vuforia developer portal](https://github.com/gcpmendez/VuforiaArt/blob/master/vuforia10.JPG?raw=true)

**6to paso:** Añadida la cámara, la base y el objeto ahora nos toca crear la **base de datos de la imagen** que queremos utilizar como patrón para que aparezca el F16.  

Para ello nos vamos a ImageTarget Database en vuforia; nos registramos, creamos la base de datos y subimos la imagen elegida como patrón.

![vuforia developer portal](https://github.com/gcpmendez/VuforiaArt/blob/master/vuforia7.JPG?raw=true)

Creada la base de datos en Target Manager, nos la descargamos y la importamos (doble click en el archivo descargado) al proyecto de Unity 3D.

Importada la BD de ImagenTarget seleccionamos el objeto Image Target y añadimos como patrón la imagen deL suelo.

![vuforia developer portal](https://github.com/gcpmendez/VuforiaArt/blob/master/vuforia8.JPG?raw=true)
> **Nota:** Cambiaremos el ancho según las propiedades de la imagen.

**7mo paso:** Configurada ya la escena, pasamos a crear la aplicación para instalarla en nuestro dispositivo **Android**.
* En **File > Build Settings :**
* Nos aseguramos que este seleccionada nuestra escena, sino Clicamos sobre 'add current' y seleccionamos.
*  Pinchamos en el simbolo de Android y nos aseguramos que Default Orientation no esta en Auto Rotation, establecemos 'landscape Left'  
* En **Players Settings :**
* Minimum API Level esta a Android 2.3.1 'Jelly Bean' (API level 9)   
* Bundle Identifier esta a un nombre valido (e.g. com.mycompany.firstARapp). Nombre de la compañia y nombre del producto establecidos al principio.

![vuforia developer portal](https://github.com/gcpmendez/VuforiaArt/blob/master/vuforia11.JPG?raw=true)  

**Último paso:** Construimos la aplicación con build y nos generará el .apk que podremos instalar en el dispositivo Android. Lo instalamos en nuestro dispositivo Android y comprobamos que funcione todo. :grin::grin:

> **Nota:** He visto que la aplicación no funciona con ciertos tipos de dispositivos al instalarla, sale el mensaje "Aplicación no instalada". La solución es establecer las "player Settings" como sigue:
* Default Orientation: landscape Left
* Device Filter: ARMv7
* Install Location: Automatic
* Api Comptatibility Level: .NET 2.0 Subnet
* Versión de android: establecer la de nuestro dispositivo.

> Con esto ya funciona. He subido el APK RealidadAumentadaCoche.apk con la nueva configuración.

## Ayúdame a mejorar este tutorial

Cada **bugs** que encuentres házmelo saber a [gcpmendez@gmail.com](mailto:gcpmendez@gmail.com)

## Enlaces Externos

  [1]: [ETSII ULL](http://www.ull.es/view/centros/etsii/Tercero_7/es), Escuela Técnica Superior de Ingeniería Informática - Graduado en Ingeniería Informática.  
  [2]: [Unity](http://unity3d.com/es/get-unity/download/archive), Archivos de descarga de UNITY.  
  [3]: [SDK de Vuforia para Unity](https://developer.vuforia.com/downloads/sdk), portal para desarrolladores de vuforia.

## Licencia
<center> <a rel="license"  href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a>  <br />Este trabajo tiene una licencia <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>. </center>
