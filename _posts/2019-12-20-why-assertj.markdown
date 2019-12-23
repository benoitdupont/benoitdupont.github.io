---
layout: post
title:  "Why Assertj ?"
date:   2019-12-20 13:50:18 +0100
categories: jekyll update
---

_Work in progress, alpha version 0.2_


_Yet another testing framework?_ 

As I was working on a project with a colleague[^1], I found that he systematically used AssertJ assertions. I did not see right away any added value
compared to plain Junit assertions, but as my initial reluctance faded, I decided to give it a go, and now I'm convinced. I'll try to demonstrate
here one of the many cool features of this nice framework. 

Let introduce the protagonists of the story: 

I want to know if Daenerys[^2] has more than two names (which is a reasonable number already), 
and is the Mother of Dragons (which is generally the latest name, as the most important), so let's ask her:
{% highlight java %}
//Given
Daenerys dae = new Daenerys(
            "Daenerys Stormborn of the House Targaryen",
            "the First of Her Name",
            "The Unburnt",
            "Queen of the Andals and the First Men",
            "Khaleesi of the Great Grass Sea",
            "Breaker of Chains",
            "Mother of Dragons");

// When
List<String> theManyNamesOfDaenerys = dae.whatsYourName();

// Then, in classic JUnit way                       
assertNotNull(theManyNamesOfDaenerys);
assertTrue(theManyNamesOfDaenerys.size() > 2);

String oneOfTheseNames = theManyNamesOfDaenerys.get(6);
assertEquals(oneOfTheseNames, "Mother of Dragons");
{% endhighlight %}

Asserting on a specific object in a Collection is usually a frequent use case, and to avoid NPE and such,  
you need to assert that the collection is not null and has the correct size, then you need to extract the element in a 
variable and finally assert on his content. During many years this has bothered me and I wanted a way to write this in a
more elegant way.  

And now with AssertJ:

{% highlight java %}
assertThat(names)
        .hasSizeGreaterThan(2)
        .last()
        .isEqualTo("Mother of Dragons");
{% endhighlight %}

So much concise, wow ! And look at the interesting assertions like ``hasSizeGreaterThan`` and ``last``, which are collection/list specific.

As you can see, and as stated on the [AssertJ-website]: _AssertJ's ambition is to provide a rich and intuitive set of strongly-typed assertions for unit testing._

So in other words, by providing the object to the ``assertThat``, you automagically receive tailor-made/specific assertions for the 
type of the object !

Let's take a boolean

{% highlight java %}
assertThat(jonSnow.doYouKnowNothing())
    .isTrue();
{% endhighlight %}

Or a String:

{% highlight java %}
assertThat("You know nothing, Jon Snow")
    .startsWith("You know nothing")
    .isBlank()
    .contains("Jon")
    //... and many other assertions
{% endhighlight %}

Note that error messages are also very detailed in AssertJ. 

Here's a failing ``assertEquals(6, theManyNamesOfDaenerys)`` in JUnit:
```
org.opentest4j.AssertionFailedError: 
Expected :6
Actual   :7
<Click to see difference>
```

And with AssertJ:
```
java.lang.AssertionError:
Expected size:<6> but was:<7> in:
<["Daenerys Stormborn of the House Targaryen",
  "the First of Her Name",
  "The Unburnt",
  "Queen of the Andals and the First Men",
  "Khaleesi of the Great Grass Sea",
  "Breaker of Chains",
  "Mother of Dragons"]>
```

I still use and like JUnit, but now with AssertJ I found library that provide better assertions, that leads to a code more 
concise and elegant and better feedback on failed tests. I prefer using one clever and assertion over multiple simpler ones.

Note that theses are only some the many nice features of AssertJ, more on this on my next article: 10 things I didn't know about AssertJ

TODO link with github examples

[^1]: Thank you Jeremy for this
[^2]: This is only the small name when Daenerys is presented to Khal Moro. The longer version, according to [this post][quora] on Quora is: _Daenerys Stormborn of the House Targaryen, First of Her Name, the Unburnt, Queen of the Andals and the First Men, Khaleesi of the Great Grass Sea, Breaker of Chains, and Mother of Dragons_

[quora]: https://www.quora.com/What-is-the-full-title-of-Daenerys-Targaryen
[AssertJ-website]: https://github.com/joel-costigliola/assertj-core
