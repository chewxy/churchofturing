---
title: "What Is an Algorithm?"
date: 2018-03-05T14:39:26+11:00
author: "chewxy"
---

Conversations with children can often be very illuminating, and often in both directions. I spent the past weekend with a 7-year old child, and the child's 2-year old sibling. As a result we had many wonderful conversations about mathematics. The 7-year old (hence forth called J, and to simplify things, I'll use the "he"/"him/his" pronoun). 

J knows and understands fairly well, the concept of addition and subtraction. He's a little shaky on multiplication and is unsure about division. From conversations with the mother, I gather that he'll be taught multiplication and division in this school year. By the end of the weekend I am satisfied to report that according to his mother he now understands up to division. 

We talked about many things, but one interesting topic was addition. Halfway through, J complained to me that his sibling, M "understood" addition only if you asked M exactly in this sequence "1 + 1", "1 + 2", "1 + 3", "1 + 4".  It turns out his sibling only knew the order of the numbers, and not really addition. What struck me however, was how J described the sequence of additions. He had described them as a sequence of numbers that have 1 added to them. 

So I pressed on, and before long, J had a look of realization and asked me: "why does addition work?"

## Why Does Addition Work? ##

J had understood implicity but was unable to express some things we adults take for granted: the encapsulation of steps. Addition works because it's the encapsulation of a series of steps.

If we start with a rule that says the only way to access another number is trough incrementing along the order, then addition was the encapsulation of a number of steps of incrementing the numbers one at a time. In his own words, "it's like M crawls from 1 to 2 to 3, but I can jump!". 

That J recognized this early is quite remarkable. Adults often take this for granted. When introspective, we would of course realize we're taking one step after another. However, we didn't have a way to describe it except in ad-hoc fashion. In fact, it wasn't until the 1920s that mathematicians started wondering about the formalizing the notion of "steps" in doing mathematics. 

Following the publication of [Whitehead and Russell](https://en.wikipedia.org/wiki/Principia_Mathematica), and the posing of the [Entscheidungsproblem](https://en.wikipedia.org/wiki/Entscheidungsproblem), Emil Post did a lot of work in the 1920s in trying to formalize the notion of a "step". Convinced he was going down the wrong path, he did not publish until the 1940s. At the same time, much work was being done by Alan Turing and Alonzo Church. An often-unmentioned contemporary, George Stibitz, may also have invented something of the notion of a Turing Machine.

[Lambda calculus](https://en.wikipedia.org/wiki/Lambda_calculus) and [Turing machines](https://en.wikipedia.org/wiki/Turing_machine) are formalizations of algorithms - the methods of formalization are different, but end up being different views of the same thing. The "thing" in question is what we now call an algorithm.

## What is An Algorithm? ##

The so-called encapsulation of steps is an informal defination of an algorithm: A sequence of operations to be taken one after another. This arises very naturally in real life. We as humans, do one thing, then the next, and then the next, in sequence. The notion of "nextness" is the root of all algorithms. 

Here I must note that it is a very common thing for young children to repeatedly ask "and then?" - often to annoy adults around them -  but more and more, I am starting to believe that it is a "default mode" of a child's brain. The brain in its default state, I believe to be an emergent unhalting algorithm - the exact model of computation I suspect is closer to an infinite automata, which in some ways can be seen to be more powerful than Turing machines/lambda calculus.

But I digress.


### Features of An Algorithm ###

It's hard to pinpoint exactly what is an algorithm. We are of course able to informally say what an algorithm is. But to even begin to formalize the concept of an algorithm, we must look at what features *all* algorithms have:

* Algorithms can take an input, `I`
* Algorithms *may* have an output, `O`. There is only an output *if the algorithm terminates*.
* To compute the output, a series of steps is done. This is called  a **computation** on the input.
* If the computation terminates, the algorithm may be *interpreted* as a function that maps `I` to `O`.

There is one other thing that an algorithm must have in order to be formalized - Algorithms are made up of a finite sequence of symbols, made up of a finite alphabet. But this has to do more with the technical parts, which this post will skip.

The series of operations that is performed on the input, together with the input, is called an algorithm. 

### Computation ###

A computation is simply an operation to be performed slavishly according to the rules of the system. Turing himself remarked that it was to be done in a desultory manner.  Therefore **an algorithm is just a sequence of operations to be performed strictly according to the rules of the system**.  

The rules of the system are the rules that are necessary to solve a problem: a "programme"/"menu"/"listing" of rules, if you will. Take a guess which term came to be uses in popular parlance.


The notion of computation is inextricably linked to the idea of computability. At the risk of sounding tautological, a computable thing is one that can be computed by a computer, the act of which is called a computation and thus is able to be represented as an algorithm. Conversely speaking, if the computation does not terminate, then it means that it cannot be represented by an algorithm.

**Computable functions** are a special case of algorithms where the input and outut of the algorithm are numbers. **Computably enumerable sets** are sets where there is a computable function that can produce all the members of the set. This is particularly important in analysis, because as it turns out there are such things as computably enumerable but uncomputable sets.

In particular, the idea that **computable functions** are functions with numbers as inputs and outputs only should be troubling to the daily programmer. "But I write functions to deal with various things all the time!", is what one would say. I shall cover that in the future, when I discuss Gödelization.

I will also leave the topic of non-computable stuff to future posts.

## Back to Scheduled Programming ##

An algorithm is something we all intuitively understand on the gross level. However, the minutae requires a lot of finely tuned mathematical intuitions. You would think that having spent many years writing programs, the idea of an algorithm should be second nature to me. It isn't. At least not the formal version. 

I measure my understanding by a fairly decent yardstick: if I am able to explain a very difficult concept to a young child, or an old person, then I would have succeeded. I attempted this with J, across multiple instances and using multiple concrete examples. I think I was okay at it. Afterall, I did get him to derive up to division. 

The child did enquire about non-terminating problems, but he did not completely comprehend recursivity. I thought for the briefest moment when he asked about algorithms that computed other algorithms, he might be getting somewhere, but upon further pressing it just appeared that he got bored waiting for his mother to bring him his schnitzel.

The notion of functional abstraction (i.e. encapsulation, as opposed to abstraction from the category theory sense) was also a hard one to explain, but I went somewhere with that, so that's a future blog post.