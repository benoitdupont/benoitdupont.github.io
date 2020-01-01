---
layout: post
title:  "New Java Developer ? Here's how you can write better code"
date:   2019-12-21 13:50:18 +0100
categories: Java
---

_Work in progress, alpha version 0.3_

Fresh out from university, ready to start your career, wanting to improve your coding skills ? 

Here's a compilation full of resources that you can read and watch to write better code:

_Note: this is a strongly opinionated article from my own experience, for an audience of junior Java developers_

# Some books that you just need to read

1. Clean Code: A Handbook of Agile Software Craftsmanship, by Uncle Bob. A great book on how to write simple and elegant code
2. The Pragmatic Programmer: From Journeyman to Master, by Andrew Hunt and David Thomas. A good general purpose book on the skills and 
the ecosystem to become a good programmer.  
3. Test Driven Development: By Example, by Kent Beck. It's not easy to be convinced about TDD by reading theory on the subject. But seeing it 
in action in the book is way better.

# Learn your environment
 Knowning the Java programming language is not enough, you also need to know how it interact with the other components to 
 answer business requirement. Here's a list of subjects that you need to at least understand in a general way:
 
 * A build tool like Maven or Gradle
 * Application servers like JBoss, ...
 * Spring Boot 
 * Spring, and understand concepts of dependency injection and inversion of control
 * Jakarta EE, because usually when you work in an enterprise, you need enterprise Java
 * Database: it's always handy to know how a database works because your application cannot be totally agnostic. Note that there
 are now plain old relational databases (Oracle, PostgreSQL, ...) but also NoSQL databases (MongoDB, Cassandra, Neo4j, ...)
  that also need to be considered 
 * Java libraries and frameworks that interact Database interaction: JDBC, ORM/JPA (Hibernate)
 * Testing: at least JUnit, and if you want more, Testing Driven Development, AssertJ and Mockito 
 * Linux, because your server will most probably run on Linux, knowing how to read logs, user permission, basic shell script, ... 
 is always handy.
 * Cloud, IaaS, PaaS, Docker, ... : usually applications don't live anymore on a simple server but on the Cloud, you need
 at least to know the basics
 * SOAP and Rest webservices 
 * UI technologies: it's hard here to suggest one, I would say try to keep up with the most used currently on a worlwide scale. 
 According to https://hotframeworks.com/, it's React and Angular
 * Messaging: I suggest at least the basics of JMS (Java Messaging System) 
 * Batches: Spring Batch is one of the major actors here
 * Git: Yes it's better than SVN, and yes it's complicated but it's worth it !
 * CI/CD: The concepts of continuous integration and continuous development are really important to grasp when you not only develop code, 
 but need to ship it into production.
 
# Know your Java
 
You don't usually use all the features of Java. But the more you know, the better, as you'll be able to have the right tool
 or information to tackle the many difficulties of development.
 
After several years of Java development, I got the opportunity to be certified in Java. I read the excellent book 
SCJP Sun Certified Programmer for Java 5 Study Guide (Exam 310-055) from Katherine Sierra and Bert Bates which very instructive.
(TODO confirm this) Read the most recent the book _OCA: Oracle Certified Associate Java SE 8 Programmer I Study Guide: 
Exam 1Z0-808_, and if you've got the opportunity, do get certified !
 
Follow Java actuality by reading blogs and magazines like the [Java Magazine][https://blogs.oracle.com/javamagazine] or
the [stack overflow blog/newsletter][https://stackoverflow.blog/newsletter]
Watch conferences one the subject, usually all the talks are freely available on youtube, like Devoxx, SpringOne, ...

Use static code analysis tools like Sonar in order to detect the mistakes in your code, and don't hesitate to read the rules used used to detect defects.
 
# At your job
_It's hard to not quote all the pragmatic programmer stuff, I'll try to highlight the most important for me_

* Find a mentor
* Do a lot of pair (or mob) programming
* Ask for frequent code review
* Look at good code, for example mature Open Source framework like Spring 
* Publish your code on github, it's a nice way to push yourself: if a code is public, then you'll think twice before writing
something stupid

# Go for Open Source ?
Yes ! There are two ways here, that both requires a lot of involvement:

1. Create your own project, publish it, spread the words and you could start building something collaboratively
1. Find a project and contribute

While I won't advise against Open Source, two remarks: 

For #1 it's not that easy to find an original idea, less be able to attract people to use it. But don't hesitate if you 
want it, as it won't be lost time
For #2, it's not that easy to find a good project where to start and effectively contribute. You'll need something 
with ease of access for beginners, and with contributors that are disposed to help you. Luckily theses projects exists and 
usually the guys are really nice, and publish ideal issues for newcomers (first time issues).