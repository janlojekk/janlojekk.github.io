# Kotlin

Kotlin () is a cross-platform, statically typed, general-purpose high-level programming language with type inference. Kotlin is designed to interoperate fully with Java, and the JVM version of Kotlin's standard library depends on the Java Class Library,
but type inference allows its syntax to be more concise. Kotlin mainly targets the JVM, but also compiles to JavaScript (e.g., for frontend web applications using React) or native code via LLVM (e.g., for native iOS apps sharing business logic with Android apps). Language development costs are borne by JetBrains, while the Kotlin Foundation protects the Kotlin trademark.On 7 May 2019, Google announced that the Kotlin programming language was now its preferred language for Android app developers. Since the release of Android Studio 3.0 in October 2017, Kotlin has been included as an alternative to the standard Java compiler. The Android Kotlin compiler produces Java 8 bytecode by default (which runs in any later JVM), but lets the programmer choose to target Java 9 up to 20, for optimization, or allows for more features; has bidirectional record class interoperability support for JVM, introduced in Java 16, considered stable as of Kotlin 1.5.
Kotlin has support for the web with Kotlin/JS, either through a classic interpreter-based backend which has been declared stable since version 1.3, or an intermediate representation-based backend which has been declared stable since version 1.8. Kotlin/Native (for e.g. Apple silicon support) is considered beta since version 1.3.


== History ==
In July 2011, JetBrains unveiled Project Kotlin, a new language for the JVM, which had been under development for a year. JetBrains lead Dmitry Jemerov said that most languages did not have the features they were looking for, with the exception of Scala. However, he cited the slow compilation time of Scala as a deficiency. One of the stated goals of Kotlin is to compile as quickly as Java. In February 2012, JetBrains open sourced the project under the Apache 2 license.The name comes from Kotlin Island, near St. Petersburg. Andrey Breslav mentioned that the team decided to name it after an island, just like Java was named after the Indonesian island of Java (though Java, the programming language's name, is said to have been inspired by "java" the American slang term for coffee, which itself derives from the island name).JetBrains hoped that the new language would drive IntelliJ IDEA sales.The first commit to the Kotlin Git repository was on November 8, 2010.Kotlin 1.0 was released on February 15, 2016. This is considered to be the first officially stable release and JetBrains has committed to long-term backwards compatibility starting with this version.
At Google I/O 2017, Google announced first-class support for Kotlin on Android.Kotlin 1.2 was released on November 28, 2017. Sharing code between JVM and JavaScript platforms feature was newly added to this release (multiplatform programming is by now a beta feature upgraded from "experimental"). A full-stack demo has been made with the new Kotlin/JS Gradle Plugin.Kotlin 1.3 was released on 29 October 2018, bringing coroutines for asynchronous programming.On 7 May 2019, Google announced that the Kotlin programming language is now its preferred language for Android app developers.Kotlin 1.4 was released in August 2020, with e.g. some slight changes to the support for Apple's platforms, i.e. to the Objective-C/Swift interop.Kotlin 1.5 was released in May 2021.
Kotlin 1.6 was released in November 2021.
Kotlin 1.7 was released in June 2022, including the alpha version of the new Kotlin K2 compiler.Kotlin 1.8 was released in December 2022, 1.8.0 was released on January 11, 2023.Kotlin 1.9 was released in July 2023, 1.9.0 was released on July 6, 2023.


== Design ==
Development lead Andrey Breslav has said that Kotlin is designed to be an industrial-strength object-oriented language, and a "better language" than Java, but still be fully interoperable with Java code, allowing companies to make a gradual migration from Java to Kotlin.Semicolons are optional as a statement terminator; in most cases a newline is sufficient for the compiler to deduce that the statement has ended.Kotlin variable declarations and parameter lists have the data type come after the variable name (and with a colon separator), similar to Ada, BASIC, Pascal, TypeScript and Rust. This, according to an article from Roman Elizarov, current project lead, results in alignment of variable names and is more pleasing to eyes, especially when there are a few variable declarations in succession, and one or more of the types is too complex for type inference, or needs to be declared explicitly for human readers to understand.Variables in Kotlin can be read-only, declared with the val keyword, or mutable, declared with the var keyword.Class members are public by default, and classes themselves are final by default, meaning that creating a derived class is disabled unless the base class is declared with the open keyword.
In addition to the classes and member functions (which are equivalent to methods) of object-oriented programming, Kotlin also supports procedural programming with the use of functions.
Kotlin functions and constructors support default arguments, variable-length argument lists, named arguments, and overloading by unique signature. Class member functions are virtual, i.e. dispatched based on the runtime type of the object they are called on.
Kotlin 1.3 added support for contracts, which are stable for the standard library declarations, but still experimental for user-defined declarations. Contracts are inspired by Eiffel's design by contract programming paradigm.
Kotlin code may be compiled to JavaScript, allowing for interoperability between code written in the two languages. This can be used either to write full web applications in Kotlin, or to share code between a Kotlin backend and a JavaScript frontend.


== Syntax ==


=== Procedural programming style ===
Kotlin relaxes Java's restriction of allowing static methods and variables to exist only within a class body. Static objects and functions can be defined at the top level of the package without needing a redundant class level. For compatibility with Java, Kotlin provides a JvmName annotation which specifies a class name used when the package is viewed from a Java project. For example, @file:JvmName("JavaClassName").


=== Main entry point ===

As in C, C++, C#, Java, and Go, the entry point to a Kotlin program is a function named "main", which may be passed an array containing any command-line arguments. This is optional since Kotlin 1.3. Perl, PHP, and Unix shell–style string interpolation is supported. Type inference is also supported.


=== Extension functions ===
Similar to C#, Kotlin allows adding an extension function to any class without the formalities of creating a derived class with new functions. An extension function has access to all the public interface of a class, which it can use to create a new function interface to a target class. An extension function will appear exactly like a function of the class and will be shown in code completion inspection of class functions. For example:

By placing the preceding code in the top-level of a package, the String class is extended to include a lastChar function that was not included in the original definition of the String class.


=== Unpack arguments with spread operator ===
Similar to Python, the spread operator asterisk (*) unpacks an array's contents as individual arguments to a function, e.g:


=== Destructuring declarations ===

Destructuring declarations decompose an object into multiple variables at once, e.g. a 2D coordinate object might be destructured into two integers, x and y.
For example, the Map.Entry object supports destructuring to simplify access to its key and value fields:


=== Nested functions ===
Kotlin allows local functions to be declared inside of other functions or methods.


=== Classes are final by default ===
In Kotlin, to derive a new class from a base class type, the base class needs to be explicitly marked as "open".  This is in contrast to most object-oriented languages such as Java where classes are open by default.
Example of a base class that is open to deriving a new subclass from it:


=== Abstract classes are open by default ===

Abstract classes define abstract or "pure virtual" placeholder functions that will be defined in a derived class. Abstract classes are open by default.


=== Classes are public by default ===
Kotlin provides the following keywords to restrict visibility for top-level declaration, such as classes, and for class members: public, internal, protected, and private.
When applied to a class member:

When applied to a top-level declaration:

Example:


=== Primary constructor vs. secondary constructors ===
Kotlin supports the specification of a "primary constructor" as part of the class definition itself, consisting of an argument list following the class name. This argument list supports an expanded syntax on Kotlin's standard function argument lists that enables declaration of class properties in the primary constructor, including visibility, extensibility, and mutability attributes. Additionally, when defining a subclass, properties in super-interfaces and super-classes can be overridden in the primary constructor.

However, in cases where more than one constructor is needed for a class, a more general constructor can be defined using secondary constructor syntax, which closely resembles the constructor syntax used in most object-oriented languages like C++, C#, and Java.


=== Sealed classes ===
Sealed classes and interfaces restrict subclass hierarchies, meaning more control over the inheritance hierarchy.
Declaration of sealed interface and class:

All the subclasses of the sealed class are defined at compile time. 
No new subclasses can be added to it after the compilation of the module having the sealed class.
For example, a sealed class in a compiled jar file cannot be subclassed.


=== Data classes ===
Kotlin's data class construct defines classes whose primary purpose is storing data. This construct is similar to normal classes except that the key functions equals, toString, and hashCode are automatically generated from the class properties. In Java, such classes are expected to provide a standard assortment of functions including those. Data classes are not required to declare any methods, though each must have at least one property. A data class often is written without a body, though it is possible to give a data class any methods or secondary constructors that are valid for any other class. The data keyword is used before the class keyword to define a data class.


=== Kotlin interactive shell ===


=== Kotlin as a scripting language ===
Kotlin can also be used as a scripting language. A script is a Kotlin source file using the .kts filename extension, with executable source code at the top-level scope:

Scripts can be run by passing the -script option and the corresponding script file to the compiler.


=== Null safety ===
Kotlin makes a distinction between nullable and non-nullable data types. All nullable objects must be declared with a "?" postfix after the type name. Operations on nullable objects need special care from developers: a null-check must be performed before using the value, either explicitly, or with the aid of Kotlin's null-safe operators:

?. (the safe navigation operator) can be used to safely access a method or property of a possibly null object. If the object is null, the method will not be called and the expression evaluates to null.  Example:

?: (the null coalescing operator) is a binary operator that returns the first operand, if non-null, else the second operand. It is often referred to as the Elvis operator, due to its resemblance to an emoticon representation of Elvis Presley.


=== Lambdas ===
Kotlin provides support for higher-order functions and anonymous functions, or lambdas.

Lambdas are declared using braces, {  }. If a lambda takes parameters, they are declared within the braces and followed by the -> operator.


=== Complex "hello world" example ===


== Tools ==
Android Studio  (based on IntelliJ IDEA) has official support for Kotlin, starting from Android Studio 3.
Integration with common Java build tools is supported, including Apache Maven, Apache Ant, and Gradle.
Emacs has a Kotlin Mode in its MELPA package repository.
JetBrains also provides a plugin for Eclipse.
IntelliJ IDEA has plug-in support for Kotlin. IntelliJ IDEA 15 was the first version to bundle the Kotlin plugin in the IntelliJ Installer, and to provide Kotlin support out of the box.


== Applications ==
When Kotlin was announced as an official Android development language at Google I/O in May 2017, it became the third language fully supported for Android, after Java and C++. As of 2020, Kotlin is the most widely used language on Android, with Google estimating that 70% of the top 1,000 apps on the Play Store are written in Kotlin. Google itself has 60 apps written in Kotlin, including Maps and Drive. Many Android apps, such as Google Home, are in the process of being migrated to Kotlin, and therefore use both Kotlin and Java. Kotlin on Android is seen as beneficial for its null-pointer safety, as well as for its features that make for shorter, more readable code.In addition to its prominent use on Android, Kotlin is gaining traction in server-side development. The Spring Framework officially added Kotlin support with version 5, on 4 January 2017. To further support Kotlin, Spring has translated all its documentation to Kotlin, and added built-in support for many Kotlin-specific features such as coroutines. In addition to Spring, JetBrains has produced a Kotlin-first framework called Ktor for building web applications.In 2020, JetBrains found in a survey of developers who use Kotlin that 56% were using Kotlin for mobile apps, while 47% were using it for a web back-end. Just over a third of all Kotlin developers said that they were migrating to Kotlin from another language. Most Kotlin users were targeting Android (or otherwise on the JVM), with only 6% using Kotlin Native.


== Adoption ==
In 2018, Kotlin was the fastest growing language on GitHub, with 2.6 times more developers compared to 2017. It is the fourth most loved programming language according to the 2020 Stack Overflow Developer Survey.Kotlin was also awarded the O'Reilly Open Source Software Conference Breakout Award for 2019.Many companies / organizations have used Kotlin for backend development:

Allegro
Amazon
Atlassian
Cash App
Flux
Google
Gradle
JetBrains
Meshcloud
Norwegian Tax Administration
OLX
Pivotal
Rocket Travel
Shazam
ZalandoSome companies / organizations have used Kotlin for web development:

Barclay's Bank
Data2viz
Fritz2
JetBrainsA number of companies have publicly stated they were using Kotlin:

Basecamp
Corda, a distributed ledger developed by a consortium of well-known banks (such as Goldman Sachs, Wells Fargo, J.P. Morgan, Deutsche Bank, UBS, HSBC, BNP Paribas, and Société Générale), has over 90% Kotlin code in its codebase.
Coursera
DripStat
Duolingo
Netflix
Pinterest
Trello
Uber


== See also ==
Comparison of programming languages


== References ==
This article contains quotations from Kotlin tutorials which are released under an Apache 2.0 license.


== External links ==
Official website
