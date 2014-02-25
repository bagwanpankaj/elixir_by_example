---
layout: post
title:  "Introduction to Elixir"
date:   2014-02-25 21:54:30
tags: introduction
---

Elixir is a functional, meta-programming aware language that translates to Erlang VM. It is a dynamic language with flexible syntax and macro support that leverages Erlang's abilities to build concurrent, distributed and fault-tolerant applications with hot code upgrades.

It also makes it easy to bite erlang syntax and macro's (that is in general way tough for people from OO world). So In conclusion we can say that it leverages ruby's expressiveness and erlang's efficient and proven VM; to make developing great application easy.

#### Prequisite

There are no prequisite to run elixir except

1.) Elrang VM, go get yours from [here](http://www.erlang.org/download.html) or by your OS's preferred package manager.

#### Installation

I am not gonna cover these trivial stuff here, as they are already covered [here](http://elixir-lang.org/getting_started/1.html), in detail.

<!-- more --> 

#### Overview

Erlang is functional language, so is elixir. Variables are immutables, that means a variable can not be mutable in its given scope/visibility.

Some features of elixir language are:

1.) Expression syntax: In Elixir, everything is an expression. if, case, cond, try, unless, receive, and so on are all expressions that result in a value when evaluated. 

2.) Pattern matching: In elixir, values are always matched, if noticed, = syntax is a matcher, not assigner. Any value can be matched against using a syntax similar to.

3.) First-class functions: Functions are values in Elixir, and can be passed to other functions. This feature is at the core of functional programming and is what makes functions like foldl and foldr useful.

4.) Closures: Elixir has full-fledged lexical closures as seen in other functional programming languages, making higher-order operations like map and reduce easy to use.

5.) Records: Records in elixir are more useful and elagent than Erlang.
In Elixir, a record consists of 3 things: A module, a list of attributes, and methods to manipulate attributes. Records have the same tuple representation as in Erlang, but record methods can be called directly on record values.

6.) Protocols: A common problem in Erlang is that extending APIs for new types is close to impossible if the API doesn’t allow passing in functions to handle custom types. In object-oriented languages, interfaces usually solve this problem. In Elixir, protocols can be used to dispatch function calls dynamically based on the type of a value.

7.) Metaprogramming: Instead of Erlang’s C-like preprocessor, Elixir has Lisp-style hygienic macros. Such a macro system is significantly less error-prone and makes AST manipulation at compile-time trivial. In addition, all Elixir code inside macros and in module/record definitions is executed at compile-time making possibilities for code generation practically limitless.
Unicode strings: All strings in Elixir are encoded in UTF-8 as Erlang binaries. Similarly, all functions in the String module assume UTF-8 encoding. Globalization is much less of a pain than in other languages thanks to this.

8.) Immutability: Everything is immutable - more or less. While all data structures are entirely immutable, state can be maintained on a per-process level. Processes also have the so-called process dictionary which can be used to maintain shared state if really necessary. It is generally frowned upon.

9.) Variable rebinding: In Elixir, variables can be rebound to different values, even though everything is immutable. It turns out that this is useful in practice and doesn’t actually violate immutability (single assignment is not immutability). The compiler rewrites a variable rebinding as creating a new version of the variable, effectively transforming code into SSA (static single assignment) form.

10.) Erlang interop: Calling Erlang/OTP functions from Elixir has no overhead and does not look much different from regular function calls. Elixir code can also use behaviors - a feature that helps in writing modules conforming to a certain interface.