---
layout: post
title:  "New Java Developer ? Here's how you can write better code"
date:   2019-12-21 13:50:18 +0100
categories: jekyll update
published: true
---

_Work in progress, alpha version 0.1_

Fresh out from university, ready to start your career, frustrated because your code is not satisfying ? 

Here's a compilation of all the resources to you can read and watch to write better code:

_Note: this is a strongly opinionated article from my own experience, for Java developers_

# Some books that you just need to read

1. Clean code
2. Pragmatic Programmer
3. Testing Driven Development

_I'm not trying to be comprehensive here, but I try to be reasonable on where to start_

Other books that are worth recommending:
* Clean Coder
* Refactoring
* Gof patterns
* Effective Java
* ...

# Tooling
Use static code analysis like Sonar, by seeing the code violations (read the rules!) you'll avoid making the same mistake twice.

In the same field, use Intellij. I know that coming from Eclipse or Netbeans it seems overwhelming, but the thing that detect mistake 
and the tool is very very nice. The free community edition is already good with a lot of features.

# Learn your environment: 
 Java is not everything. You also need a lot of extra knowledge:
 
 * A build tool like Maven or Gradle
 * Application servers like JBoss, or the new thing with Spring Boot
 * Spring, and understand concepts of dependency injection and inversion of control
 * Jakarta EE, because usually when you work in an enterprise, you need enterprise Java
 * Database: always handy to know how a database works because your application cannot be totally agnostic. Note that there
 are now plain old relational databases, and NoSQL databases that also need to be considered 
 * Database interaction: JDBC, ORM-JPA (hibernate)
 * Testing: at least Junit, and if you want more, AssertJ and Mockito 
 * Linux, because your server will run on Linux, knowing how to read logs, user permission, basic shell script, ... 
 is always handy
 * Cloud, IaaS, PaaS, Docker, ... : usually applications don't live anymore on a simple server but on the Cloud, you need
 at least to know the basicsd
 * Webservices: SOAP and Rest are the two main actors here
 * UI technologies: it's hard here to suggest one, I would say try to keep up with the most used currently on a worlwide scale. 
 According to https://hotframeworks.com/, it's React and AngularJS 
 * Messaging: I suggest at least the basics of JMS 
 * Batches: Spring Batch is a major actor here
 * Git: Yes it's better than SVN, and yes it's complicated but it's worth it !
 
# Know your Java
 
 You don't usually use all the features of Java. But the more you know, the better, as you'll be able to have the right tool
 or information to tackle the many difficulties of development.
 
 I would say, read this excellent book: OCA: Oracle Certified Associate Java SE 8 Programmer I Study Guide: Exam 1Z0-808.  (TODO check that
 it's the same author than the one I read), and while you are a it, pass the certification if you can.
 
 Follow Java actuality, watch conferences one the subjet (usually all the talks are freely available on youtube, like Devoxx, SpringOne, ...)
 
 I like the Java Magazine: https://blogs.oracle.com/javamagazine/

# At your job (or not)
_It's hard to not quote all the pragmatic programmer stuff, I'll try to highlight the most important for me_

* Find a mentor
* Do a lot of pair programming
* Ask for frequent code review
* Look at better code 
* Publish your code on github, it's a nice way to push yourself: if a code is public, then you'll think twice before writing
something stupid

# Go for Open Source ?
Yes sure, if you can. But I think it's a little hard for a newcomer, but don't hesitate to start there, the difficulty is 
to find a project where you can effectively contribute.


