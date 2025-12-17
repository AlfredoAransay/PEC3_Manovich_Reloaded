# PEC3 Manovich Reloaded
## Visionando el futuro con las gafas de Manovich 

**Autor:** Alfredo Aransay Medina

**Asignatura:** Cultura Digital

**Fecha:** 17 de Diciembre de 2025


## **0. Introducción**

Después de desarrollar un caso de **remediación**, en el cual hemos visto como los nuevos medios reestructuran mediante la apropiación, la transformación y la reinterpretación los antiguos medios preexistentes, aplicando la transcodificación para impulsar una evolución en la cultura digital, llegando al punto que nos atañe ahora, que es la **hibridación** de medios.

Según Lev Manovich, **la hibridación es un proceso de remediación que va más allá de la multimedia y es clave en la fusión de los nuevos medios digitales**, donde el software nos brinda la capacidad de manipular y combinar diferentes formatos, ya sea de, texto, imagen, sonido y video, para crear nuevas y coherentes experiencias de software.

Para dilucidar sobre este nuevo termino llamado **hibridación**, vamos a intentar explicar mediante la visión que nos proporcionan las hipotéticas gafas de Manovich, dos breves casos de estudio y como los diferentes medios que los componen para dar lugar a una **remezcla profunda**, todo ello en un único entorno software mediante la integración de técnicas, estructuras de datos, operaciones y formas de interfaz.


---
## **1. Strudel REPL**
### 1.1 Breve introducción a Strudel REPL

![Strudel REPL](https://hackaday.com/wp-content/uploads/2025/10/Screenshot-From-2025-10-15-08-47-59.png?w=800)

**Strudel REPL es un entorno interactivo de codificación en vivo *(live coding)* diseñado para la creación de música ejecutado en el navegador web**. Strudel es una implementación en Javascript del lenguaje de patrones algorítmicos Tidal Cycles *(originalmente escrito en Haskell)*. Ha sido diseñado para ser accesible y fácil de usar ofreciendo una experiencia visual y sonora única sin necesidad de ser un experto en programación. 

>#### *Strudel ofrece un experiencia visual y sonora única sin necesidad de ser un experto en programación, permitiendo al usuario escribir expresivamente piezas de música dinámicas.*

### Strudel permite al usuario:
* Crear patrones rítmicos y musicales en tiempo real mediante programación.
* Manipular sonidos (como bombos, cajas, platillos) y ritmos.
* Controlar instrumentos virtuales.
* Secuenciar música de una manera totalmente flexible.
* Realizar música en vivo.


### Código de un patrón en Strudel
```haskell
// "Festival of fingers 3"
// @license CC BY-NC-SA 4.0 https://creativecommons.org/licenses/by-nc-sa/4.0/
// @by Felix Roos

setcps(1)

n("[-7*3],0,2,6,[8 7]")
  .echoWith(
    4, // echo 4 times
    1/4, // 1/4s between echos
    (x,i)=>x
      .add(n(i*7)) // add octaves
      .gain(1/(i+1)) // reduce gain
      .clip(1/(i+1))
    )
  .mul(gain(perlin.range(.5,.9).slow(8)))
  .stack(n("[22 25]*3")
         .clip(sine.range(.5,2).slow(8))
         .gain(sine.range(.4,.8).slow(5))
         .echo(4,1/12,.5))
  .scale("<D:dorian G:mixolydian C:dorian F:mixolydian>")
  .slow(2).piano()
//.pianoroll({maxMidi:160})
```
***Festival of fingers 3** by Felix Roos*

### 1.2 Mi visión de 'Strudel REPL' a través de las gafas de Lev Manovich
**Strudel REPL es un claro ejemplo de hibridación de medios que ha evolucionado desde la remediación**. En él las notas musicales se escriben mediante la introducción de código y algoritmos, que a su vez se transcodifican en instrucciones entendibles por Strudel para aplicar técnicas de sinstesis y secuenciación de audio a través de los sonidos almacenados en su base de datos, todo ello ejecutado desde el navegador web que actúa como un gran estudio de sonido virtual en el que el usuario es el productor.

Strudel remedia los medios físicos como son las partituras, los instrumentos (sintetizadores, cajas de ritmos, ...) o las mesas de mezclas, fusionándolos en una **remezcla profunda** a través del metamedio ordenador. Es decir:
1. El navegador web se utiliza como contenedor hardware sustituyendo al estudio de sonido y actuando como un DAW (Digital Audio Workstation).
2. El *live coding* actúa como las manos del ser humano manipulando el hardware virtual.
3. El código se transcodifica para comunicarse con Strudel y así manipular, secuenciar y crear música en tiempo real.
4. Los algoritmos sonorizan patrones rítmicos y melódicos simulando un pentagrama, aportando un enfoque dinámico a la composición.
5. Ofrece una retroalimentación visual mostrando qué partes de los patrones están sonando, ayudando a aprender y experimentar de una manera fluida y flexible.

#### **Strudel REPL no realiza una mera imitación o un simulación de los medios preexsitentes, sino que crea una nueva especie de software que habla un lenguaje propio dentro del metamedio en el que se ejecuta para generar arte. Strudel es una forma divertida de explorar la creación de música algorítmica y patrones sonoros en vivo de manera interactiva, directamente desde el navegador sin la necesidad de instalaciones de software complejas.**

---
## **2. Tribe XR DJ Academy**
### 2.1 Breve introducción a Tribe XR Academy

![Tribe XR DJ Academy](https://shared.fastly.steamstatic.com/store_item_assets/steam/apps/2411700/ss_9e3d3ea881d1fdb5e25129035e76606f5b45afdc.1920x1080.jpg?t=1689268338)

**Tribe XR es un entorno de realidad virtual o VR inmersivo mixto diseñado como un simulador de cabina DJ profesional**, con costosos equipos profesionales como son el Pioneer DJ CDJ-3000 o el mixer DJM-900NXS2, permitiendo a aspirantes a DJ aprender y practicar en una simulación realista, añadiendo la posibilidad de retransmitir las sesiones en vivo. **Tribe XR funciona como una academia musical online interactiva** ofreciendo tutoriales y lecciones en vivo con mentores y talleres para todos los niveles, desde los fundamentos para principiantes hasta técnicas más avanzadas para profesionales.

>#### *Tribe XR ofrece un metaverso virtual democratizando el acceso al DJing tanto a principiantes como a profesionales, siendo una herramienta innovadora para el aprendizaje y la performance musical.*

### 2.2 Mi visión de 'Tribe XR DJ Academy' a través de las gafas de Lev Manovich
**Tribe XR es una plataforma que remedia, imita y simula perfectamente los equipos profesionales de DJ a través de una interfaz VR inmersiva**, permitiendo al usuario actuar como si estuviera en una sesión real con equipo real. Con Tribe XR se lleva la simulación a un estado híbrido permitiendo al usuario no solo practicar, sino también aprender como si estuviera en una academia, ya que ofrece una plataforma de aprendizaje con videotutoriales y *workshops* en vivo. A su vez permite al usuario realizar sesiones en directo en el metaverso, tanto en solitario como colaborativas funcionando como una red social, es decir, se transforma en un objeto de retransmisión mediático como performance visual para una comunidad global.

**Tribe XR funciona como una remezcla profunda fusionando tres medios:**
1. **El medio hardware**. Se imita mediante una representación fiel el equipo hardware de un DJ, los platos y la mesa de mezclas, los cuales son manipulados en tiempo real a través de la acción táctil gracias al VR inmersivo.
2. **El medio datos**. Se integra con algunos de los principales sistemas de música en streaming, como pueden ser por ejemplo SounCloud o Beatport, sustituyendo los característicos vinilos físicos por una librería casi infinita de temas y sonidos. Además permite importar tus propios archivos de audio para ofrecer sesiones más personales.
3. **El medio físico**. Este se fusiona a través de un equipo VR y un motor de videojuegos (Unreal Engine) permitiendo al usuario interactuar con todo el sistema, ofreciendo una interfaz dinámica en 3D que simula una actuación en vivo retransmitida de manera global, a través de las principales redes de *streaming* como pueden ser Twitch, YouTube o Facebook.

#### **Tribe XR DJ Academy ofrece una experiencia inmersiva única muy cercana a la realidad, una cabina de DJ virtual profesional, permitiendo al principiante y al profesional interarctuar con el nuevo metamedio de sesiones virtuales, ofreciendo actuaciones reales a personas reales dentro de un metaverso global.**

---
## **3. Conclusiones**
> #### Gracias al análisis y a la visión de Lev Manovich sobre los procesos de hibridación ahora somos capaces de ver como el software avanza y toma el mando de todo lo que nos rodea, ya no se trata de sustituir los antiguos medios por nuevas capas de software que los mejoren y remedien, sino que se ha de ir más allá remezclando los nuevos medios en nuevas especies de software más complejas que proporcionen nuevos lenguajes y experiencias de cultura, arte y tecnología.

---
### Referencias y Bibliografía

* Manovich, Lev. (2013). **El Software toma el mando**. Barcelona: Editorial UOC. 
* *Strudel REPL*. Disponible en: https://strudel.cc/ (Consultado: 08 de Diciembre de 2025).
* *Tribe XR DJ Academy (2025)*. Disponible en: https://www.tribexr.com/ (Consultado: 08 de Diciembre de 2025).
* *Future Music Digital Magazine (2021)*. Disponible en: https://www.futuremusic-es.com/pioneer-dj-en-vr-usa-una-cabina-virtual-de-tribe-xr-con-cdj-3000-y-djm-900nsx2-para-retransmitir-tus-sets-en-directo/ (Consultado: 14 de Diciembre de 2025).
* *HACKADAY (2025)*. Disponible en: https://hackaday.com/2025/10/16/live-coding-techno-with-strudel/ (Consultado: 14 de Diciembre de 2025).

### Imágenes
* HACKADAY. https://hackaday.com/2025/10/16/live-coding-techno-with-strudel/
* TRIBE XR. https://store.steampowered.com/app/2411700/Tribe_XR__Lifetime_Subscription/?l=spanish

----
Licencia: Material Creative Commons desarrollado bajo licencia CC BY-SA 4.0.
