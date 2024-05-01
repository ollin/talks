# Hypermedia-Driven Applications with HTMX

## next public talk(s):
* [2024-05-14 - Basel - Switzerland](https://www.jug.ch/html/events/2024/htmx_bs.html)

## past public talks
* [2024-04-30 - Bern - Switzerland](https://www.jug.ch/html/events/2024/htmx_be.html), no recording
* [2024-04-24 - Lucerne - Switzerland](https://www.jug.ch/html/events/2024/htmx_lu.html), no recording

## Talk Resources
* [Slides - Deutsch,German](https://docs.google.com/presentation/d/1PsLzS-oLv9CQgDPbuWp6F2hV3l6Y162eafKhHuZbLWE/edit?usp=sharing)
* [example project - Spring Boot, Kotlin, Thymeleaf - based on the book (see below)](https://github.com/ollin/htmxbook)
* [example project - Ktor, Kotlin, kotlinx html dsl, - also based on the book (see below)](https://github.com/ollin/contacts)

### HTMX resources
* [htmx.org](https://htmx.org/)
* [book about Hypermedia Systems](https://hypermedia.systems/)
* [Video with Carson Gross - creator of HTMX](https://www.youtube.com/watch?v=LriHRa9t1fQ) and [@ThePrimeagen](https://twitter.com/ThePrimeagen)
* [Video](https://youtu.be/-ptq9HCrI_U?t=353) with good explaination about state management and what to choose when
* [Video](https://www.youtube.com/watch?v=0l6I0tA-Il4) with more details about HTMX (big thx [Lars](https://github.com/LarsEckart) for showing me the video)

### HTMX + JVM (Java, Kotlin, ...) related stuff
* [Spring Boot and Thymeleaf library for htmx](https://github.com/wimdeblauwe/htmx-spring-boot)
* [Typesafe HTML DSL](https://kotlinlang.org/docs/typesafe-html-dsl.html)

### Comparisons with other frameworks
#### JVM
* [Efficient Full-Stack Development with Java | Simon Martinelli](https://www.youtube.com/watch?v=FI1Ao-qFFoY) (big thx to [Simon](https://github.com/simasch) for making it! und [Peti](https://github.com/Petikoch) for showing me the video)

  

## Oliver Nautsch<!-- include: oliver.md -->

* [LinkedIn](https://www.linkedin.com/in/oliver-nautsch/)
* [X (aka Twitter)](https://twitter.com/ollispieps)


<!-- endInclude -->

# notes for myself
## most noticeable things / todo
1. When I use the kotlinx html dsl and use the domain model directly, I get hints in the HTML (as the DSL) from the compiler. At this point everyone becomes very attentive. For example, at compile time I get an error if I remove an attribute in the domain model but still use it in the UI code. So no runtime error, which is very good. I should do all the examples with the typesafe html dsl.
2. We need a component library for the kotlins html dsl. I have no idea at the moment what makes sense, but the listeners keep asking.
3. The string literals when setting the attribute values of HTMX in the DSL feel unnatural.  An extension of the DSL would also make sense here.
4. Somehow I have to get the type save routing (see: https://ktor.io/docs/server-resources.html#resource_url) from Ktor into the DSL when I configure the HTTP methods with HTMX.

## feedback
* Guter Mix von Einführung/Basics, Thema und dann der Aspekt Frontend Team. (translated: Good mix of introduction/basics, topic and then the frontend team aspect.)
* Einleitung/Einstieg war etwas schwierig, wenn man sich vorher noch nicht HTMX angeschaut hat. (translated: Introduction/entry was a bit difficult if you haven't watched HTMX before.)
* Wichtiges Thema. Wes? Frontends ist mehr als Angular, Vue, React,... (Frontend Architektur) (tranlasted: Important topic. What? Frontends is more than Angular, Vue, React,... (Frontend architecture))
* Sehr spannende Erkenntnis bzgl. Code Completion und Überprüfung zur Build-Zeit im Beispiel mit Kotlin. (translated: Very exciting insight regarding code completion and check at build time in the example with Kotlin.)
