# Swift

Swift is a high-level general-purpose, multi-paradigm, compiled programming language developed by Apple Inc. and the open-source community. Swift compiles to machine code, as it is an LLVM-based compiler. Swift was first released in June 2014, and the Swift toolchain has shipped in Xcode since version 6, released in 2014.
Apple intended Swift to support many core concepts associated with Objective-C, notably dynamic dispatch, widespread late binding, extensible programming, and similar features, but in a "safer" way, making it easier to catch software bugs; Swift has features addressing some common programming errors like null pointer dereferencing and provides syntactic sugar to help avoid the pyramid of doom. Swift supports the concept of protocol extensibility, an extensibility system that can be applied to types, structs and classes, which Apple promotes as a real change in programming paradigms they term "protocol-oriented programming" (similar to traits and type classes).Swift was introduced at Apple's 2014 Worldwide Developers Conference (WWDC). It underwent an upgrade to version 1.2 during 2014 and a major upgrade to Swift 2 at WWDC 2015. Initially a proprietary language, version 2.2 was made open-source software under the Apache License 2.0 on December 3, 2015, for Apple's platforms and Linux.Through version 3.0 the syntax of Swift went through significant evolution, with the core team making source stability a focus in later versions. In the first quarter of 2018 Swift surpassed Objective-C in measured popularity.Swift 4.0, released in 2017, introduced several changes to some built-in classes and structures. Code written with previous versions of Swift can be updated using the migration functionality built into Xcode. Swift 5, released in March 2019, introduced a stable binary interface on Apple platforms, allowing the Swift runtime to be incorporated into Apple operating systems. It is source compatible with Swift 4.Swift 5.1 was officially released in September 2019. Swift 5.1 builds on the previous version of Swift 5 by extending the stable features of the language to compile-time with the introduction of module stability. The introduction of module stability makes it possible to create and share binary frameworks that will work with future releases of Swift.Swift 5.5, officially announced by Apple at the 2021 WWDC, significantly expands language support for concurrency and asynchronous code, notably introducing a unique version of the actor model.Swift 5.9, was released in September 2023 and includes a macro system, generic parameter packs, and ownership features like the new consume operator.The current version, Swift 5.10, was released in March 2024. This version improves the language's concurrency model, allowing for full data isolation to prevent data races. It is also the last release before Swift 6.


== History ==
Development of Swift started in July 2010 by Chris Lattner, with the eventual collaboration of many other programmers at Apple. Swift was motivated by the need for a replacement for Apple's earlier programming language Objective-C, which had been largely unchanged since the early 1980s and lacked modern language features. Swift took language ideas "from Objective-C, Rust, Haskell, Ruby, Python, C#, CLU, and far too many others to list". On June 2, 2014, the Apple Worldwide Developers Conference (WWDC) application became the first publicly released app written with Swift. A beta version of the programming language was released to registered Apple developers at the conference, but the company did not promise that the final version of Swift would be source code compatible with the test version. Apple planned to make source code converters available if needed for the full release.The Swift Programming Language, a free 500-page manual, was also released at WWDC, and is available on the Apple Books Store and the official website.Swift reached the 1.0 milestone on September 9, 2014, with the Gold Master of Xcode 6.0 for iOS. Swift 1.1 was released on October 22, 2014, alongside the launch of Xcode 6.1. Swift 1.2 was released on April 8, 2015, along with Xcode 6.3. Swift 2.0 was announced at WWDC 2015, and was made available for publishing apps in the App Store on September 21, 2015. Swift 3.0 was released on September 13, 2016. Swift 4.0 was released on September 19, 2017. Swift 4.1 was released on March 29, 2018.Swift won first place for Most Loved Programming Language in the Stack Overflow Developer Survey 2015 and second place in 2016.On December 3, 2015, the Swift language, supporting libraries, debugger, and package manager were open-sourced under the Apache 2.0 license with a Runtime Library Exception, and Swift.org was created to host the project. The source code is hosted on GitHub, where it is easy for anyone to get the code, build it themselves, and even create pull requests to contribute code back to the project.
In December 2015, IBM announced its Swift Sandbox website, which allows developers to write Swift code in one pane and display output in another. The Swift Sandbox was deprecated in January 2018.During the WWDC 2016, Apple announced an iPad exclusive app, named Swift Playgrounds, intended to teach people how to code in Swift. The app is presented in a 3D video game-like interface which provides feedback when lines of code are placed in a certain order and executed.In January 2017, Chris Lattner announced his departure from Apple for a new position with Tesla Motors, with the Swift project lead role going to team veteran Ted Kremenek.During WWDC 2019, Apple announced SwiftUI with Xcode 11, which provides a framework for declarative UI structure design across all Apple platforms.Official downloads for the Ubuntu distribution of Linux have been available since Swift 2.2, with more distros added since Swift 5.2.4, CentOS and Amazon Linux. There is an unofficial SDK and native toolchain package for Android too.


=== Platforms ===
The platforms Swift supports are Apple's operating systems (Darwin, iOS, iPadOS, macOS, tvOS, watchOS), Linux, Windows, and Android.A key aspect of Swift's design is its ability to interoperate with the huge body of existing Objective-C code developed for Apple products over the previous decades, such as Cocoa and the Cocoa Touch frameworks. On Apple platforms, it links with the Objective-C runtime library, which allows C, Objective-C, C++ and Swift code to run within one program.


=== Version history ===


== Features ==
Swift is a general purpose programming language that employs modern programming-language theory concepts and strives to present a simple, yet powerful syntax. Swift incorporates innovations and conventions from various programming languages, with notable inspiration from Objective-C, which it replaced as the primary development language on Apple Platforms.
Swift was designed to be safe and friendly to new programmers while not sacrificing speed. By default Swift manages all memory automatically and ensures variables are always initialized before use. Array accesses are checked for out-of-bounds errors and integer operations are checked for overflow. Parameter names allow creating clear APIs. Protocols define interfaces that types may adopt, while extensions allow developers to add more function to existing types. Swift enables object-oriented programming with the support for classes, subtyping, and method overriding. Optionals allow nil values to be handled explicitly and safely. Concurrent programs can be written using async/await syntax and actors isolate shared mutable state in order to eliminate data races.


=== Basic syntax ===
Swift's syntax is similar to C-style languages. Code begins executing in the global scope by default. Alternatively, the @main attribute can be applied a structure, class, or enumeration declaration to indicate that it contains the program's entry point.
Swift's "Hello, World!" program is:The print(_:separator:terminator:) function used here is included in Swift's standard library, which is available to all programs without the need to import external modules. Statements in Swift don't have to end with a semicolon, however semicolons are required to separate multiple statements written on the same line. Single-line comments begin with // and continue until the end of the current line. Multiline comments are contained by /* and */ characters.
Constants are declared with the let keyword and variables with the var keyword. Values must be initialized before they are read. Values may infer their type based on the type of the provided initial value. If the initial value is set after the value's declaration, a type must be declared explicitly.Control flow in Swift is managed with if-else, guard, and switch statements, along with while and for-in loops.
If statements take a boolean parameter and execute the body of the if statement if the condition is true, otherwise it executes the optional else body. if-let syntax provides syntactic sugar for checking for the existence of an optional value and unwrapping it at the same time.Functions are defined with the func keyword. Function parameters may have names which allow function calls to read like phrases. An underscore before the parameter name allows the argument label to be omitted from the call site. Tuples can be used by functions to return multiple pieces of data at once.Functions, and anonymous functions known as closures, can be assigned to properties and passed around the program like any other value.guard statements require that the given condition is true before continuing on past the guard statement, otherwise the body of the provided else clause is run. The else clause must exit control of the code block in which the guard statement appears. guard statements are useful for ensuring that certain requirements are met before continuing on with program execution. In particular they can be used to create an unwrapped version of an optional value that is guaranteed to be non-nil for the remainder of the enclosing scope.switch statements compare a value with multiple potential values and then executes an associated code block. switch statements must be made exhaustive, either by including cases for all possible values or by including a default case which is run when the provided value doesn't match any of the other cases. switch cases do not implicitly fall through, although they may explicitly do so with the fallthrough keyword. Pattern matching can be used in various ways inside switch statements. Here is an example of an integer being matched against a number of potential ranges:for-in loops iterate over a sequence of values:while loops iterate as long as the given boolean condition evaluates to true:


=== Closure support ===
Swift supports closures, which are self-contained blocks of functionality that can be passed around and used in code, and can also be used as anonymous functions. Here are some examples:

Closures can be assigned to variables and constants, and can be passed into other functions or closures as parameters. Single-expression closures may drop the return keyword.
Swift also has a trailing closure syntax, which allows the closure to be written after the end of the function call instead of within the function's parameter list. Parentheses can be omitted altogether if the closure is the function's only parameter:

Starting from version 5.3, Swift supports multiple trailing closures:
Swift will provide shorthand argument names for inline closures, removing the need to explicitly name all of the closures parameters. Arguments can be referred to with the names $0, $1, $2, and so on:Closures may capture values from their surrounding scope. The closure will refer to this captured value for as long as the closure exists:


=== String support ===
The Swift standard library includes unicode-compliant String and Character types. String values can be initialized with a String literal, a sequence of characters surrounded by double quotation marks. Strings can be concatenated with the + operator:

String interpolation allows for the creation of a new string from other values and expressions. Values written between parentheses preceded by a \ will be inserted into the enclosing string literal:A for-in loop can be used to iterate over the characters contained in a string:
When the Foundation framework is imported Swift invisibly bridges the String type to NSString, the String class commonly used in Objective-C.


=== Callable objects ===


=== Access control ===
Swift supports five access control levels for symbols: open, public, internal, fileprivate, and private. Unlike many object-oriented languages, these access controls ignore inheritance hierarchies: private indicates that a symbol is accessible only in the immediate scope, fileprivate indicates it is accessible only from within the file, internal indicates it is accessible within the containing module, public indicates it is accessible from any module, and open (only for classes and their methods) indicates that the class may be subclassed outside of the module.


=== Optionals and chaining ===
An important feature in Swift is option types, which allow references or values to operate in a manner similar to the common pattern in C, where a pointer may either refer to a specific value or no value at all. This implies that non-optional types cannot result in a null-pointer error; the compiler can ensure this is not possible.
Optional types are created with the Optional enum. To make an Integer that is nullable, one would use a declaration similar to var optionalInteger: Optional<Int>. As in C#, Swift also includes syntactic sugar for this, allowing one to indicate a variable is optional by placing a question mark after the type name, var optionalInteger: Int?. Variables or constants that are marked optional either have a value of the underlying type or are nil. Optional types wrap the base type, resulting in a different instance. String and String? are fundamentally different types, the former is of type String while the latter is an Optional that may be holding some String value.
To access the value inside, assuming it is not nil, it must be unwrapped to expose the instance inside. This is performed with the ! operator:

In this case, the ! operator unwraps anOptionalInstance to expose the instance inside, allowing the method call to be made on it. If anOptionalInstance is nil, a null-pointer error occurs, terminating the program. This is known as force unwrapping. Optionals may be safely unwrapped using optional chaining which first tests whether the instance is nil, and then unwrap it if it is non-null:

In this case the runtime calls someMethod only if anOptionalInstance is not nil, suppressing the error. A ? must be placed after every optional property. If any of these properties are nil the entire expression evaluates as nil. The origin of the term chaining comes from the more common case where several method calls/getters are chained together. For instance:

can be reduced to:

Swift's use of optionals allows the compiler to use static dispatch because the unwrapping action is called on a defined instance (the wrapper), versus occurring in a runtime dispatch system.


=== Value types ===
In many object-oriented languages, objects are represented internally in two parts. The object is stored as a block of data placed on the heap, while the name (or "handle") to that object is represented by a pointer. Objects are passed between methods by copying the value of the pointer, allowing the same underlying data on the heap to be accessed by anyone with a copy. In contrast, basic types like integers and floating-point values are represented directly; the handle contains the data, not a pointer to it, and that data is passed directly to methods by copying. These styles of access are termed pass-by-reference in the case of objects, and pass-by-value for basic types.
Both concepts have their advantages and disadvantages. Objects are useful when the data is large, like the description of a window or the contents of a document. In these cases, access to that data is provided by copying a 32- or 64-bit value, versus copying an entire data structure. However, smaller values like integers are the same size as pointers (typically both are one word), so there is no advantage to passing a pointer, versus passing the value.
Swift offers built-in support for objects using either pass-by-reference or pass-by-value semantics, the former using the class declaration and the latter using struct. Structs in Swift have almost all the same features as classes: methods, implementing protocols and using the extension mechanisms. For this reason, Apple terms all data generically as instances, versus objects or values. Structs do not support inheritance, however.The programmer is free to choose which semantics are more appropriate for each data structure in the application. Larger structures like windows would be defined as classes, allowing them to be passed around as pointers. Smaller structures, like a 2D point, can be defined as structs, which will be pass-by-value and allow direct access to their internal data with no indirection or reference counting. The performance improvement inherent to the pass-by-value concept is such that Swift uses these types for almost all common data types, including Int and Double, and types normally represented by objects, like String and Array. Using value types can result in significant performance improvements in user applications as well.Array, Dictionary, and Set all utilize copy on write so that their data are copied only if and when the program attempts to change a value in them. This means that the various accessors have what is in effect a pointer to the same data storage. So while the data is physically stored as one instance in memory, at the level of the application, these values are separate and physical separation is enforced by copy on write only if needed.


=== Extensions ===
Extensions add new functionality to an existing type, without the need to subclass or even have access to the original source code. Extensions can add new methods, initializers, computed properties, subscripts, and protocol conformances. An example might be to add a spell checker to the base String type, which means all instances of  String in the program gain the ability to spell-check. The system is also widely used as an organizational technique, allowing related code to be gathered into library-like extensions.

Extensions are declared with the extension keyword.


=== Protocol-oriented programming ===
Protocols promise that a particular type implements a set of methods or properties, meaning that other instances in the system can call those methods on any instance implementing that protocol. This is often used in modern object-oriented languages as a substitute for multiple inheritance, although the feature sets are not entirely similar.
In Objective-C, and most other languages implementing the protocol concept, it is up to the programmer to ensure that the required methods are implemented in each class. Swift adds the ability to add these methods using extensions, and to use generic programming (generics) to implement them. Combined, these allow protocols to be written once and support a wide variety of instances. Also, the extension mechanism can be used to add protocol conformance to an object that does not list that protocol in its definition.For example, a protocol might be declared called Printable, which ensures that instances that conform to the protocol implement a description property and a printDetails() method requirement:

This protocol can now be adopted by other types:

Extensions can be used to add protocol conformance to types. Protocols themselves can also be extended to provide default implementations of their requirements. Adopters may define their own implementations, or they may use the default implementation:
In Swift, like many modern languages supporting interfaces, protocols can be used as types, which means variables and methods can be defined by protocol instead of their specific type:

It does not matter what concrete type of someSortOfPrintableInstance is, the compiler will ensure that it conforms to the protocol and thus this code is safe. This syntax also means that collections can be based on protocols also, like let printableArray = [any Printable].
Both extensions and protocols are used extensively in Swift's standard library; in Swift 5.9, approximately 1.2 percent of all symbols within the standard library were protocols, and another 12.3 percent were protocol requirements or default implementations. For instance, Swift uses extensions to add the Equatable protocol to many of their basic types, like Strings and Arrays, allowing them to be compared with the == operator. The Equatable protocol also defines this default implementation:

This function defines a method that works on any instance conforming to Equatable, providing a not equals operator. Any instance, class or struct, automatically gains this implementation simply by conforming to Equatable.
Protocols, extensions, and generics can be combined to create sophisticated APIs. For example, constraints allow types to conditionally adopt protocols or methods based on the characteristics of the adopting type. A common use case may be adding a method on collection types only when the elements contained within the collection are Equatable:


=== Concurrency ===
Swift 5.5 introduced structured concurrency into the language. Structured concurrency uses Async/await syntax similar to Kotlin, JavaScript, and Rust. An async function is defined with the async keyword after the parameter list. When calling an async function the await keyword must be written before the function to indicate that execution will potentially suspend while calling function. While a function is suspended the program may run some other concurrent function in the same program. This syntax allows programs to clearly call out potential suspension points and avoid a version of the Pyramid of doom (programming) caused by the previously widespread use of closure callbacks. The async let syntax allows multiple functions to run in parallel. await is again used to mark the point at which the program will suspend to wait for the completion of the async functions called earlier.Tasks and TaskGroups can be created explicitly to create a dynamic number of child tasks during runtime:Swift uses the Actor model to isolate mutable state, allowing different tasks to mutate shared state in a safe manner. Actors are declared with the actor keyword and are reference types, like classes. Only one task may access the mutable state of an actor at the same time. Actors may access and mutate their own internal state freely, but code running in separate tasks must mark each access with the await keyword to indicate that the code may suspend until other tasks finish accessing the actor's state.


=== Libraries, runtime, development ===
On Apple systems, Swift uses the same runtime as the extant Objective-C system, but requires iOS 7 or macOS 10.9 or higher. It also depends on Grand Central Dispatch. Swift and Objective-C code can be used in one program, and by extension, C and C++ also. Beginning in Swift 5.9, C++ code can be used directly from Swift code. In the case of Objective-C, Swift has considerable access to the object model, and can be used to subclass, extend and use Objective-C code to provide protocol support. The converse is not true: a Swift class cannot be subclassed in Objective-C.To aid development of such programs, and the re-use of extant code, Xcode 6 and higher offers a semi-automated system that builds and maintains a bridging header to expose Objective-C code to Swift. This takes the form of an additional header file that simply defines or imports all of the Objective-C symbols that are needed by the project's Swift code. At that point, Swift can refer to the types, functions, and variables declared in those imports as though they were written in Swift. Objective-C code can also use Swift code directly, by importing an automatically maintained header file with Objective-C declarations of the project's Swift symbols. For instance, an Objective-C file in a mixed project called "MyApp" could access Swift classes or functions with the code #import "MyApp-Swift.h". Not all symbols are available through this mechanism, however—use of Swift-specific features like generic types, non-object optional types, sophisticated enums, or even Unicode identifiers may render a symbol inaccessible from Objective-C.Swift also has limited support for attributes, metadata that is read by the development environment, and is not necessarily part of the compiled code. Like Objective-C, attributes use the @ syntax, but the currently available set is small. One example is the @IBOutlet attribute, which marks a given value in the code as an outlet, available for use within Interface Builder (IB). An outlet is a device that binds the value of the on-screen display to an object in code.
On non-Apple systems, Swift does not depend on an Objective-C runtime or other Apple system libraries; a set of Swift "Corelib" implementations replace them. These include a "swift-corelibs-foundation" to stand in for the Foundation Kit, a "swift-corelibs-libdispatch" to stand in for the Grand Central Dispatch, and an "swift-corelibs-xctest" to stand in for the XCTest APIs from Xcode.As of 2019, with Xcode 11, Apple has also added a major new UI paradigm called SwiftUI.  SwiftUI replaces the older Interface Builder paradigm with a new declarative development paradigm.


=== Memory management ===
Swift uses Automatic Reference Counting (ARC) to manage memory. Every instance of a class or closure maintains a reference count which keeps a running tally of the number of references the program is holding for on to. When this count reaches 0 the instance is deallocated. This automatic deallocation removes the need for a garbage collector as instances are deallocated as soon as they are no longer needed.
A strong reference cycle can occur if two instances each strongly reference each other (e.g. A references B, B references A). Since neither instances reference count can ever reach zero neither is ever deallocated, resulting in a memory leak. Swift provides the keywords weak and unowned to prevent strong reference cycles. These keywords allow an instance to be referenced without incrementing its reference count. weak references must be optional variables, since they can change and become nil. Attempting to access an unowned value that has already been deallocated results in a runtime error.

A closure within a class can also create a strong reference cycle by capturing self references. Self references to be treated as weak or unowned can be indicated using a capture list.


=== Debugging ===
A key element of the Swift system is its ability to be cleanly debugged and run within the development environment, using a read–eval–print loop (REPL), giving it interactive properties more in common with the scripting abilities of Python than traditional system programming languages. The REPL is further enhanced with playgrounds, interactive views running within the Xcode environment or Playgrounds app that respond to code or debugger changes on-the-fly. Playgrounds allow programmers to add in Swift code along with markdown documentation. Programmers can step through code and add breakpoints using LLDB either in a console or an IDE like Xcode.


== Comparisons to other languages ==
Swift is considered a C family programming language and is similar to C in various ways:

Most operators in C also appear in Swift, although some operators such as + have slightly different behavior. For example, in Swift, + traps on overflow, whereas &+ is used to denote the C-like behavior of wrapping on overflow.
Curly braces are used to group statements.
Variables are assigned using an equals sign, but compared using two consecutive equals signs. A new identity operator, ===, is provided to check if two data elements refer to the same object.
Control statements while, if, and switch are similar, but have extended functions, e.g., a switch that takes non-integer cases, while and if supporting pattern matching and conditionally unwrapping optionals, for uses the for i in 1...10 syntax.
Square brackets are used with arrays, both to declare them and to get a value at a given index in one of them.It also has similarities to Objective-C:

Basic numeric types: Int, UInt, Float, Double
Class methods are inherited, like instance methods; self in class methods is the class the method was called on.
Similar for...in enumeration syntax.Differences from Objective-C include:

Statements need not end with semicolons (;), though these must be used to allow more than one statement on one line.
No header files.
Uses type inference.
Generic programming.
Functions are first-class objects.
Enumeration cases can have associated data (algebraic data types).
Operators can be redefined for classes (operator overloading), and new operators can be defined.
Strings fully support Unicode. Most Unicode characters can be used in either identifiers or operators.
No exception handling. Swift 2 introduces a different and incompatible error-handling model.
Several features of earlier C-family languages that are easy to misuse have been removed:
Pointers are not exposed by default. There is no need for the programmer to keep track of and mark names for referencing or dereferencing.
Assignments return no value. This prevents the common error of writing i = 0 instead of i == 0 by throwing a compile-time error.
No need to use break statements in switch blocks. Individual cases do not fall through to the next case unless the fallthrough statement is used.
Variables and constants are always initialized and array bounds are always checked.
Integer overflows, which result in undefined behavior for signed integers in C, are trapped as a run-time error in Swift. Programmers can choose to allow overflows by using the special arithmetical operators &+, &-, &*, &/ and &%. The properties min and max are defined in Swift for all integer types and can be used to safely check for potential overflows, versus relying on constants defined for each type in external libraries.
The one-statement form of if and while, which allows for the omission of braces around the statement, is unsupported.
C-style enumeration for (int i = 0; i < c; i++), which is prone to off-by-one errors, is unsupported (from Swift 3 onward).
The pre- and post- increment and decrement operators (i++, --i ...) are unsupported (from Swift 3 onward), more so since C-style for statements are also unsupported from Swift 3 onward.


== Development and other implementations ==
Because Swift can run on Linux, it is sometimes also used as a server-side language. Some web frameworks have already been developed, such as IBM's Kitura (now discontinued), Perfect and Vapor.
An official "Server APIs" work group has also been started by Apple, with members of the Swift developer community playing a central role.A second free implementation of Swift that targets Cocoa, Microsoft's Common Language Infrastructure (.NET Framework, now .NET), and the Java and Android platform exists as part of the Elements Compiler from RemObjects Software.Subsets of Swift have been ported to additional platforms, such as Arduino and Mac OS 9.


== See also ==
Comparison of programming languages
Objective-C
D (programming language)
Kotlin (programming language)
Python (programming language)
Nim (programming language)


== References ==


== External links ==
Official website 
Swift at Apple Developer
Swift's source code on GitHub
Swift Example
Server-side Swift - The Vapor Framework
