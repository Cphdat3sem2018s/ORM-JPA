# ORM (Object Relational Mapping) with JPA (Java Persistence API)

## Learning Goals
  * Understand the purpose of Object-relational mapping (ORM): When and how to use it
ORM / JPA / JPQL
  * Be able to use JPA as an ORM in java.  
    Be able to:
    * Generate Entity classes from a database.
    * Generate database tables from entity classes.
    * Work around/with the incongruences/impedance between database- and OOP-modelling
      (I.e. issues related to inheritance, directionality, and cardinality).
  * Be able to create/read/update/delete entities with the EntityManager
  * Be able to create named / dynamic JPQL queries.

## Business Competences
Be able to work with databases through an ORM framework. The focus is on
java/JPA, but the core concepts are widely applicable.

## Plan (starting from Tuesday)
This week we will use a mixture of oracle documentation/tutorials and the Java
Persistence wikibook. While the wikibook seems significantly easier to read, it
is not structured to follow our schedule, and it is overly verbose. The java
materials on the other hand tend to be too terse, but to the point. Therefore,
we will be jumping back and forth between these resources, but you may find that
you prefer one over the other. In that event, it should be possible for you to
find most relevant information in either, but you may have to look around for it.

### [Day 1](Day1) Introduction to ORM 
What/why is an ORM, install eclipselink+mysql dependencies, generate tables,
generate classes (reverse JPA), the persistence unit, the Entity class, the
EntityManager.

The reading materials are:
  * [ORM](https://en.wikipedia.org/wiki/Object-relational_mapping)
    Introdiction and sections 1-2
  * [Java Persistence wikibook](https://en.wikibooks.org/wiki/Java_Persistence)
    Read:
      * the first 3 paragraphs of 3.3 (until "JPA is the latest of several..")
      * 5 intro titled "Mapping, Round..". Stop at the "Access Type" section
  * [Oracle persistence tutorial](https://docs.oracle.com/javaee/7/tutorial/persistence-intro001.htm#BNBQA)
    The language in this resource is somewhat dense. It may be beneficial to
    read this after the lecture, rather than before.
    Read:
      * 37.1 (the intro on the linked page),
      * 37.1.1 - 37.1.2.1
      * 37.1.3
  * [Java Persistence wikibook](https://en.wikibooks.org/wiki/Java_Persistence)
    (Same resource as before)
    Read 6.2 "Persisting (Inserting, Updating, Merging)":
      * 1-1.2.1 (detach vs managed, persist..)
      * 1.3-1.3.2 (merge)
  * The JPA annotations are listed and documented
    [here](https://docs.oracle.com/javaee/7/api/javax/persistence/package-summary.html)
    (scroll down to "Annotation Types Summary"), and some are better explained
    [here](http://www.oracle.com/technetwork/middleware/ias/toplink-jpa-annotations-096251.html#Basic).
    Do not read these, use them to look annotations up if/as you need them.

The following tutorial from netbeans, as well as a couple videos
Christian made, may help you through the JPA setup process if you forget it
after the lecture.
These are _not_ useful learning resources. I recommend only using them if you
forget how to setup the persistence unit, and do table/class generation with JPA.
  * [netbeans persistence unit tutorial](http://wiki.netbeans.org/SimpleJPAApplicationWithNetbeans#Create_Persistence_Unit)
  * [Video JPA setup](https://www.twitch.tv/videos/168683174)
  * [Video JPA database table -> entityclass](https://www.twitch.tv/videos/168934609)
  * [Video JPA relationships](https://www.twitch.tv/videos/168939780)

### [Day 2](Day2) - Relationships 
Relationships, cardinality, directionality.

Reading materials:
  * [Oracle tutorial](https://docs.oracle.com/javaee/7/tutorial/persistence-intro001.htm#BNBQA) Read:  
    37.1.4-37.1.6 (end of chapter).


### [Day 3](Day3) - Inheritance and JPQL
Inheritance in OOP vs ER, strategies for inheritance in JPA, queries, facade.

Reading materials:
  * [Java Persistence Wikibook](https://en.wikibooks.org/wiki/Java_Persistence/Inheritance) Inheritance chapter.  
    Skip the XML examples.
  * [Java Persistence Wikibook](https://en.wikibooks.org/wiki/Java_Persistence/Inheritance) JPQL chapter. Read:  
    1-1.5


## Exercises
[Exercise 1 - Basic JPA](https://docs.google.com/document/d/1CB9LYW6uzFy6ibe7fLSHGI_5Ymx6kzdSdARNtsNO0ME/edit?usp=sharing)<br>
<!--
[Exercise 2 - Relationships](https://docs.google.com/document/d/1Juic12T0bjb2sf-9dTuxrKXa1l5QA6ak-wTTINlK4dY/edit?usp=sharing)<br>
[Exercise 3 - Inheritance](https://docs.google.com/document/d/1IiTDPL4wDW_0S8sWAHxH_ijYu9SyB6xzyql7aRnTomI/edit?usp=sharing)<br>
[Exercise 4 - JPQL](https://docs.google.com/document/d/18QeY8y6yz0JVo39gQfQ22InDUHtBN29ViFao5s4tQPc/edit?usp=sharing)

## Study point exercises
[Study point exercises](https://docs.google.com/document/d/1BKihRmnhl18P5GCzSlO3UnDlUBm5fEaLUalaiTTxev4/edit?usp=sharing)
-->

<!--
## References

**Relationships**<br>
<a href="https://www.javacodegeeks.com/2015/02/jpa-tutorial.html" target="_blank">Javacodegeeks (Chapters 5, 5.1, 5.2, 5.3)</a><br>
<a href="https://www.tutorialspoint.com/jpa/jpa_entity_relationships.htm" target="_blank">Tutorialspoint - Relationships</a><br>

**Inheritance**<br>
<a href="https://www.javacodegeeks.com/minibook/jpa-minibook" target="_blank">JPA Minibook (Pages 25-33)</a><br>
<a href="https://en.wikibooks.org/wiki/Java_Persistence/Inheritance" target="_blank">Wikibooks - Persistence</a><br>

**Entity manager**<br>
<a href="https://www.tutorialspoint.com/jpa/jpa_entity_managers.htm" target="_blank">Tutorialspoint - Entity manager</a><br>

**JPQL**<br>
[Wikibooks - JPQ](https://en.wikibooks.org/wiki/Java_Persistence/JPQL)  
this the main resource on JPQL)  
[JBay Blog - JPQL Tutorial](http://blog.jbaysolutions.com/2014/10/16/jpa-2-tutorial-queries-on-the-model)  
[JPQL demo part 1](https://drive.google.com/open?id=0BwZfnBsxgR1jYXdqMjVTU3dGTDA)  
[JPQL demo part 2](https://drive.google.com/open?id=0BwZfnBsxgR1jVWlfd28zN2JYUm8) -- this may not play in the browser, but you can download it.
-->
