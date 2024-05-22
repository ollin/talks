# Hypermedia-Driven Applications with HTMX
If anyone is interested in this talk, please contact me (see below for contact information). I am currently preparing a one-day workshop. 

## next public talk(s):
* tbd

## past public talks
* [2024-05-21 - Zürich - Switerland (English)](https://www.meetup.com/coders-only/events/300858871/), no recording
* [2024-05-14 - Basel - Switzerland (English)](https://www.jug.ch/html/events/2024/htmx_bs.html), no recording
* [2024-04-30 - Bern - Switzerland (Deutsch)](https://www.jug.ch/html/events/2024/htmx_be.html), no recording
* [2024-04-24 - Lucerne - Switzerland (Deutsch)](https://www.jug.ch/html/events/2024/htmx_lu.html), no recording

## Talk Resources
* [Slides - Deutsch,German](https://docs.google.com/presentation/d/1PsLzS-oLv9CQgDPbuWp6F2hV3l6Y162eafKhHuZbLWE/edit?usp=sharing)
* [Sides - English](https://docs.google.com/presentation/d/1dbel096SXJUOKiQS0k5fKpGL_JM09U8Be0A4x_HYXFs/edit?usp=sharing)
* [example project - based on the book (see below)](https://github.com/ollin/contacts)
  *   subproject with spring boot, thymeleaf, kotlin
  *   subproject with ktor, kotlin, typesafe html dsl

### HTMX resources
* [htmx.org](https://htmx.org/)
* [book about Hypermedia Systems](https://hypermedia.systems/)
* [Video with Carson Gross - creator of HTMX](https://www.youtube.com/watch?v=LriHRa9t1fQ) and [@ThePrimeagen](https://twitter.com/ThePrimeagen)
* [Video](https://youtu.be/-ptq9HCrI_U?t=353) with good explaination about state management and what to choose when
* [Video](https://www.youtube.com/watch?v=0l6I0tA-Il4) with more details about HTMX (big thx [Lars](https://github.com/LarsEckart) for showing me the video)
* [Video - From React to htmx on a real-world SaaS product: we did it, and it's awesome!](https://www.youtube.com/watch?v=3GObi93tjZI)

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
   - [Ossi:](https://github.com/busykoala): the problem here is, that this is always language depenced. Designer might not want that, or can not do it.
3. The string literals when setting the attribute values of HTMX in the DSL feel unnatural.  An extension of the DSL would also make sense here.
4. Make an example with inline editing
5. Look at [fritz2](https://www.fritz2.dev/) - web components?
6. ✅ Somehow I have to get the type save routing (see: https://ktor.io/docs/server-resources.html#resource_url) from Ktor into the DSL when I configure the HTTP methods with HTMX.
   - see [Building links from ressources](https://ktor.io/docs/server-resources.html#resource_links)
```kotlin

a(classes = "text-red-600 hover:text-indigo-900") {
    id = "contact_${contact.id}"
    href = "#"
    attributes["hx-delete"] = application.href<Contacts.Id>(Contacts.Id(id = contact.id))

...


@Resource("contacts")
class Contacts {
    @Resource("{id}")
    class Id(val parent: Contacts = Contacts(), val id: UuidAsString)
}
```   

## feedback
* Guter Mix von Einführung/Basics, Thema und dann der Aspekt Frontend Team. (translated: Good mix of introduction/basics, topic and then the frontend team aspect.)
* Einleitung/Einstieg war etwas schwierig, wenn man sich vorher noch nicht HTMX angeschaut hat. (translated: Introduction/entry was a bit difficult if you haven't watched HTMX before.)
* Wichtiges Thema. Wes? Frontends ist mehr als Angular, Vue, React,... (Frontend Architektur) (tranlasted: Important topic. What? Frontends is more than Angular, Vue, React,... (Frontend architecture))
* Sehr spannende Erkenntnis bzgl. Code Completion und Überprüfung zur Build-Zeit im Beispiel mit Kotlin. (translated: Very exciting insight regarding code completion and check at build time in the example with Kotlin.)
* Super workshop heute!
