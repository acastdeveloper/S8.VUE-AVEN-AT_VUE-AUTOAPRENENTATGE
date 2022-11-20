# SPRINT 8. VUE AVENÇAT

###### Sumari

- Descripció i Objectius

- Part teòrica
  
  - Curs Vue, part 3
  
  - Curs Vue, part 4
  
  - A practicar

- Part pràctica. S8. Star Wars

---

# DESCRIPCIÓ I OBJECTIUS

És hora de començar a testar la teva aplicació!

És un tema difícil, però és important que puguis assolir els conceptes teòrics d'aquest sprint, ja que, pot preparar-te per saber com actuar davant d'una entrevista laboral!

##### **Objectiu general**

- Aprendre a crear els teus primers tests.

- Saber utilitzar Vuex, centralitzant tota la lògica i dades de l'aplicació.



##### **Objectius específics**

- Saber utilitzar Test Utils, la llibreria oficial de testing de Vue.  

- Fer servir Jest per córrer test en Vue.

- Saber crear un store de Vuex. 

- Crear accions i mutacions de Vuex.

- Implementar getters perquè els components puguin obtenir les dades del state de Vuex.

---

# PART TEÒRICA

## Curs Vue, part 3

En aquest curs aprendràs els conceptes fonamentals d'unit **testing** en Vue.

Les proves unitàries o **unit testing** són una manera de comprovar que un fragment de codi funciona correctament.

És un dels procediments que s'utilitzen per dur a terme dins d'una metodologia àgil de treball, per tant, és totalment necessari perquè, tanmateix, garanteixi la qualitat del codi.



### Vue Test Útils

Abans de començar, està bé que tinguis clar els principals elements del testing:

- **Vue Test Útils** és la llibreria de testing oficial per a Vue.js. Ens dona molta facilitat a l'hora de muntar components, simular esdeveniments d'usuari, renderitzat superficial, modificar l'estat i els props de components i més.

- **Jest** és el motor de tests mantingut (s'utilitza per Facebook). Els avantatges principals de Jest sobre altres frameworks de tests són: per un cantó, la velocitat i, per l'altre, que no és necessari configurar res (o gairebé res) per fer-lo servir. Per tant, permet més adaptabilitat i potencia les funcions.

- **TDD o Test-driven development** és un procés de desenvolupament de programari que segueix un cicle molt curt:

-Es defineixen els requisits del programari.

-Es creen tests per a cobrir aquests requeriments.

-S'implementa el programari per a passar els tests.

A continuació, pots conèixer les diferents modalitats sobre com es realitza un test unitari al teu codi:

[Vue Testing with Vue Test Utils - YouTube](https://www.youtube.com/watch?v=QIDhzBg5eWY)



### Testejar un component amb Jest

A continuació, tens un exemple molt simple sobre com testar a fons el comportament d'un component:

**->[Vue js unit test a Vue component with jest](https://egghead.io/lessons/vue-js-unit-test-a-vue-component-with-jest)**  



### Jest

Convé aprofundir respecte al funcionament de **Jest,** que es caracteritza per actuar amb molta "naturalitat" a l'hora de crear tests.

Visualitza amb detall el següent vídeo  que explica com fer un **Unit test** utilitzant **Jest.**

[Unit Test con Jest - YouTube](https://www.youtube.com/watch?v=mJnAtmTAP-U)



## Curs Vue, part 4 (Vuex)

En aquesta part del curs s'expliquen els conceptes avançats de **Vue** i **Vuex**.

És molt important que sàpigues llegir documentacions de les tecnologies que utilitzes. Per això, després d'aprendre un concepte nou en cada apartat d'aquest curs, et recomanem acudir a la documentació oficial de Vue i repassar aquest concepte.

**->[Documentació oficial de Vue](https://v3.vuejs.org/guide/introduction.html#what-is-vue-js)**

A més la documentació oficial de Vue està molt ben estructurada, amb explicacions molt clares i concises!

Aquí tens també l'enllaç a la documentació de Vuex.

**->[Documentació de Vuex](https://vuex.vuejs.org/#what-is-a-state-management-pattern).**

---

### Introducció a Vuex

Quan treballes amb una llibreria com Vue, la informació dels components es transporta de component pare a component fill a través de "props" i viceversa a través d'emetre un esdeveniment que escoltarà el pare. 

Hi ha algunes vegades que necessites accedir a informació d'un component des d'un altre sense que tinguin la relació de pare i fill. Com l'obtindràs llavors? Tècnicament, es pot fer, però a més de ser complicat acabes amb la lògica de negoci repartida per qualsevol component que segurament es repeteix i que en aplicacions grans és un autèntic caos. 

Aquí és on entra la centralització d'aquesta informació amb eines com Vuex (en Vue) o Redux (en React). No sols pots centralitzar informació, sinó també funcions!

A continuació, tens les instruccions per instal·lar-ho i els primers passos en Vuex:

[#10 Introducción a Vuex (Instalación con CDN) | Curso de Vue.js 😍 Desde Cero - YouTube](https://www.youtube.com/watch?v=-qmLWz6pWnM)

>  **Important**
> 
> Guarda l'exemple d'aquest primer vídeo, ja que continuarem amb ell en els següents apartats d'aquesta part del curs.

Atès que Vuex costa entendre al principi, i el vídeo anterior és massa superficial, et proposem un altre segon vídeo en el qual s'explica més en profunditat Vuex:

[VUEX - Introducción COMPLETA al MANEJO DE ESTADOS con Vue.js - YouTube](https://www.youtube.com/watch?v=zJkPhjjOZ0A)



### State i mapState de Vuex

Ara aprendrem com compartir l'estat de l'store de Vuex de manera elegant "mapeando" el state amb mapSatate.

[#11 mapState con Vuex | Curso de Vue.js 😍 Desde Cero - YouTube](https://www.youtube.com/watch?v=KyLjsiQradM)



### Mutation i mapMutation en Vuex

Amb Vuex no podem arribar a una variable de l'estat des d'un component i manipular-la perquè canviï directament. Ja que, executant aquesta tasca, els components no reaccionarien al canvi i no tindria cap utilitat.

Pel fet que la llibreria segueix un sistema de flux unidireccional, on totes les fases es trobin en un cicle tancat, haurem d'utilitzar un nou concepte conegut com a "mutacions". Les mutacions són aquelles funcions que s'encarreguen de canviar el valor del nostre estat.

[#12 mapMutation y Parámetros en Mutation con Vuex | Curso de Vue.js 😍 Desde Cero - YouTube](https://www.youtube.com/watch?v=eQ_fVRbYIbM)

>  **Important**
> 
> No s'han de gestionar operacions asíncrones des de les mutacions.

**Com gestionem l'asincronia en les meves aplicacions? No podré fer anomenades a servidor o bases de dades en una aplicació de Vue?** Doncs sí, per això van néixer les accions, que veurem en el següent capítol.



### Action y mapAction en Vuex

Les accions funcionen igual que les mutacions. Això sí, no poden mutar l'estat – això ho deleguen a les mutacions – i es permeten totes les operacions asíncrones que necessitem. Per exemple, una crida a API:

[#13 Action y mapAction con Vuex | Curso de Vue.js 😍 Desde Cero - YouTube](https://www.youtube.com/watch?v=qPPxLX0yHfM)



### Getters de Vuex

**Els "Getters" són part de la store Vuex** i s'utilitzen per calcular dades basades ​​en l'estat de l'store.

Bàsicament, són una de les moltes coses que fan que Vue i Vuex siguin excepcionalment potents quan actuen juntes.

> “*Vuex ens permet definir 'getters' en el store. Pot pensar en ells com a 'computed properties' per als ssotres.*”.

 Documentació oficial de Vue

Algunes coses que són genials sobre els getters és que:

- Són fàcilment accessibles dins dels components i les actions de Vuex.

- Emmagatzemen dades en caché i s'actualitzen de manera intel·ligent quan canvia l'estat.

- Poden retornar funcions, de manera que sigui possible passar arguments addicionals per a calcular dades basades ​​en ells.

[GETTERS | VueJS &amp; Vuex | Learning the Basics - YouTube](https://www.youtube.com/watch?v=iw1eajzWQAM)



### Moduls de Vuex

Tal com passa amb la nostra aplicació, quan un **Store** comença a créixer massa pot presentar més dificultats per poder gestionar-ho en un únic fitxer. Com **Vuex** presenta una solució on es gestiona tot l'estat en únic objecte, hem de pensar una forma per a poder **"modularitzar"**, però alhora continuar tenint aquesta estructura en arbre únic.

**Vuex** compta amb una funcionalitat que ens permetrà dividir el nostre arbre de dades en mòduls més específics, els quals comptaran cadascun d'ells amb tot el necessari per gestionar aquestes porcions.

D'aquesta manera segmentarem la nostra aplicació de tal manera que les dades no es barregin.

[VUEX Modules | Aprende a trabajar con módulos en Vue.js [ESPAÑOL] - YouTube](https://www.youtube.com/watch?v=Nzne3qYMl_o)



### Nuxt

**Nuxt.js** és un framework que està basat en Vue.js i escrit en JavaScript.

És totalment modular, de manera que podem començar amb un paquet molt senzill i, segons els nostres requeriments i el nostre projecte vagi creixent, podem instal·lar les llibreries o paquets que necessitem.

**Nuxt.js** ve a solucionar una mica les configuracions, que eren més tedioses, amb Vue.js, ja que fa que aquest procés sigui realment fàcil i molt senzill.

[Nuxt.js - Introduction by Project - YouTube](https://www.youtube.com/watch?v=nteDXuqBfn0)



### Navigation Guards

Imagina que tens un sistema web on qualsevol usuari pot registrar-se i "loguearse". Tenint en compte que la majoria dels sistemes, posseeixen una zona de panell d'administració, a la qual, només els usuaris Administradors poden entrar.

Com programaries això? Fàcil, depenent de quin usuari estigui "loguejat", em fixo que rol o permís té i ho habilito a ingressar al panell o no, això sense importar el framework o llenguatge s'ha de complir.

Ara bé, imagineu-vos en el cas que hagin de bloquejar l'accés a 20 vistes. No es torna molt tediós haver de fer el codi en cadascuna d'elles per a revisar si té permisos o no? Bé, en el cas de **Vue**, aquí es podrien utilitzar els guards (a més de moltes altres funcions que posseeixen):

[Getting Started with Vue.js Navigation Guards to Restrict Access to Routes - YouTube](https://www.youtube.com/watch?v=30XtkPC8nHI)



## A practicar!

Com sempre diem, la millor manera d'acabar d'entendre els conceptes apresos és practicant!

A continuació, tens un tutorial molt complet, en el qual es fa el **setup** del projecte, es creen els components i es maqueten, s'implementen les rutes, l'autenticació, crea les vistes d'administrador amb la seva gestió de rols i molt més.

Veuràs que és una mica llarg, però almenys les 3 primeres hores hauries de poder anar ràpidament, ja que, has estat diverses setmanes amb Vue!

Aquest tutorial et pot servir per a fer protfoli, a més d'aprendre Firebase, servei en el núvol que ens ajuda a crear aplicacions sense haver de saber **Back - end**.

Moltes empreses valoren que sàpigues tecnologies en el núvol com Firebase, Amazon Web Services, Azure...

[6 Hour Vue.js &amp; Firebase Project - FireBlogs - YouTube](https://www.youtube.com/watch?v=ISv22NNL-aE)



**Nota**: Si no tens temps a acabar-ho, pots continuar-ho quan acabis el curs.
