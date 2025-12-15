# PEC3 Manovich Reloaded
## Visionando el futuro con las gafas de Manovich 
### Recurso de aprendizaje de Cultura Digital 

**Autor:** Alfredo Aransay Medina
**Asignatura:** Cultura Digital
**Fecha:** 12 de Diciembre de 2025


## Introducción

Después de desarrollar un caso de **remediación**, en el cual hemos visto como los nuevos medios reestructuran mediante la apropiación, la transformación y la reinterpretación los antiguos medios preexistentes, aplicando la transcodificación para impulsar una evolución en la cultura digital, llegando al punto que nos atañe ahora, que es la **hibridación** de medios.

Según Lev Manovich, **la hibridación es un proceso de remediación que va más allá de la multimedia y es clave en la fusión de los nuevos medios digitales**, donde el software nos brinda la capacidad de manipular y combinar diferentes formatos, ya sea de, texto, imagen, sonido y video, para crear nuevas y coherentes experiencias de software.

Para dilucidar sobre este nuevo termino llamado **hibridación**, vamos a intentar explicar mediante la visión que nos proporcionan la hipotéticas gafas de Manovich, dos breves casos de estudio y como los diferentes medios que los componen, dando lugar a una **remezcla profunda**, todo ello en un único entorno software mediante la integración de técnicas, estructuras de datos, operaciones y formas de interfaz.


---
## 1. Strudel REPL
### 1.1 Breve introducción a Strudel REPL

![Strudel REPL](https://hackaday.com/wp-content/uploads/2025/10/Screenshot-From-2025-10-15-08-47-59.png?w=800)

Strudel REPL es un entorno interactivo de codificación en vivo *(live coding)* para la creación de música, se ejecuta en el navegador web, y se basa en el lenguaje de patrones algorímicos Tidal Cycles, que es un lenguaje específico del dominio incrustado en el lenguaje Haskell pero escrito en JavaScript para ser más accesible, ofreciendo una experiencia visual y sonora única sin necesidad de ser un experto en programación.

Strudel permite a los usuarios escribir código para:
* Crear patrones rítmicos y musicales en tiempo real mediante programación.
* Manipular sonidos (como bombos, cajas, platillos) y ritmos.
* Controlar instrumentos virtuales.
* Secuenciar música de una manera totalmente flexible.

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
Strudel REPL es un claro ejemplo de hibridación de medios que ha evolucionado desde la remediación. En él las notas musicales se escriben mediante la introducción de código y algortimos, que a su vez se transcodifican en instrucciónes entendibles por Strudel para aplicar técnicas de sinstesis y secuenciación de audio a través de los sonidos almacenados en su base de datos, todo ello ejecutado desde el navegador web que actúa como un gran estudio de sonido virtual en el que el usuario es el productor.

Strudel remedia los medios físicos como son las partituras, los instrumentos o las mesas de mezclas, fusionándolos en una **remezcla profunda** mediante la hibridación en un metamedio ordenador, es decir, un navegador web es utilizado como contenedor o DAW (Digital Audio Workstation) y como receptor de las intrucciones aportadas por el usuario a través del *live coding* para crear música en tiempo real.

**Por lo tanto, Strudel REPL no realiza una mera imitación o un simulación de los medios preexsitentes, sino que crea una nueva especie de software que habla un lenguaje propio en el metamedio en el que se ejecuta para generar arte.**

---
## 2. Tribe XR DJ Academy
### 2.1 Breve introducción a Tribe XR Academy

![Tribe XR DJ Academy](https://shared.fastly.steamstatic.com/store_item_assets/steam/apps/2411700/ss_9e3d3ea881d1fdb5e25129035e76606f5b45afdc.1920x1080.jpg?t=1689268338)

Tribe XR es un entorno de realidad virtual o VR inmersivo que simula una cabina DJ, con equipos profesionales como son el Pioneer DJ CDJ-3000 o el mixer DJM-900NXS2, permitiendo a aspirantes a DJ aprender y practicar como si fueran sesiones reales, añadiendo la posibilidad de retransmitir las sesiones en tiempo real. Tribe XR también funciona como una academia online ofreciendo tutoriales y lecciones en vivo.

### 2.2 Mi visión de 'Tribe XR DJ Academy' a través de las gafas de Lev Manovich
Tribe XR es una plataforma que redemia, imita y simula perfectamente los equipos profesionales de DJ a través de una interfaz VR inmersiva, permitiendo al usuario actuar como si estuviera en una sesión real con equipo real. Con Tribe XR se lleva la simulación a un estado híbrido que permite al usuario no solo practicar, sino también aprender como si estuviera en una academia, ya que ofrece una plataforma de aprendizaje con videotutoriales y *workshops*. A su vez permite al usuario realizar sesiones en directo, tanto en solitario como colaborativas funcionando como una red social, es decir un objeto de retransmisión mediático como performance visual para una comunidad global.

Tribe XR funciona como una remezcla profunda fusionando tres medios:
1. **El medio hardware**. Se simula el equipo de un DJ, los platos y la mesa de mezclas son manipulados en tiempo real mediante la acción táctil gracias al VR inmersivo.
2. **El medio datos**. Se integra una base de datos con los principales sistemas de música, como es por ejemplo SounCloud, sustituyendo los característicos vinilos físicos por una libreria casi infinita de temas.
3. **El medio físico**. Este se fusiona a través de un equipo VR y un motor de videojuegos (Unreal Engine) permitiendo al usuario interactuar con todo el sistema, ofreciendo una interfaz dinámica en 3D que simula una actuación real que se ofrece en *streaming* en tiempo real.

**Entonces qué ofrece Tribe XR DJ Academy, más que simular una actuación real creo que ofrece una experiencia muy cercana a la realidad, puesto que permite al usuario interarctuar con el nuevo metamedio 'cabina de DJ virtual', ofreciendo actuaciones reales o personas reales.**

---
### Referencias y Bibliografía

* Manovich, Lev. (2013). **El Software toma el mando**. Barcelona: Editorial UOC. 
* Strudel REPL. https://strudel.cc/
* Tribe XR DJ Academy. https://www.tribexr.com/
* Future Music Digital Magazine. https://www.futuremusic-es.com/pioneer-dj-en-vr-usa-una-cabina-virtual-de-tribe-xr-con-cdj-3000-y-djm-900nsx2-para-retransmitir-tus-sets-en-directo/
* HACKADAY. https://hackaday.com/2025/10/16/live-coding-techno-with-strudel/

### Imágenes
* HACKADAY - https://hackaday.com/2025/10/16/live-coding-techno-with-strudel/
* TRIBE XR - https://store.steampowered.com/app/2411700/Tribe_XR__Lifetime_Subscription/?l=spanish

----
Licencia: Material Creative Commons desarrollado bajo licencia CC BY-SA 4.0.
