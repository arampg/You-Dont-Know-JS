# You Don't Know JS Yet: Get Started - 2nd Edition
# Chapter 1: What *Is* JavaScript?

No sabes JS, aún. Ni yo, completamente al menos. Nadie de nosotros. Pero todos podemos empezar a conocerlo mejor.

En este primer capítulo, de este primer libro de la serie *You Don't Know JS Yet* (YDKJSY), emplearemos un tiempo para construir una base sobre la que avanzar. Necesitamos empezar cubriendo una variedad de detalles importantes dentro de este contexto, despejando algunos mitos y confusiones sobre lo que el lenguaje realmente es... ¡y lo que no!.

Esto nos ayudará a obtener un valioso conocimiento acerca de la identidad y el proceso de cómo JS se organiza y se mantiene; todos los desarrolladores JS deberían entenderlo. Si deseas conocer JS, así es como puedes comenzar a dar los primeros pasos en este viaje.

## About This Book

Enfatizo la palabra viaje porque saber JS no es el destino, es una dirección. Da igual cuanto tiempo pases con el lenguaje, siempre encontrarás algo nuevo que aprender y entender mejor. No mires este libro como algo sobre lo que pasar precipitadamente para alcanzar un objetivo rápido. Paciencia y perseverancia serán las mejores compañeras en tus primeros pasos

Como continuación a este capítulo de fondo, el resto del libro se va disponiendo como un mapa de alto nivel de lo que irás encontrando a medida que indagas y estudias JS con los libros YDKJSY.

Concretamente, el Capítulo 4 identifica 3 pilares principales sobre los que se organiza el lenguaje JS: contexto/clausuras, prototipos/objetos, y tipos/coerción. JS es un lenguaje amplio y moderno, con muchas herramientas y competencias. Pero todo JS se basa en estos tres pilares fundamentales.

Ten presente que aunque este libro se titule "Get Started," **no pretende ser un libro introductorio/para principiante**. La tarea principal de este libro es prepararte para estudiar JS a fondo a lo largo del resto de la serie; está escrito asumiendo que ya llevas varios meses familiarizándote con JS, antes de abordar YDKJSY. Así que para extraer el máximo de *Get Started*, asegúrate de emplear suficiente tiempo programando en JS para reforzar tu experiencia.

Aunque hayas programado durante mucho tiempo en JS, no deberías pasar por alto este libro, ni ojearlo de manera rápida. Tómate tu tiempo para procesar todo el material que hay en él. **Un buen comienzo siempre depende de un primer paso firme.**

## What's With That Name?

El nombre Javascript es probablemente el nombre más incomprendido y malinterpretado de un lenguaje de programación.

Tiene algo que ver con Java? Es solo la parte de secuencia de comandos de Java? Es solo para escribir secuencias de comandos y no programas reales?

En realidad, el nombre JavaScript es el resultado un malabarismo de marketing. Cuando Brendan Eich concibió el lenguaje, le asignó el nombre en clave Mocha. Internamente en Netscape, se usó la marca LiveScript. Pero cuando llegó el momento de ponerle un nombre público, "JavaScript" ganó en la votación.


Por qué? Porque este lenguaje fue diseñado inicialmente para atraer un público de programadores de Java mayoritariamente, y porque la palabra "script" era popular y se usaba con frecuencia para hacer referencua a programas ligeros. Estos "scripts" ligeros serían los primeros en incrustarse en páginas de esta nueva cosa llamada ¡web!

En otras palabras, JavaScript era un ardid de marketing para intentar posicionar este lenguaje como una alternativa aceptable a escribir en un más conocido y pesado Java de aquellos entonces. Podría haberse llamado perfectamente "WebJava".

Hay algunas semejanzas superficiales entre código JavaScript y código Java. Estas similitudes no provienen de un desarrollo conjunto, precisamente, sino que ambos lenguajes se fijan como objetivos desarrolladores supuestas expectativas de sintaxis de C (y por lo tanto de C++).

Por ejemplo, usamos `{` para empezar un bloque de código y `}` para acabar este bloque, como lo hace C/C++ y Java. También usamos `;` para puntuar el final de una declaración.

De alguna forma, relaciones legales los unen incluso más allá de la sintaxis. Oracle (a través de Sun), la compañía que todavía posee y mantiene Java, también posee la marca registrada oficial para el nombre "JavaScript" (a través de Nestcape). Esta marca registrada no se ejecuta casi nunca, y sería muy difícil que se cumpliera hoy en día.

Por este motivo, se ha sugerido que se use JS en lugar de JavaScript. Es una abreviación muy común, además de un buen candidato para el nombre de un lenguaje oficia. De hecho, estos libros usan JS casi exclusivamente para hacer referencia al lenguaje.

Como distanciamiento de la marca registrada en propiedad de Oracle, el nombre oficial del lenguaje especificado por TC39 y formalizado por los estándares ECMA, es **ECMAScript**. Y de hecho, desde 2016, al nombre oficial del lenguaje se le agrega al final la revisión del año; mientras se escriben estas líneas, es ECMAScript 2019, o también abreviado ES2019.

En otras palabras, el JavaScript/JS que se ejecuta en tu navegador o en Node.js, es *una* implementación del estándar ES2019.

| NOTA: |
| :--- |
| No uses términos como "JS6" o "ES8" para referirte al lenguaje. Algunos lo hacen, pero esos términos solo sirven para perpetuar la confusión. "ES20xx" o simplemente "JS" es con lo que deberías quedarte. |


Tanto si lo llamas JavaScript, JS, ECMAScript, o ES2019, ¡no es una variante de JAVA, claramente!

> "Java is to JavaScript as ham is to hamster." --Jeremy Keith, 2009
> "Java es para JavaScript, lo que pan es a pantera " --Anonymous, 2020

## Language Specification

He mencionado TC39, el comité técnico directivo que gestiona JS. Su principal tarea es gestionar la especificación oficial para el lenguaje. Se reúnen habitualmente para votar cambios propuestos, los cuales entregan a ECMA, la organización de estándares.

La sintaxis y el comportamiento de JS se definen en la especificación de ES.

ES2019 ha resultado ser la 10ª especificación/revisión desde la aparición de JS en 1995, por lo tanto en la URL de la especificación oficial, alojada por ECMA, encontrarás "10.0":

https://www.ecma-international.org/ecma-262/10.0/

El comité TC39 está compuesto por entre 50 y 100 personas de un amplio sector de compañías dedicadas a la web, como fabricantes de navegadores (Mozilla, Google, Apple) y fabricantes de dispositivos (Samsung, etc). Todos los miembros del comité son voluntarios, aunque muchos de ellos son empleados de estas compañías y pueden percibir parte de su sueldo como contribución al comité.

TC39 se reúne generalmente cada dos meses, normalmente durante 3 días, para revisar el trabajo realizado por los miembros desde el último encuentro, y votar propuestas. El lugar de las reuniones va rotando entre las compañías miembro que desean hospedarlas.

Todas las propuestas del TC39 transcurren por un proceso de cinco etapas (¡y como somos desarrolladores, tienen base 0!), de la Etapa 0 a la Etapa 4. Puedes leer más sobre el proceso de las etapas aquí: https://tc39.es/process-document/

Etapa 0 significa, sin tapujos, que alguien del TC39 piensa que es una idea válida y piensa abogar por ella y trabajar en ella. Esto significa que muchas de las ideas que personas que no son miembros del TC39 proponen, a través de medios informales como social media, o posts en blogs, son realmente "Previo a la Etapa 0". Necesitas convencer a algún miembro del TC39 que abogue por ella para que sea considerada "Etapa 0" oficialmente.

Una vez que la propuesta alcanza el estado "Etapa 4", es apta para que sea incluida en la próxima revisión anual del lenguaje. Puede llevar desde varios meses hasta unos cuantos años para que una propuesta consiga completar el proceso a través de todas las etapas.

Todas las propuestas se gestionan abiertamente, en el repositorio de Github de TC39: https://github.com/tc39/proposals

Cualquiera, ya pertenezaca o no al TC39, es bienvenido en los debates públicos y los procesos para trabajar en las propuestas. Sin embargo, únicamente los miembros del TC39 puede asistir a las reuniones y votar las propuestas y cambios. Por lo que en la práctica, la voz de un miembro del TC39 es decisiva a la hora de decidir el camino de JS.

Contrario a lo que dicen algunos mitos consolidados y que de manera frustrante parecen permanecer en el tiempo, *no* existe múltiples versiones por ahí fuera de JS. Solamente hay **un JS**, el estándar oficial mantenido por TC39 y ECMA.

A principios de los años 2000, cuando Microsoft mantenía una versión bifurcada (forked) y reverse-engineered (no del todo compatible) de JS llamada "JScript", se podía decir que había varias versiones de JS. Pero esos días quedaron atrás. Es obsoleto e impreciso hacer tales afirmaciones sobre JS hoy en día.

Todos los navegadores principales y fabricantes de dispositivos se han comprometido a mantener sus implementaciones de JS de acuerdo a esta especificación central. Por supuesto, los motores implementan características en tiempos distintos. Pero nunca debiera ser el caso en el que el motor v8 (el motor JS de Chrome) implementa una característica de forma diferente, o de manera incompatible a como lo hace el motor SpiderMonkey (motor Js de Mozilla).

Eso significa que puedes aprender **un JS** y confiar en ese mismo JS en cualquier sitio.

### The Web Rules Everything About (JS)

Mientras que una diversidad de entornos que ejecutan JS se expanden continuamente (desde navegadores, a servidores -Node.js-, a robots, a bombillas, a...). el entorno que realmente gobierna JS es la web. En otras palabras, la manera de implementar JS para navegadores web es, en la práctica totalidad, la única realidad que importa.


Para la mayor parte, el JS definido en la especificación y el JS que se ejecuta en motores basados en navegadores es el mismo. Pero hay algunas diferencias que deben ser consideradas.

A veces la especificación dicta algún nuevo o mejorado comportamiento, pero no acaba de coincidir con el comportamiento de un motor JS para navegador. Esta disparidad es histórica: los motores JS han seguido manteniendo durante más de 20 años algunos casos complejos sobre los que descansa el contenido web, y rechazan adaptarse al nuevo cambio para evitar romper el contenido.

En estos casos, a menudo TC39 se retracta y simplemente escoge ajustarse a la realidad de la web. Por ejemplo, TC39 acordó añadir el método `contains(..)` para Arrays, pero se descubrió que existía un conflicto con un viejo framework JS que aún se usa en algunas webs, y por eso lo cambiaron a un nombre con el que no hubiera conflicto `includes(..)`. Lo mismo ocurrió con una *crisis comunitaria* en JS, trágico-cómica, apodada como "smooshgate", donde el nombre que se había programadao era `flatten(..)` pero al final quedó como  `flat(..)`.

En alguna ocasión, el TC39 ha decido mantenerse firme aunque sea improbable que los motores JS para navegadores alguna vez se cumplan la especificación en este punto. 

¿La solución? Apéndice B, "Características adicionales ECMAScript para navegadores Web".[^specApB] La especificación JS incluye este apéndice para detallar cualquier disparidad entre la especificación JS y la realidad de JS en la web. En otras palabras, son excepciones que se permiten *solo* para el JS en la web; otros entornos JS se deben ajustar a la letra de la ley.

La Sección B.1 y B.2 cubre "añadidos" de JS (sintaxis y APIs) que el JS para web incluye, de nuevo por razones históricas, pero que TC39 no prevé incluir formalmente en el core de JS. Por ejemplo prefijos `0` en literales octal, las utilidades globales `escape(..)` / `unescape(..)`, String "helpers" como `anchor(..)` y `blink()`, el método de la expresión regular `compile(..)`.

La Sección B3 incluye algunos conflictos donde el código de puede ejecutar en entornos JS tanto web, como no web, pero el comportamiento *podría* ser visiblemente diferente, obteniendo distintos resultados. La mayoría de los cambios listados incluyen situaciones que se etiquetan como errores tempranos cuando el código se ejecuta en modo estrico.

Apéndice B *gotchas* no se encuentran a menudo, pero es una buena idea evitar estas formaciones para asegurarte que continuará funcionando en un futuro. Siempre que sea posible, sigue la especificación de JS y no dependas de comportamientos que solo se manifiestan de determinada manera en ciertos entornos de motores JS.

### Not All (Web) JS...

Este código es un programa JS?

```js
alert("Hello, JS!");
```

Según cómo lo mires. La función `alert(..)` mostrada aquí no está incluida en la especificación Js, pero *está* en todos los entornos JS. Aun así, no la encontrarás en el Apéndice B. Pero... ¿entonces?

Varios entornos JS (como motores de navegadores JS, Node.js, etc.) añaden APIs dentro del contexto global de tus programas JS que dan capacidades específicas del entorno, como ser capaz de mostrar una caja del estilo *alert* en el navegador del usuario.

De hecho, una amplia variedad de APIs del estilo JS, como `fetch(..)`, `getCurrentLocation(..)`, y `getUserMedia(..)`, son todo web APIs que parecen JS. En Node.js podemos acceder a cientos de métodos API desde varios módulos integrados, como `fs.write(..)`.

Otro ejemplo muy común es `console.log(..)`... ¡y el resto de métodos `console.*`! Estos no están especificados en JS, pero debido a su uso universal están definidos por prácticamente todos los entornos JS, de acuerdo a un vasto consenso.

Entonces `alert(..)` y `console.log(..)` no están definidos por JS. Pero parecen *JS*. Son funciones y métodos de objeto y obedecen a la sintaxis de JS. Los comportamientos que hay detrás suyo están controlados por el entorno que ejecuta el motor JS, pero en la práctica tienen que atenerse a lo que diga JS para poder jugar en su campo.


La mayoría de las quejas de diferencias entre navegadores de las que se queja la gente "JS es muy incoherente" son debido a diferencias en cómo esos entornos se comportan, no en cómo el propio JS actúa.

Por tanto una llamada a `alert(..)` *es* JS, pero `alert` en sí es tan solo un invitado, no parte de la especificación oficial de JS.

### It's Not Always JS

En una primera instancia, usar la consola/REPL (Read-Evaluate-Print-Loop) en las Herramientas para Desarollador de tu navegador (o Node), puede parecer como un entorno JS. Pero en realidad, no lo es.

Las Herramientas para Desarrollador son... herramientas para desarrolladores. Su cometido principal es hacer la vida más fácil a los desarrolladores. Priorizan la DX (Experiencia de Desarrollador). Reflejar de manera precisa y exclusiva todos los matices del comportamiento JS del strict-spec *no* es el objetivo de tales herramientas. De por sí, hay algunas peculiaridades que podrían actuar como "gotchas" si piensas que la consola funciona como un entorno *puro* JS.

¡Que esto sea así es bueno! ¡Me alegro de que las Herramientas para Desarrollador hagan la vida más fácil a los desarrolladores! Me alegra tener encantos de UX como autocompletar variables/propiedades, etc. Tan solo me gustaría señalas que no podemos, ni debemos esperar que estas herramientas *siempre* se comporten como lo haría un prograram en JS, porque no es el propósito de estas herramientas.

Como el comportamiento de estas herramientas varía entre navegadores, y como va cambiando (a veces bastante a menudo), no voy a "harcodear" ningún detalle específico en este texto, y evitar así que quede desactualizado rápidamente.

Pero voy a indicar algunos ejemplos de particularidades que se han dado en algunas ocasiones en diferentes entornos de consolas JS, como argumento de que no se debe asumir comportamiento JS nativo mientras se usan:

* Si una declaración `var` o `function` en el nivel más alto del "contexto global" de la consola crea en realidad una variable global real (y duplicada en la propiedad `window`, y viceversa).

* Lo que ocurre con múltiples declaraciones `let` y `const` en el nivel más alto del "contexto global".

* Si `"use strict";` en una entrada de una línea (presionando `<enter>` después) habilita modo estricto para el resto de sesión en la consola, de la misma forma en que lo haría en la primera línea de un archivo .js, y si puedes usar `"use strict";` más allá de la primera línea y habilitar de igual forma el modo estricto para el resto de sesión.

* Cómo actúa la asignación por defecto de `this` en modo no estricto para las llamadas de funciones, y si el "objecto global" usado contendrá las variables globales esperadas.

* Cómo se comporta el hoisting (Libro 2, *Contexto y Clausuras*) en entradas de múltiples líneas. 

* ... muchas otras

La consola del desarrollador no pretende ser un compilador JS que gestiona el código que introduces exactamente del mismo modo que un motor JS gestiona un archivo .js. Trata de facilitarte el hecho de que introduzcas unas líneas y veas los resultados inmediatamente. Son casos de uso completamente diferente, y como tales, no tiene sentido esperar que puede manejar ambos de la misma forma.

No creas que la consola de desarrollador reproduce fielmente el comportamiento de las semánticas de JS; para ello, lee la especificación. Piensa en la consola como un entorno JS *amigable*. En este sentido te será útil.

## Many Faces

The term "paradigm" in programming language context refers to a broad (almost universal) mindset and approach to structuring code. Within a paradigm, there are myriad variations of style and form that distinguish programs, including countless different libraries and frameworks that leave their unique signature on any given code.

But no matter what a program's individual style may be, the big picture divisions around paradigms are almost always evident at first glance of any program.

Typical paradigm-level code categories include procedural, object-oriented (OO/classes), and functional (FP):

* Procedural style organizes code in a top-down, linear progression through a pre-determined set of operations, usually collected together in related units called procedures.

* OO style organizes code by collecting logic and data together into units called classes.

* FP style organizes code into functions (pure computations as opposed to procedures), and the adaptations of those functions as values.

Paradigms are neither right nor wrong. They're orientations that guide and mold how programmers approach problems and solutions, how they structure and maintain their code.

Some languages are heavily slanted toward one paradigm—C is procedural, Java/C++ are almost entirely class oriented, and Haskell is FP through and through.

But many languages also support code patterns that can come from, and even mix and match from, different paradigms. So called "multi-paradigm languages" offer ultimate flexibility. In some cases, a single program can even have two or more expressions of these paradigms sitting side by side.

JavaScript is most definitely a multi-paradigm language. You can write procedural, class-oriented, or FP-style code, and you can make those decisions on a line-by-line basis instead of being forced into an all-or-nothing choice.

## Backwards & Forwards

One of the most foundational principles that guides JavaScript is preservation of *backwards compatibility*. Many are confused by the implications of this term, and often confuse it with a related but different term: *forwards compatibility*.

Let's set the record straight.

Backwards compatibility means that once something is accepted as valid JS, there will not be a future change to the language that causes that code to become invalid JS. Code written in 1995—however primitive or limited it may have been!—should still work today. As TC39 members often proclaim, "we don't break the web!"

The idea is that JS developers can write code with confidence that their code won't stop working unpredictably because a browser update is released. This makes the decision to choose JS for a program a more wise and safe investment, for years into the future.

That "guarantee" is no small thing. Maintaining backwards compatibility, stretched out across almost 25 years of the language's history, creates an enormous burden and a whole slew of unique challenges. You'd be hard pressed to find many other examples in computing of such a commitment to backwards compatibility.

The costs of sticking to this principle should not be casually dismissed. It necessarily creates a very high bar to including changing or extending the language; any decision becomes effectively permanent, mistakes and all. Once it's in JS, it can't be taken out because it might break programs, even if we'd really, really like to remove it!

There are some small exceptions to this rule. JS has had some backwards-incompatible changes, but TC39 is extremely cautious in doing so. They study existing code on the web (via browser data gathering) to estimate the impact of such breakage, and browsers ultimately decide and vote on whether they're willing to take the heat from users for a very small-scale breakage weighed against the benefits of fixing or improving some aspect of the language for many more sites (and users).

These kinds of changes are rare, and are almost always in corner cases of usage that are unlikely to be observably breaking in many sites.

Compare *backwards compatibility* to its counterpart, *forwards compatibility*. Being forwards-compatible means that including a new addition to the language in a program would not cause that program to break if it were run in an older JS engine. **JS is not forwards-compatible**, despite many wishing such, and even incorrectly believing the myth that it is.

HTML and CSS, by contrast, are forwards-compatible but not backwards-compatible. If you dug up some HTML or CSS written back in 1995, it's entirely possible it would not work (or work the same) today. But, if you use a new feature from 2019 in a browser from 2010, the page isn't "broken" -- the unrecognized CSS/HTML is skipped over, while the rest of the CSS/HTML would be processed accordingly.

It may seem desirable for forwards-compatibility to be included in programming language design, but it's generally impractical to do so. Markup (HTML) or styling (CSS) are declarative in nature, so it's much easier to "skip over" unrecognized declarations with minimal impact to other recognized declarations.

But chaos and non-determinism would ensue if a programming language engine selectively skipped statements (or even expressions!) that it didn't understand, as it's impossible to ensure that a subsequent part of the program wasn't expecting the skipped-over part to have been processed.

Though JS isn't, and can't be, forwards-compatible, it's critical to recognize JS's backwards compatibility, including the enduring benefits to the web and the constraints and difficulties it places on JS as a result.

### Jumping the Gaps

Since JS is not forwards-compatible, it means that there is always the potential for a gap between code that you can write that's valid JS, and the oldest engine that your site or application needs to support. If you run a program that uses an ES2019 feature in an engine from 2016, you're very likely to see the program break and crash.

If the feature is a new syntax, the program will in general completely fail to compile and run, usually throwing a syntax error. If the feature is an API (such as ES6's `Object.is(..)`), the program may run up to a point but then throw a runtime exception and stop once it encounters the reference to the unknown API.

Does this mean JS developers should always lag behind the pace of progress, using only code that is on the trailing edge of the oldest JS engine environments they need to support? No!

But it does mean that JS developers need to take special care to address this gap.

For new and incompatible syntax, the solution is transpiling. Transpiling is a contrived and community-invented term to describe using a tool to convert the source code of a program from one form to another (but still as textual source code). Typically, forwards-compatibility problems related to syntax are solved by using a transpiler (the most common one being Babel (https://babeljs.io)) to convert from that newer JS syntax version to an equivalent older syntax.

For example, a developer may write a snippet of code like:

```js
if (something) {
    let x = 3;
    console.log(x);
}
else {
    let x = 4;
    console.log(x);
}
```

This is how the code would look in the source code tree for that application. But when producing the file(s) to deploy to the public website, the Babel transpiler might convert that code to look like this:

```js
var x$0, x$1;
if (something) {
    x$0 = 3;
    console.log(x$0);
}
else {
    x$1 = 4;
    console.log(x$1);
}
```

The original snippet relied on `let` to create block-scoped `x` variables in both the `if` and `else` clauses which did not interfere with each other. An equivalent program (with minimal re-working) that Babel can produce just chooses to name two different variables with unique names, producing the same non-interference outcome.

| NOTE: |
| :--- |
| The `let` keyword was added in ES6 (in 2015). The preceding example of transpiling would only need to apply if an application needed to run in a pre-ES6 supporting JS environment. The example here is just for simplicity of illustration. When ES6 was new, the need for such a transpilation was quite prevalent, but in 2020 it's much less common to need to support pre-ES6 environments. The "target" used for transpiliation is thus a sliding window that shifts upward only as decisions are made for a site/application to stop supporting some old browser/engine. |

You may wonder: why go to the trouble of using a tool to convert from a newer syntax version to an older one? Couldn't we just write the two variables and skip using the `let` keyword? The reason is, it's strongly recommended that developers use the latest version of JS so that their code is clean and communicates its ideas most effectively.

Developers should focus on writing the clean, new syntax forms, and let the tools take care of producing a forwards-compatible version of that code that is suitable to deploy and run on the oldest-supported JS engine environments.

### Filling the Gaps

If the forwards-compatibility issue is not related to new syntax, but rather to a missing API method that was only recently added, the most common solution is to provide a definition for that missing API method that stands in and acts as if the older environment had already had it natively defined. This pattern is called a polyfill (aka "shim").

Consider this code:

```js
// getSomeRecords() returns us a promise for some
// data it will fetch
var pr = getSomeRecords();

// show the UI spinner while we get the data
startSpinner();

pr
.then(renderRecords)   // render if successful
.catch(showError)      // show an error if not
.finally(hideSpinner)  // always hide the spinner
```

This code uses an ES2019 feature, the `finally(..)` method on the promise prototype. If this code were used in a pre-ES2019 environment, the `finally(..)` method would not exist, and an error would occur.

A polyfill for `finally(..)` in pre-ES2019 environments could look like this:

```js
if (!Promise.prototype.finally) {
    Promise.prototype.finally = function f(fn){
        return this.then(
            function t(v){
                return Promise.resolve( fn() )
                    .then(function t(){
                        return v;
                    });
            },
            function c(e){
                return Promise.resolve( fn() )
                    .then(function t(){
                        throw e;
                    });
            }
        );
    };
}
```

| WARNING: |
| :--- |
| This is only a simple illustration of a basic (not entirely spec-compliant) polyfill for `finally(..)`. Don't use this polyfill in your code; always use a robust, official polyfill wherever possible, such as the collection of polyfills/shims in ES-Shim. |

The `if` statement protects the polyfill definition by preventing it from running in any environment where the JS engine has already defined that method. In older environments, the polyfill is defined, but in newer environments the `if` statement is quietly skipped.

Transpilers like Babel typically detect which polyfills your code needs and provide them automatically for you. But occasionally you may need to include/define them explicitly, which works similar to the snippet we just looked at.

Always write code using the most appropriate features to communicate its ideas and intent effectively. In general, this means using the most recent stable JS version. Avoid negatively impacting the code's readability by trying to manually adjust for the syntax/API gaps. That's what tools are for!

Transpilation and polyfilling are two highly effective techniques for addressing that gap between code that uses the latest stable features in the language and the old environments a site or application needs to still support. Since JS isn't going to stop improving, the gap will never go away. Both techniques should be embraced as a standard part of every JS project's production chain going forward.

## What's in an Interpretation?

A long-debated question for code written in JS: is it an interpreted script or a compiled program? The majority opinion seems to be that JS is an interpreted (scripting) language. But the truth is more complicated than that.

For much of the history of programming languages, "interpreted" languages and "scripting" languages have been looked down on as inferior compared to their compiled counterparts. The reasons for this acrimony are numerous, including the perception that there is a lack of performance optimization, as well as dislike of certain language characteristics, such as scripting languages generally using dynamic typing instead of the "more mature" statically typed languages.

Languages regarded as "compiled" usually produce a portable (binary) representation of the program that is distributed for execution later. Since we don't really observe that kind of model with JS (we distribute the source code, not the binary form), many claim that disqualifies JS from the category. In reality, the distribution model for a program's "executable" form has become drastically more varied and also less relevant over the last few decades; to the question at hand, it doesn't really matter so much anymore what form of a program gets passed around.

These misinformed claims and criticisms should be set aside. The real reason it matters to have a clear picture on whether JS is interpreted or compiled relates to the nature of how errors are handled.

Historically, scripted or interpreted languages were executed in generally a top-down and line-by-line fashion; there's typically not an initial pass through the program to process it before execution begins (see Figure 1).

<figure>
    <img src="images/fig1.svg" width="650" alt="Interpreting a script to execute it" align="center">
    <figcaption><em>Fig. 1: Interpreted/Scripted Execution</em></figcaption>
    <br><br>
</figure>

In scripted or interpreted languages, an error on line 5 of a program won't be discovered until lines 1 through 4 have already executed. Notably, the error on line 5 might be due to a runtime condition, such as some variable or value having an unsuitable value for an operation, or it may be due to a malformed statement/command on that line. Depending on context, deferring error handling to the line the error occurs on may be a desirable or undesirable effect.

Compare that to languages which do go through a processing step (typically, called parsing) before any execution occurs, as illustrated in Figure 2:

<figure>
    <img src="images/fig2.svg" width="650" alt="Parsing, compiling, and executing a program" align="center">
    <figcaption><em>Fig. 2: Parsing + Compilation + Execution</em></figcaption>
    <br><br>
</figure>

In this processing model, an invalid command (such as broken syntax) on line 5 would be caught during the parsing phase, before any execution has begun, and none of the program would run. For catching syntax (or otherwise "static") errors, generally it's preferred to know about them ahead of any doomed partial execution.

So what do "parsed" languages have in common with "compiled" languages? First, all compiled languages are parsed. So a parsed language is quite a ways down the road toward being compiled already. In classic compilation theory, the last remaining step after parsing is code generation: producing an executable form.

Once any source program has been fully parsed, it's very common that its subsequent execution will, in some form or fashion, include a translation from the parsed form of the program—usually called an Abstract Syntax Tree (AST)—to that executable form.

In other words, parsed languages usually also perform code generation before execution, so it's not that much of a stretch to say that, in spirit, they're compiled languages.

JS source code is parsed before it is executed. The specification requires as much, because it calls for "early errors"—statically determined errors in code, such as a duplicate parameter name—to be reported before the code starts executing. Those errors cannot be recognized without the code having been parsed.

So **JS is a parsed language**, but is it *compiled*?

The answer is closer to yes than no. The parsed JS is converted to an optimized (binary) form, and that "code" is subsequently executed (Figure 2); the engine does not commonly switch back into line-by-line execution (like Figure 1) mode after it has finished all the hard work of parsing—most languages/engines wouldn't, because that would be highly inefficient.

To be specific, this "compilation" produces a binary byte code (of sorts), which is then handed to the "JS virtual machine" to execute. Some like to say this VM is "interpreting" the byte code. But then that means Java, and a dozen other JVM-driven languages, for that matter, are interpreted rather than compiled. Of course, that contradicts the typical assertion that Java/etc are compiled languages.

Interestingly, while Java and JavaScript are very different languages, the question of interpreted/compiled is pretty closely related between them!

Another wrinkle is that JS engines can employ multiple passes of JIT (Just-In-Time) processing/optimization on the generated code (post parsing), which again could reasonably be labeled either "compilation" or "interpretation" depending on perspective. It's actually a fantastically complex situation under the hood of a JS engine.

So what do these nitty-gritty details boil down to? Step back and consider the entire flow of a JS source program:

1. After a program leaves a developer's editor, it gets transpiled by Babel, then packed by Webpack (and perhaps half a dozen other build processes), then it gets delivered in that very different form to a JS engine.

2. The JS engine parses the code to an AST.

3. Then the engine converts that AST to a kind-of byte code, a binary intermediate representation (IR), which is then refined/converted even further by the optimizing JIT compiler.

4. Finally, the JS VM executes the program.

To visualize those steps, again:

<figure>
    <img src="images/fig3.svg" width="650" alt="Steps of JS compilation and execution" align="center">
    <figcaption><em>Fig. 3: Parsing, Compiling, and Executing JS</em></figcaption>
    <br><br>
</figure>

Is JS handled more like an interpreted, line-by-line script, as in Figure 1, or is it handled more like a compiled language that's processed in one-to-several passes first, before execution (as in Figures 2 and 3)?

I think it's clear that in spirit, if not in practice, **JS is a compiled language**.

And again, the reason that matters is, since JS is compiled, we are informed of static errors (such as malformed syntax) before our code is executed. That is a substantively different interaction model than we get with traditional "scripting" programs, and arguably more helpful!

### Web Assembly (WASM)

One dominating concern that has driven a significant amount of JS's evolution is performance, both how quickly JS can be parsed/compiled and how quickly that compiled code can be executed.

In 2013, engineers from Mozilla Firefox demonstrated a port of the Unreal 3 game engine from C to JS. The ability for this code to run in a browser JS engine at full 60fps performance was predicated on a set of optimizations that the JS engine could perform specifically because the JS version of the Unreal engine's code used a style of code that favored a subset of the JS language, named "ASM.js".

This subset is valid JS written in ways that are somewhat uncommon in normal coding, but which signal certain important typing information to the engine that allow it to make key optimizations. ASM.js was introduced as one way of addressing the pressures on the runtime performance of JS.

But it's important to note that ASM.js was never intended to be code that was authored by developers, but rather a representation of a program having been transpiled from another language (such as C), where these typing "annotations" were inserted automatically by the tooling.

Several years after ASM.js demonstrated the validity of tooling-created versions of programs that can be processed more efficiently by the JS engine, another group of engineers (also, initially, from Mozilla) released Web Assembly (WASM).

WASM is similar to ASM.js in that its original intent was to provide a path for non-JS programs (C, etc.) to be converted to a form that could run in the JS engine. Unlike ASM.js, WASM chose to additionally get around some of the inherent delays in JS parsing/compilation before a program can execute, by representing the program in a form that is entirely unlike JS.

WASM is a representation format more akin to Assembly (hence, its name) that can be processed by a JS engine by skipping the parsing/compilation that the JS engine normally does. The parsing/compilation of a WASM-targeted program happen ahead of time (AOT); what's distributed is a binary-packed program ready for the JS engine to execute with very minimal processing.

An initial motivation for WASM was clearly the potential performance improvements. While that continues to be a focus, WASM is additionally motivated by the desire to bring more parity for non-JS languages to the web platform. For example, if a language like Go supports threaded programming, but JS (the language) does not, WASM offers the potential for such a Go program to be converted to a form the JS engine can understand, without needing a threads feature in the JS language itself.

In other words, WASM relieves the pressure to add features to JS that are mostly/exclusively intended to be used by transpiled programs from other languages. That means JS feature development can be judged (by TC39) without being skewed by interests/demands in other language ecosystems, while still letting those languages have a viable path onto the web.

Another perspective on WASM that's emerging is, interestingly, not even directly related to the web (W). WASM is evolving to become a cross-platform virtual machine (VM) of sorts, where programs can be compiled once and run in a variety of different system environments.

So, WASM isn't only for the web, and WASM also isn't JS. Ironically, even though WASM runs in the JS engine, the JS language is one of the least suitable languages to source WASM programs with, because WASM relies heavily on static typing information. Even TypeScript (TS)—ostensibly, JS + static types—is not quite suitable (as it stands) to transpile to WASM, though language variants like AssemblyScript are attempting to bridge the gap between JS/TS and WASM.

This book isn't about WASM, so I won't spend much more time discussing it, except to make one final point. *Some* folks have suggested WASM points to a future where JS is excised from, or minimized in, the web. These folks often harbor ill feelings about JS, and want some other language—any other language!—to replace it. Since WASM lets other languages run in the JS engine, on its face this isn't an entirely fanciful fairytale.

But let me just state simply: WASM will not replace JS. WASM significantly augments what the web (including JS) can accomplish. That's a great thing, entirely orthogonal to whether some people will use it as an escape hatch from having to write JS.

## *Strict*ly Speaking

Back in 2009 with the release of ES5, JS added *strict mode* as an opt-in mechanism for encouraging better JS programs.

The benefits of strict mode far outweigh the costs, but old habits die hard and the inertia of existing (aka "legacy") code bases is really hard to shift. So sadly, more than 10 years later, strict mode's *optionality* means that it's still not necessarily the default for JS programmers.

Why strict mode? Strict mode shouldn't be thought of as a restriction on what you can't do, but rather as a guide to the best way to do things so that the JS engine has the best chance of optimizing and efficiently running the code. Most JS code is worked on by teams of developers, so the *strict*-ness of strict mode (along with tooling like linters!) often helps collaboration on code by avoiding some of the more problematic mistakes that slip by in non-strict mode.

Most strict mode controls are in the form of *early errors*, meaning errors that aren't strictly syntax errors but are still thrown at compile time (before the code is run). For example, strict mode disallows naming two function parameters the same, and results in an early error. Some other strict mode controls are only observable at runtime, such as how `this` defaults to `undefined` instead of the global object.

Rather than fighting and arguing with strict mode, like a kid who just wants to defy whatever their parents tell them not to do, the best mindset is that strict mode is like a linter reminding you how JS *should* be written to have the highest quality and best chance at performance. If you find yourself feeling handcuffed, trying to work around strict mode, that should be a blaring red warning flag that you need to back up and rethink the whole approach.

Strict mode is switched on per file with a special pragma (nothing allowed before it except comments/whitespace):

```js
// only whitespace and comments are allowed
// before the use-strict pragma
"use strict";
// the rest of the file runs in strict mode
```

| WARNING: |
| :--- |
| Something to be aware of is that even a stray `;` all by itself appearing before the strict mode pragma will render the pragma useless; no errors are thrown because it's valid JS to have a string literal expression in a statement position, but it also will silently *not* turn on strict mode! |

Strict mode can alternatively be turned on per-function scope, with exactly the same rules about its surroundings:

```js
function someOperations() {
    // whitespace and comments are fine here
    "use strict";

    // all this code will run in strict mode
}
```

Interestingly, if a file has strict mode turned on, the function-level strict mode pragmas are disallowed. So you have to pick one or the other.

The **only** valid reason to use a per-function approach to strict mode is when you are converting an existing non-strict mode program file and need to make the changes little by little over time. Otherwise, it's vastly better to simply turn strict mode on for the entire file/program.

Many have wondered if there would ever be a time when JS made strict mode the default? The answer is, almost certainly not. As we discussed earlier around backwards compatibility, if a JS engine update started assuming code was strict mode even if it's not marked as such, it's possible that this code would break as a result of strict mode's controls.

However, there are a few factors that reduce the future impact of this non-default "obscurity" of strict mode.

For one, virtually all transpiled code ends up in strict mode even if the original source code isn't written as such. Most JS code in production has been transpiled, so that means most JS is already adhering to strict mode. It's possible to undo that assumption, but you really have to go out of your way to do so, so it's highly unlikely.

Moreover, a wide shift is happening toward more/most new JS code being written using the ES6 module format. ES6 modules assume strict mode, so all code in such files is automatically defaulted to strict mode.

Taken together, strict mode is largely the de facto default even though technically it's not actually the default.

## Defined

JS is an implementation of the ECMAScript standard (version ES2019 as of this writing), which is guided by the TC39 committee and hosted by ECMA. It runs in browsers and other JS environments such as Node.js.

JS is a multi-paradigm language, meaning the syntax and capabilities allow a developer to mix and match (and bend and reshape!) concepts from various major paradigms, such as procedural, object-oriented (OO/classes), and functional (FP).

JS is a compiled language, meaning the tools (including the JS engine) process and verify a program (reporting any errors!) before it executes.

With our language now *defined*, let's start getting to know its ins and outs.

[^specApB]: ECMAScript 2019 Language Specification, Appendix B: Additional ECMAScript Features for Web Browsers, https://www.ecma-international.org/ecma-262/10.0/#sec-additional-ecmascript-features-for-web-browsers (latest as of time of this writing in January 2020)
