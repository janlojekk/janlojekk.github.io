# Ruby

Ruby is an interpreted, high-level, general-purpose programming language. It was designed with an emphasis on programming productivity and simplicity. In Ruby, everything is an object, including primitive data types. It was developed in the mid-1990s by Yukihiro "Matz" Matsumoto in Japan.
Ruby is dynamically typed and uses garbage collection and just-in-time compilation. It supports multiple programming paradigms, including procedural, object-oriented, and functional programming. According to the creator, Ruby was influenced by Perl, Smalltalk, Eiffel, Ada, BASIC, Java, and Lisp.


== History ==


=== Early concept ===
Matsumoto has said that Ruby was conceived in 1993. In a 1999 post to the ruby-talk mailing list, he describes some of his early ideas about the language:
I was talking with my colleague about the possibility of an object-oriented scripting language. I knew Perl (Perl4, not Perl5), but I didn't like it really, because it had the smell of a toy language (it still has). The object-oriented language seemed very promising. I knew Python then. But I didn't like it, because I didn't think it was a true object-oriented language –  OO features appeared to be add-on to the language. As a language maniac and OO fan for 15 years, I really wanted a genuine object-oriented, easy-to-use scripting language. I looked for but couldn't find one. So I decided to make it.
Matsumoto describes the design of Ruby as being like a simple Lisp language at its core, with an object system like that of Smalltalk, blocks inspired by higher-order functions, and practical utility like that of Perl. He praised the language for its ingenuity and creativity for its solution for compiling intervals.
The name "Ruby" originated during an online chat session between Matsumoto and Keiju Ishitsuka on February 24, 1993, before any code had been written for the language. Initially two names were proposed: "Coral" and "Ruby". Matsumoto chose the latter in a later e-mail to Ishitsuka. Matsumoto later noted a factor in choosing the name "Ruby"–it was the birthstone of one of his colleagues.


=== Early releases ===
The first public release of Ruby 0.95 was announced on Japanese domestic newsgroups on December 21, 1995. Subsequently, three more versions of Ruby were released in two days. The release coincided with the launch of the Japanese-language ruby-list mailing list, which was the first mailing list for the new language.
Already present at this stage of development were many of the features familiar in later releases of Ruby, including object-oriented design, classes with inheritance, mixins, iterators, closures, exception handling and garbage collection.After the release of Ruby 0.95 in 1995, several stable versions of Ruby were released in these years:

Ruby 1.0: December 25, 1996
Ruby 1.2: December 1998
Ruby 1.4: August 1999
Ruby 1.6: September 2000In 1997, the first article about Ruby was published on the Web. In the same year, Matsumoto was hired by netlab.jp to work on Ruby as a full-time developer.In 1998, the Ruby Application Archive was launched by Matsumoto, along with a simple English-language homepage for Ruby.In 1999, the first English language mailing list ruby-talk began, which signaled a growing interest in the language outside Japan. In this same year, Matsumoto and Keiju Ishitsuka wrote the first book on Ruby, The Object-oriented Scripting Language Ruby (オブジェクト指向スクリプト言語 Ruby), which was published in Japan in October 1999. It would be followed in the early 2000s by around 20 books on Ruby published in Japanese.By 2000, Ruby was more popular than Python in Japan. In September 2000, the first English language book Programming Ruby was printed, which was later freely released to the public, further widening the adoption of Ruby amongst English speakers. In early 2002, the English-language ruby-talk mailing list was receiving more messages than the Japanese-language ruby-list, demonstrating Ruby's increasing popularity in the non-Japanese speaking world.


=== Ruby 1.8 and 1.9 ===
Ruby 1.8 was initially released August 2003, was stable for a long time, and was retired June 2013. Although deprecated, there is still code based on it. Ruby 1.8 is only partially compatible with Ruby 1.9.
Ruby 1.8 has been the subject of several industry standards. The language specifications for Ruby were developed by the Open Standards Promotion Center of the Information-Technology Promotion Agency (a Japanese government agency) for submission to the Japanese Industrial Standards Committee (JISC) and then to the International Organization for Standardization (ISO). It was accepted as a Japanese Industrial Standard (JIS X 3017) in 2011 and an international standard (ISO/IEC 30170) in 2012.Around 2005, interest in the Ruby language surged in tandem with Ruby on Rails, a web framework written in Ruby. Rails is frequently credited with increasing awareness of Ruby.Effective with Ruby 1.9.3, released October 31, 2011, Ruby switched from being dual-licensed under the Ruby License and the GPL to being dual-licensed under the Ruby License and the two-clause BSD license. Adoption of 1.9 was slowed by changes from 1.8 that required many popular third party gems to be rewritten. Ruby 1.9 introduces many significant changes over the 1.8 series. Examples include:
block local variables (variables that are local to the block in which they are declared)
an additional lambda syntax: f = ->(a,b) { puts a + b }
an additional Hash literal syntax using colons for symbol keys: {symbol_key: "value"} == {:symbol_key => "value"}
per-string character encodings are supported
new socket API (IPv6 support)
require_relative import security


=== Ruby 2 ===
Ruby 2.0 was intended to be fully backward compatible with Ruby 1.9.3. As of the official 2.0.0 release on February 24, 2013, there were only five known (minor) incompatibilities. Ruby 2.0 added several new features, including:

Method keyword arguments
A new method, Module#prepend, to extend a class
A new literal to create an array of symbols
New API for lazy evaluation of Enumerables
A new convention of using #to_h to convert objects to HashesStarting with 2.1.0, Ruby's versioning policy changed to be more similar to semantic versioning.Ruby 2.2.0 includes speed-ups, bugfixes, and library updates and removes some deprecated APIs. Most notably, Ruby 2.2.0 introduces changes to memory handling – an incremental garbage collector, support for garbage collection of symbols and the option to compile directly against jemalloc. It also contains experimental support for using vfork(2) with system() and spawn(), and added support for the Unicode 7.0 specification. Since version 2.2.1, Ruby MRI performance on PowerPC64 was improved. Features that were made obsolete or removed include callcc, the DL library, Digest::HMAC, lib/rational.rb, lib/complex.rb, GServer, Logger::Application as well as various C API functions.Ruby 2.3.0 includes many performance improvements, updates, and bugfixes including changes to Proc#call, Socket and IO use of exception keywords, Thread#name handling, default passive Net::FTP connections, and Rake being removed from stdlib. Other notable changes include:

The ability to mark all string literals as frozen by default with a consequently large performance increase in string operations.
Hash comparison to allow direct checking of key/value pairs instead of just keys.
A new safe navigation operator &. that can ease nil handling (e.g. instead of if obj && obj.foo && obj.foo.bar, we can use if obj&.foo&.bar).
The did_you_mean gem is now bundled by default and required on startup to automatically suggest similar name matches on a NameError or NoMethodError.
Hash#dig and Array#dig to easily extract deeply nested values (e.g. given profile = { social: { wikipedia: { name: 'Foo Baz' } } }, the value Foo Baz can now be retrieved by profile.dig(:social, :wikipedia, :name)).
.grep_v(regexp) which will match all negative examples of a given regular expression in addition to other new features.Ruby 2.4.0 includes performance improvements to hash table, Array#max, Array#min, and instance variable access. Other notable changes include:

Binding#irb: Start a REPL session similar to binding.pry
Unify Fixnum and Bignum into Integer class
String supports Unicode case mappings, not just ASCII
A new method, Regexp#match?, which is a faster boolean version of Regexp#match
Thread deadlock detection now shows threads with their backtrace and dependencyA few notable changes in Ruby 2.5.0 include rescue and ensure statements automatically use a surrounding do-end block (less need for extra begin-end blocks), method-chaining with yield_self, support for branch coverage and method coverage measurement, and easier Hash transformations with Hash#slice and Hash#transform_keys On top of that come a lot of performance improvements like faster block passing (3 times faster), faster Mutexes, faster ERB templates and improvements on some concatenation methods.
A few notable changes in Ruby 2.6.0 include an experimental just-in-time compiler (JIT), and RubyVM::AbstractSyntaxTree (experimental).
A few notable changes in Ruby 2.7.0 include pattern Matching (experimental), REPL improvements, a compaction GC, and separation of positional and keyword arguments.


=== Ruby 3 ===
Ruby 3.0.0 was released on Christmas Day in 2020. It is known as Ruby 3x3 which means that programs would run three times faster in Ruby 3.0 comparing to Ruby 2.0. and some had already implemented in intermediate releases on the road from 2 to 3. To achieve 3x3, Ruby 3 comes with MJIT, and later YJIT, Just-In-Time Compilers, to make programs faster, although they are described as experimental and remain disabled by default (enabled by flags at runtime).
Another goal of Ruby 3.0 is to improve concurrency and two more utilities Fibre Scheduler, and experimental Ractor facilitate the goal. Ractor is light-weight and thread-safe as it is achieved by exchanging messages rather than shared objects.
Ruby 3.0 introduces RBS language to describe the types of Ruby programs for static analysis. It is separated from general Ruby programs.
There are some syntax enhancements and library changes in Ruby 3.0 as well.Ruby 3.1 was released on Christmas Day in 2021. It includes YJIT, a new, experimental, Just-In-Time Compiler developed by Shopify, to enhance the performance of real world business applications. A new debugger is also included. There are some syntax enhancements and other improvements in this release. Network libraries for FTP, SMTP, IMAP, and POP are moved from default gems to bundled gems.Ruby 3.2 was released on Christmas Day in 2022. It brings support for being run inside of a WebAssembly environment via a WASI interface. Regular expressions also receives some improvements, including a faster, memoized matching algorithm to protect against certain ReDoS attacks, and configurable timeouts for regular expression matching. Additional debugging and syntax features are also included in this release, which include syntax suggestion, as well as error highlighting. The MJIT compiler has been re-implemented as a standard library module, while the YJIT, a Rust-based JIT compiler now supports more architectures on Linux.
Ruby 3.3 was released on December 25, 2023. Ruby 3.3 introduces significant enhancements and performance improvements to the language. Key features include the introduction of the Prism parser for portable and maintainable parsing, the addition of the pure-Ruby JIT compiler RJIT, and major performance boosts in the YJIT compiler. Additionally, improvements in memory usage, the introduction of an M:N thread scheduler, and updates to the standard library contribute to a more efficient and developer-friendly Ruby ecosystem.


== Semantics and philosophy ==
Matsumoto has said that Ruby is designed for programmer productivity and fun, following the principles of good user interface design. At a Google Tech Talk in 2008 he said, "I hope to see Ruby help every programmer in the world to be productive, and to enjoy programming, and to be happy. That is the primary purpose of Ruby language." He stresses that systems design needs to emphasize human, rather than computer, needs:

Often people, especially computer engineers, focus on the machines. They think, "By doing this, the machine will run fast. By doing this, the machine will run more effectively. By doing this, the machine will something something something." They are focusing on machines. But in fact we need to focus on humans, on how humans care about doing programming or operating the application of the machines. We are the masters. They are the slaves.

Matsumoto has said his primary design goal was to make a language that he himself enjoyed using, by minimizing programmer work and possible confusion. He has said that he had not applied the principle of least astonishment (POLA) to the design of Ruby; in a May 2005 discussion on the newsgroup comp.lang.ruby, Matsumoto attempted to distance Ruby from POLA, explaining that because any design choice will be surprising to someone, he uses a personal standard in evaluating surprise. If that personal standard remains consistent, there would be few surprises for those familiar with the standard.Matsumoto defined it this way in an interview:

Everyone has an individual background. Someone may come from Python, someone else may come from Perl, and they may be surprised by different aspects of the language. Then they come up to me and say, 'I was surprised by this feature of the language, so Ruby violates the principle of least surprise.' Wait. Wait. The principle of least surprise is not for you only. The principle of least surprise means principle of least my surprise. And it means the principle of least surprise after you learn Ruby very well. For example, I was a C++ programmer before I started designing Ruby. I programmed in C++ exclusively for two or three years. And after two years of C++ programming, it still surprises me.

Ruby is object-oriented: every value is an object, including classes and instances of types that many other languages designate as primitives (such as integers, booleans, and "null"). Because everything in Ruby is an object, everything in Ruby has certain built-in abilities called methods. Every function is a method and methods are always called on an object. Methods defined at the top level scope become methods of the Object class. Since this class is an ancestor of every other class, such methods can be called on any object. They are also visible in all scopes, effectively serving as "global" procedures. Ruby supports inheritance with dynamic dispatch, mixins and singleton methods (belonging to, and defined for, a single instance rather than being defined on the class). Though Ruby does not support multiple inheritance, classes can import modules as mixins.
Ruby has been described as a multi-paradigm programming language: it allows procedural programming (defining functions/variables outside classes makes them part of the root, 'self' Object), with object orientation (everything is an object) or functional programming (it has anonymous functions, closures, and continuations; statements all have values, and functions return the last evaluation). It has support for introspection, reflective programming, metaprogramming, and interpreter-based threads. Ruby features dynamic typing, and supports parametric polymorphism.
According to the Ruby FAQ, the syntax is similar to Perl's and the semantics are similar to Smalltalk's, but the design philosophy differs greatly from Python's.


== Features ==
Thoroughly object-oriented with inheritance, mixins and metaclasses
Dynamic typing and duck typing
Everything is an expression (even statements) and everything is executed imperatively (even declarations)
Succinct and flexible syntax that minimizes syntactic noise and serves as a foundation for domain-specific languages
Dynamic reflection and alteration of objects to facilitate metaprogramming
Lexical closures, iterators and generators, with a block syntax
Literal notation for arrays, hashes, regular expressions and symbols
Embedding code in strings (interpolation)
Default arguments
Four levels of variable scope (global, class, instance, and local) denoted by sigils or the lack thereof
Garbage collection
First-class continuations
Strict boolean coercion rules (everything is true except false and nil)
Exception handling
Operator overloading
Built-in support for rational numbers, complex numbers and arbitrary-precision arithmetic
Custom dispatch behavior (through method_missing and const_missing)
Native threads and cooperative fibers (fibers are a 1.9/YARV feature)
Support for Unicode and multiple character encodings.
Native plug-in API in C
Interactive Ruby Shell, an interactive command-line interpreter that can be used to test code quickly (REPL)
Centralized package management through RubyGems
Implemented on all major platforms
Large standard library, including modules for YAML, JSON, XML, CGI, OpenSSL, HTTP, FTP, RSS, curses, zlib and Tk
Just-in-time compilation


== Syntax ==

The syntax of Ruby is broadly similar to that of Perl and Python. Class and method definitions are signaled by keywords, whereas code blocks can be defined by either keywords or braces. In contrast to Perl, variables are not obligatorily prefixed with a sigil. When used, the sigil changes the semantics of scope of the variable. For practical purposes there is no distinction between expressions and statements. Line breaks are significant and taken as the end of a statement; a semicolon may be equivalently used. Unlike Python, indentation is not significant.
One of the differences from Python and Perl is that Ruby keeps all of its instance variables completely private to the class and only exposes them through accessor methods (attr_writer, attr_reader, etc.). Unlike the "getter" and "setter" methods of other languages like C++ or Java, accessor methods in Ruby can be created with a single line of code via metaprogramming; however, accessor methods can also be created in the traditional fashion of C++ and Java. As invocation of these methods does not require the use of parentheses, it is trivial to change an instance variable into a full function, without modifying a single line of calling code or having to do any refactoring achieving similar functionality to C# and VB.NET property members.
Python's property descriptors are similar, but come with a trade-off in the development process. If one begins in Python by using a publicly exposed instance variable, and later changes the implementation to use a private instance variable exposed through a property descriptor, code internal to the class may need to be adjusted to use the private variable rather than the public property. Ruby's design forces all instance variables to be private, but also provides a simple way to declare set and get methods. This is in keeping with the idea that in Ruby, one never directly accesses the internal members of a class from outside the class; rather, one passes a message to the class and receives a response.


== Implementations ==


=== Matz's Ruby interpreter ===
The original Ruby interpreter is often referred to as Matz's Ruby Interpreter or MRI. This implementation is written in C and uses its own Ruby-specific virtual machine.
The standardized and retired Ruby 1.8 implementation was written in C, as a single-pass interpreted language.Starting with Ruby 1.9, and continuing with Ruby 2.x and above, the official Ruby interpreter has been YARV ("Yet Another Ruby VM"), and this implementation has superseded the slower virtual machine used in previous releases of MRI.


=== Alternative implementations ===
As of 2018, there are a number of alternative implementations of Ruby, including JRuby, Rubinius, and mruby. Each takes a different approach, with JRuby and Rubinius providing just-in-time compilation and mruby also providing ahead-of-time compilation.
Ruby has three major alternative implementations:

JRuby, a mixed Java and Ruby implementation that runs on the Java virtual machine. JRuby currently targets Ruby 3.1.x.
TruffleRuby, a Java implementation using the Truffle language implementation framework with GraalVM
Rubinius, a C++ bytecode virtual machine that uses LLVM to compile to machine code at runtime. The bytecode compiler and most core classes are written in pure Ruby. Rubinius currently targets Ruby 2.3.1.Other Ruby implementations include:

MagLev, a Smalltalk implementation that runs on GemTalk Systems' GemStone/S VM
mruby, an implementation designed to be embedded into C code, in a similar vein to Lua. It is currently being developed by Yukihiro Matsumoto and others
RGSS, or Ruby Game Scripting System, a proprietary implementation that is used by the RPG Maker series of software for game design and modification of the RPG Maker engine
julializer, a transpiler (partial) from Ruby to Julia. It can be used for a large speedup over e.g. Ruby or JRuby implementations (may only be useful for numerical code).
Topaz, a Ruby implementation written in Python
Opal, a web-based interpreter that compiles Ruby to JavaScriptOther now defunct Ruby implementations were:

MacRuby, a Mac OS X implementation on the Objective-C runtime. Its iOS counterpart is called RubyMotion
IronRuby an implementation on the .NET Framework
Cardinal, an implementation for the Parrot virtual machine
Ruby Enterprise Edition, often shortened to ree, an implementation optimized to handle large-scale Ruby on Rails projects
HotRuby, a JavaScript and ActionScript implementation of the Ruby programming languageThe maturity of Ruby implementations tends to be measured by their ability to run the Ruby on Rails (Rails) framework, because it is complex to implement and uses many Ruby-specific features. The point when a particular implementation achieves this goal is called "the Rails singularity". The reference implementation, JRuby, and Rubinius are all able to run Rails unmodified in a production environment.


=== Platform support ===
Matsumoto originally developed Ruby on the 4.3BSD-based Sony NEWS-OS 3.x, but later migrated his work to SunOS 4.x, and finally to Linux. By 1999, Ruby was known to work across many different operating systems. Modern Ruby versions and implementations are available on all major desktop, mobile and server-based operating systems. Ruby is also supported across a number of cloud hosting platforms like Jelastic, Heroku, Google Cloud Platform and others.
Tools such as RVM and RBEnv, facilitate installation and partitioning of multiple ruby versions, and multiple 'gemsets' on one machine.


== Repositories and libraries ==
RubyGems is Ruby's package manager. A Ruby package is called a "gem" and can be installed via the command line. Most gems are libraries, though a few exist that are applications, such as IDEs. There are over 100,000 Ruby gems hosted on RubyGems.org.Many new and existing Ruby libraries are hosted on GitHub, a service that offers version control repository hosting for Git.
The Ruby Application Archive, which hosted applications, documentation, and libraries for Ruby programming, was maintained until 2013, when its function was transferred to RubyGems.


== See also ==
Comparison of programming languages
Metasploit Project
Why's (poignant) Guide to Ruby
Crystal (programming language)
Ruby on Rails


== References ==


== Further reading ==


== External links ==

Official website
Ruby documentation
Ruby at Curlie
