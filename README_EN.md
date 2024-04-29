![Flutter Interview](https://github.com/p0dyakov/flutter_interview/assets/80569772/68dccc7f-b4f2-4eca-932a-8f9fe5559b5f)
**Repositories:** [Flutter Interview](https://github.com/p0dyakov/flutter_interview), [Flutter Roadmap](https://github.com/p0dyakov/flutter_roadmap), [Flutter Acrticles](https://github.com/p0dyakov/flutter_articles), [Flutter Best Packages](https://github.com/p0dyakov/flutter_best_packages), [Flutter Tools](https://github.com/p0dyakov/flutter_tools)


<!-- TOC start (generated with https://github.com/derlin/bitdowntoc) -->

- [General](#general)
   * [OOP](#oop)
   * [SOLID](#solid)
   * [Git Flow](#git-flow)
   * [Data structures](#data-structures)
   * [Imperative and declarative programming](#imperative-and-declarative-programming)
   * [Stack and heap](#stack-and-heap)
   * [DAO, DTO, VO, BO](#dao-dto-vo-bo)
   * [DI and Service Locator](#di-and-service-locator)
- [Dart](#dart)
   * [final and const](#final-and-const)
   * [JIT and AOT](#jit-and-aot)
   * [Hot Restart and Hot Reload](#hot-restart-and-hot-reload)
   * [HashCode](#hashcode)
   * [Extension](#extension)
   * [Mixin](#mixin)
   * [Sound Null Safety](#sound-null-safety)
   * [Type system](#type-system)
   * [Late](#late)
   * [Generics](#generics)
   * [Dart VM](#dart-vm)
   * [Zones](#zones)
   * [Types of errors](#types-of-errors)
   * [Naming rules](#naming-rules)
   * [Never](#never)
   * [Covariant](#covariant)
   * [Annotations](#annotations)
   * [int8, uint8, int16, uint16...](#int8-uint8-int16-uint16)
   * [Future](#future)
   * [Future Constructors](#future-constructors)
   * [Await under the hood](#await-under-the-hood)
   * [Event Loop](#event-loop)
   * [Completer](#completer)
   * [Stream](#stream)
   * [Generators (sync* / async*)  ](#generators-sync-async)
   * [Multithreading in Dart and Flutter ](#multithreading-in-dart-and-flutter)
   * [Isolate](#isolate)
   * [Compute](#compute)
   * [Multithreading issues](#multithreading-issues)
- [Flutter](#flutter)
   * [Stateless and Stateful widgets](#stateless-and-stateful-widgets)
   * [Stateful Widget Lifecycle](#stateful-widget-lifecycle)
   * [BuildContext](#buildcontext)
   * [InheritedWidget](#inheritedwidget)
   * [Trees](#trees)
   * [Widget](#widget)
   * [Element](#element)
   * [RenderObject](#renderobject)
   * [Types of widgets](#types-of-widgets)
   * [Types of elements](#types-of-elements)
   * [The life cycle of an Element](#the-life-cycle-of-an-element)
   * [GlobalKeys](#globalkeys)
   * [LocalKeys](#localkeys)
   * [The Flutter device is under the hood](#the-flutter-device-is-under-the-hood)
   * [Execution model in Flutter](#execution-model-in-flutter)
   * [CustomPaint](#custompaint)
   * [WidgetsFlutterBinding](#widgetsflutterbinding)
   * [Bindings](#bindings)
   * [Platform Channels](#platform-channels)
   * [Build Modes](#build-modes)
   * [Package and Plugin](#package-and-plugin)
   * [FFI Plugin](#ffi-plugin)
   * [Animation stages](#animation-stages)
   * [Types of animations](#types-of-animations)
   * [What is a Tween](#what-is-a-tween)
   * [Tween animations](#tween-animations)
   * [Frame construction](#frame-construction)
   * [Layout calculation](#layout-calculation)
   * [BuildOwner](#buildowner)
   * [PipelineOwner](#pipelineowner)
   * [Garbage Collector](#garbage-collector)
   * [Task Runners](#task-runners)
- [Architecture](#architecture)
   * [Architecture](#architecture-1)
   * [Clean architecture](#clean-architecture)
   * [State Management](#state-management)
   * [Dependency Injection  ](#dependency-injection)
   * [Architectural patterns](#architectural-patterns)
   * [Ways to navigate](#ways-to-navigate)
   * [Databases](#databases)
- [Testing](#testing)
   * [Types of tests](#types-of-tests)
   * [TDD](#tdd)
- [Development patterns](#development-patterns)

<!-- TOC end -->

<!-- TOC --><a name="general"></a>
## General

<!-- TOC --><a name="oop"></a>
### OOP
`Object-oriented programming`  — this is a programming paradigm based on the representation of a program as a collection of objects, each of which is an instance of a certain class, and classes form an inheritance hierarchy.
- `Abstraction`
Modeling the interactions of entities in the form of abstract classes and interfaces to represent the system  
- `Encapsulation`
Combining data and methods working with it in a class  
- `Inheritance`
Creating new classes based on existing ones  
- `Polymorphism`
Using objects with the same interface without information about the type and internal structure of the object  

---
<!-- TOC --><a name="solid"></a>
### SOLID
- `Single Responsibility Principle`
The class should only be responsible for one thing.
- `Open-Closed Principle`
Software entities should be open for expansion, but closed for modification.
- `Liskov Substitution Principle (Barbara Liskov Substitution Principle)`
The inheriting class should complement, not replace, the behavior of the base class.
- `Interface Segregation Principle`
Clients should not implement logic that they do not use.
- `Dependency Inversion Principle`
The modules of the upper levels should not depend on the modules of the lower levels. Classes of both upper and lower levels should depend on the same abstractions (and abstractions should not know about the details).

---
<!-- TOC --><a name="git-flow"></a>
### Git Flow
Feature
1. `The beginning of a new feature`. Creating a new branch `feature/future_name` from `develop`
2. `Completion of the feature`. Merge `feature/future_name` into `develop`, delete `feature/future_name`
3. `The beginning of the release`. Creating a release branch `release/vX.X.X`, responding from the `develop` branch
4. `Release Completion`. The release branch `release/vX.X.X` merges into `master`, the release is tagged, the release branch merges into `develop`, the release branch is deleted 

Fix
1. `The beginning of correction`. From the `master` branch, create a `hotfix/fix_name`
2. `Completion of correction`. From the `hotfix/fix_name` branch, the fix is merged into `develop` and `master`, the fix branch is deleted 

---
<!-- TOC --><a name="data-structures"></a>
### Data structures
Data structures are needed to store data in a suitable way    
- `Arrays`  
- `Stacks` (*LIFO* - last in, first out)
- `Queues` (*FIFO* - first in, first out)
- `Linked lists`  
- `Trees`
- `Graphs`  
- `Hash tables`  

--- 
<!-- TOC --><a name="imperative-and-declarative-programming"></a>
### Imperative and declarative programming
- `Imperative style` - we describe **how** to achieve the desired result  
- `Declarative style` - we describe ** what kind of result ** we need

---
<!-- TOC --><a name="stack-and-heap"></a>
### Stack and heap
- A `stack` is an area of RAM that stores temporary data such as local variables and function return addresses. The amount of memory allocated for the stack is limited. The stack works in LIFO order  
- A `heap` is an area of RAM in which data created during program execution is stored. The heap is used to dynamically allocate memory for objects that can change size during program execution. The heap size is set when the application is launched, but, unlike the stack, it is limited only physically. Memory allocation on the heap is slower than on the stack.

---
<!-- TOC --><a name="dao-dto-vo-bo"></a>
### DAO, DTO, VO, BO
- `DAO (Data Access Object, data access Object)` is an abstract interface to some type of database or other storage mechanism  
- `DTO (Data Transfer Object, data transfer object)` is an object for transferring data (objects without behavior) between layers  
- `VO (Value Object, value object)` ⎼ is an object without special methods, having a set of properties (fields) of primitive data types, or also a Value object  
- `BO (Business Object, business object)` is an object that represents an entity from a certain "domain", that is, the industry for which the application was developed  

---
<!-- TOC --><a name="di-and-service-locator"></a>
### DI and Service Locator
- `DI` - passing class dependencies through constructor parameters
- `Service Locator` - singleton / class with a set of static methods

The `Service Locator` can be accessed from anywhere in the code. This is its main disadvantage

<!-- TOC --><a name="dart"></a>
## Dart
<!-- TOC --><a name="final-and-const"></a>
### final and const
- `final` is calculated in runtime. Only the instance value is constant. When using a final instance, a new memory area is allocated in memory, even if the object value is identical. 
- `const` is calculated at compile time.  Not only the value is constant, but also the instance itself. When using a const variable, a new memory area is not allocated, but a reference to an existing instance is used.

---
<!-- TOC --><a name="jit-and-aot"></a>
### JIT and AOT
- `Just-in-time (JIT) compilation` is a type of compilation that is performed directly while the program is running, which significantly speeds up the development cycle. But it should be borne in mind that the program may slow down and run slower
- `Ahead-of-time (AOT) compilation` is a type of compilation that is fully executed before running a program. The Dart code is converted to native machine code, which is then packaged into a binary file with the extension `.so` for `Android` or `.dylib` for `iOS`. `AOT` Takes longer than `JIT`, but as a result, the program runs much faster.

---
<!-- TOC --><a name="hot-restart-and-hot-reload"></a>
### Hot Restart and Hot Reload
- `Hot Reload` loads the changes to the `Dart VM` and reboots the widget tree, saving the state. Does not restart `main()` and `initState()`
- `Hot Restart` loads the changes to the `Dart VM` and restarts the entire application. Restarts `main()` and `initState()`. The state is not saved

---
<!-- TOC --><a name="hashcode"></a>
### HashCode
A `hash code` is a getter for any object that returns an `int`. It is needed when saving an object to `map` or `set`. Hash codes must be the same for objects that are equal to each other according to the == operator  
`int get hashCode => Object.hash(runtimeType, ..., ...);`

---
<!-- TOC --><a name="extension"></a>
### Extension
`Extension` is a syntactic sugar that allows you to extend an existing class (add methods, operators, setters and getters)

--- 
<!-- TOC --><a name="mixin"></a>
### Mixin
A `mixin` is a multiple inheritance mechanism that allows classes to use the functionality of other classes without explicit inheritance.

Mixins in Dart are defined by the keyword `mixin`. They can contain methods, fields, and getters/setters, but they cannot have constructors. Instead, mixins are initialized automatically when they are applied to a class. The `with` operator is used to use mixins    

If the mixins have a method with the same name, then the implementation that is specified in the last mixin will remain. Since mixins will override this method

---
<!-- TOC --><a name="sound-null-safety"></a>
### Sound Null Safety
`Sound Null Safety` is an addition to the Dart language that strengthens the type system by separating types that allow the value of `Null` from types that do not allow the value of `Null`. This allows developers to prevent errors related to `Null`.  

---
<!-- TOC --><a name="type-system"></a>
### Type system
<p align="left" width="100%">
    <img src="https://github.com/p0dyakov/flutter_interview/assets/80569772/93afb575-ee46-46d0-9717-ea6894e6f1b3" width="30%"/>
</p>
With the advent of null safety in Dart, the hierarchy of classes and interfaces has been changed to accommodate new type safety requirements. Here are the main changes:

1. **Adding non-nullable types**:
- Non-nullable types indicate that the value cannot be null.
   - All existing types have been divided into non-nullable and nullable versions. For example, `int` became `int` (non-nullable) and `int?` (nullable)

2. **The new root of the hierarchy is "Object?"**:
   - Has a new root class `Object` been introduced?`, which can be null. In previous versions of Dart, the root class was `Object`

3. **Changes in the error hierarchy**:
- A new class `NullThrownError` has been introduced, which represents an error that occurs when trying to throw a `null` exception

4. **`late` and `required`**:
- The keywords `late` and `required` have been introduced to indicate variables that can be initialized later and must be initialized when declaring, respectively.

---
<!-- TOC --><a name="late"></a>
### Late
`Late` is a keyword in dart that allows you to declare a non-nullable variable without setting a value for it. The value is initialized only when we access it. 

---
<!-- TOC --><a name="generics"></a>
### Generics
`Generics` are parameterized types. They allow the program to get away from being tightly bound to certain types, define the functionality so that it can use data of any type and ensure their security. Generalizations also reduce code repeatability and give you the opportunity to provide a single interface and implementation for many types.

---
<!-- TOC --><a name="dart-vm"></a>
### Dart VM
`Dart VM (Dart virtual machine)` - Dart runtime environment

Components:
- `Execution Environment`
- `Garbage Collector`
- `Basic libraries and native methods`
- `System debugging`
- `Profiler`
- `ARM Architecture Simulator`

---
<!-- TOC --><a name="zones"></a>
### Zones
A zone is a mechanism that allows you to manage and handle errors and other events that occur in certain areas of the code.

1. Protecting your application from termination due to an unhandled exception
2. Association of data known as `zone-local values` with individual zones
3. Redefining a limited set of methods, such as print() and scheduleMicrotask(), inside part or all of the code
4. Perform the operation every time the code enters or exits the zone. These operations may include starting or stopping a timer or saving a stacktrace.

---
<!-- TOC --><a name="types-of-errors"></a>
### Types of errors
`Exception` is a general class for exceptions that usually occur due to errors in the program, and they can be handled and recovered from:
- DeferredLoadException
- FormatException
- IntegerDivisionByZeroException (marked as deprecated)
- IOException
- FileSystemException
- PathNotFoundException
- HttpException
- RedirectException
- ProcessException
- SignalException
- SocketException
- StdinException
- StdoutException
- TlsException
- CertificateException
- HandshakeException
- WebSocketException
- IsolateSpawnException
- TimeoutException
- NullRejectionException

`Error` is a class for errors that usually cannot be repaired, and they indicate serious problems in the program or system:
- OSError
- ArgumentError
- IndexError
- RangeError
- AssertionError
- AsyncError
- ConcurrentModificationError
- JsonUnsupportedObjectError
- JsonCyclicError
- NoSuchMethodError
- OutOfMemoryError
- RemoteError
- StackOverflowError
- StateError
- TypeError
- UnimplementedError
- UnsupportedError

---
<!-- TOC --><a name="naming-rules"></a>
### Naming rules
- Variables and constants - `lowerCamelCase`
- Classes, mixins, enums - `UpperCamelCase`
- Files - `snake_case`

---
<!-- TOC --><a name="never"></a>
### Never
`Never` is a type, meaning that no type is allowed and `Never` itself cannot be created. It is used as a return type in case of a guaranteed error.

---
<!-- TOC --><a name="covariant"></a>
### Covariant
`Covariant` is a keyword in dart that indicates that the type of the return value can be changed to a narrower type in the subclass.

---
<!-- TOC --><a name="annotations"></a>
### Annotations
`Annotations` are syntactic metadata that can be added to the code. In other words, it is an opportunity to add additional information to any component of the code, for example, to a class or method. Annotations always start with the character `@` (`@override`, `@required`). Any class can serve as an annotation if a const constructor is defined in it.

---
<!-- TOC --><a name="int8-uint8-int16-uint16"></a>
### int8, uint8, int16, uint16...
|Specifier|Common Equivalent|Bytes|Minimum value|Maximum value|
|--|--|--|--|--|
|int8|signed char|1|-128|127|
|uint8|unsigned char|1|0|255|
|int16|short|2|-32,768|32,767|
|uint16|unsigned short|2|0|65,535|
|int32|long|4|-2,147,483,648|2,147,483,647|
|uint32|unsigned long|4|0|4,294,967,295|
|int64|long long|8|-9,223,372,036,854,775,808|9,223,372,036,854,775,807|
|uint64|unsigned long long|8|0|18,446,744,073,709,551,615|

---
<!-- TOC --><a name="future"></a>
### Future
`Future` is a wrapper over the result of an asynchronous operation. The Future code is NOT executed in parallel, but is executed in a sequence defined by the Event Loop.
Future states:
- Incomplete - the operation is not completed
- Completed with Result - the operation was completed successfully
- Completed with Error - the operation was completed with an error

---
<!-- TOC --><a name="future-constructors"></a>
### Future Constructors
- `Future(FutureOr<T> computation())`: Creates a future object that uses the Timer.run method to run the computation function asynchronously and returns its result.
- `FutureOr<T>`: specifies that the calculation function should return either a Future<T> object or an object of type T. For example, to get a Future<int> object, the calculation function should return either a Future<int> object or an int object
- `Future.delayed(Duration duration, [FutureOr<T> computation()])`: creates a Future object that runs after the time delay specified through the first Duration parameter. The second optional parameter indicates the function that runs after this delay.
- `Future.error(Object error, [StackTrace stackTrace])`: Creates a Future object that contains information about the error that occurred.
- `Future.microtask(FutureOr<T> computation())`: Creates a Future object that uses the scheduleMicrotask function to run the computation function asynchronously and return its result.
- `Future.sync(FutureOr<T> computation())`: Creates a Future object that contains the result of an immediately called computation function.
- `Future.value([FutureOr<T> value])`: creates a Future object that contains the value value.

---
<!-- TOC --><a name="await-under-the-hood"></a>
### Await under the hood
Under the hood, `await` moves all subsequent code to `then` at `Future`, which we are waiting for

---
<!-- TOC --><a name="event-loop"></a>
### Event Loop
The `Event Loop` is an eternal loop that executes all incoming tasks to the isolate.
It has two FIFO task queues:

`MicroTask Queue`
It is used for very short actions that must be performed asynchronously, immediately after completing any instruction before passing control back to the Event Loop. The MicroTask queue takes precedence over the Event queue

`Event Queue`
It is used for scheduling operations that receive results from external events (I/O operations, gestures, drawing, timers, threads)

---
<!-- TOC --><a name="completer"></a>
### Completer
The `Completer` allows you to supply a Future, send an execution event, or an error event. This can be useful when you need to make a Future chain and return the result.

--- 
<!-- TOC --><a name="stream"></a>
### Stream
A `stream` is a sequence of asynchronous events. Stream tells you that there is an event and when it will be ready  
- `Single subscription` is a type of stream where there can be only one subscriber. 
- `Broadcast` is a type of stream where there can be many subscribers. At the same time, Broadcast streams give their data regardless of whether someone is subscribed to them or not. Stream subscribers receive events only from the moment of subscription, and not from the moment of the start of the stream`s life

--- 
<!-- TOC --><a name="generators-sync-async"></a>
### Generators (sync* / async*)  
`Generator` this is a keyword that allows you to create a sequence of values using `yield`
- *sync** is a synchronous generator. Returns `Iterable`
- *async** is an asynchronous generator. Returns `Stream`
	
---
<!-- TOC --><a name="multithreading-in-dart-and-flutter"></a>
### Multithreading in Dart and Flutter 
`Dart` is a single—threaded programming language. It executes one instruction at a time. But at the same time, we can run the code in a separate thread using `Isolate`

---
<!-- TOC --><a name="isolate"></a>
### Isolate
`Isolate` is a lightweight process (execution thread) that runs in parallel with other threads and processes in the application. Each `Isolate` in Dart has its own instance of the Dart virtual machine, its own memory and is controlled using its own `Event Loop`.

--- 
<!-- TOC --><a name="compute"></a>
### Compute
`Compute` is a function that creates an isolate and runs the passed code.
	
---
<!-- TOC --><a name="multithreading-issues"></a>
### Multithreading issues

- `Deadlock` — each of the threads is waiting for events that other threads can provide
- `Race conditions` — a manifestation of the nondeterminism of the program executor with different relative order of execution of commands in different threads
- `Lock Contention` — the main time of the stream is spent not performing useful work, but waiting for a resource blocked by another stream
- `Live Lock` — the thread captures the resource, but after it is convinced that it cannot complete the work, it releases the resource, canceling the results

<!-- TOC --><a name="flutter"></a>
## Flutter

<!-- TOC --><a name="stateless-and-stateful-widgets"></a>
### Stateless and Stateful widgets
- `StatelessWidget` is a widget that has no state and does not change its properties during the operation of the application. They can only be changed through external events that occur in the parent widgets. 
- `StatefulWidget` is a widget that stores the state, during the operation of the application it can change it dynamically using `setState()`. 

---
<!-- TOC --><a name="stateful-widget-lifecycle"></a>
### Stateful Widget Lifecycle
1. `createState()` is called once and creates a changeable state for this widget at a specified location in the tree
2.  `mounted is true`
3. `initState()` is called once during initialization
4. `didChangeDependencies()` is called once after initialization and further upon notifications from the Inherited widgets at the top of the tree on which the widget depends 
5. `build()` is called every time you redraw
6. `didUpdateWidget(Widget oldWidget)` is called every time the widget configuration is updated
7. `setState()` is called imperatively for redrawing
8. `deactivate()` is called when a previously active element is moved to the list of inactive elements, while being removed from the tree
9. `dispose()` is called when this object is removed from the tree **forever**
10.  `mounted is false`

--- 
<!-- TOC --><a name="buildcontext"></a>
### BuildContext
The `BuildContext` is the interface that implements the `Element`. 

`BuildContext` can be useful when needed:
- Get a reference to the `RenderObject` object corresponding to the widget (or, if the widget is not a Renderer, then a descendant widget)
- Get the size of the `RenderObject`
- Access the tree and get the nearest parent `InheritedWidget`. This is used by virtually all widgets that usually implement the of method (for example, `MediaQuery.of(context)`, `Theme.of(context)` etc.)

---
<!-- TOC --><a name="inheritedwidget"></a>
### InheritedWidget
An `InheritedWidget` is a widget that provides its descendants with the ability to interact with the data stored in it. Solves the problem with passing data through constructors. It can notify widgets at the bottom of the tree about changes in its own data, thereby provoking their redrawing.  
To get an Inherited widget, call `context.dependOnInheritedWidgetOfExactType<T extends InheritedWidget>()`in `didChangeDependencies()`

*The complexity of the operation of obtaining InheritedWidget - O(1). This speed is achieved due to the fact that Inherited widgets are stored as a hash table in the `Element`.*

---
<!-- TOC --><a name="trees"></a>
### Trees
![](https://docs.flutter.dev/assets/images/docs/arch-overview/trees.png )
- The `Widget Tree` consists of `Widgets` that are used to describe the user interface
- The `Element Tree` consists of `Elements` that manage the widget lifecycle and link widgets and rendering objects.
- The `Render Tree` consists of `RenderObject`, which are used to determine the size, position, geometry, and areas of the screen that can be affected by gestures 
	
---
<!-- TOC --><a name="widget"></a>
### Widget
A `Widget` is an immutable description of a part of the user interface. The widget is associated with the element that controls the rendering. Widgets form a structure, not a tree 

---
<!-- TOC --><a name="element"></a>
### Element
An `Element` is a mutable representation of a widget at a specific location in the tree. They manage the lifecycle, link widgets and rendering objects.

---
<!-- TOC --><a name="renderobject"></a>
### RenderObject
`RenderObject` is a mutable object of the visualization tree. It has a parent object, as well as a data field that the parent object uses to store specific information about the object itself, for example, its position. This object is responsible for rendering, accounting for sizes and constraints, listening and processing clicks. If necessary, it is marked as `dirty`. It is redrawn using its own `layer` method

---
<!-- TOC --><a name="types-of-widgets"></a>
### Types of widgets
`Proxies` are widgets that store some information and make it available to posterity. These widgets are not directly involved in shaping the user interface, but are used to get the information they can provide.
- `InheritedWidget`
- `ParentDataWidget` (`LayoutId`, `Flexible`, `KeepAlive`, etc.)
- `NotificationListener`

`Renderer` are widgets that are directly related to the layout of the screen, as they determine the size, position, and rendering
- `Row`
- `Column`
- `Stack`
- `Padding`
- `Align`
- `Opacity`

`Component` are widgets that do not directly provide final information related to dimensions, positions, appearance, but rather data (or hints) that will be used to obtain that final information.
- `RaisedButton`
- `Scaffold`
- `Text`
- `GestureDetector`
- `Container`	

---
<!-- TOC --><a name="types-of-elements"></a>
### Types of elements
![image](https://user-images.githubusercontent.com/80569772/205450564-87d6c2d0-a994-4d1d-bbaa-2c8f7fb07385.png)
A `ComponentElement` is a layout element that does not explicitly contain drawing/display logic. There is a `build()` method that returns the widget. It is formed only when creating widgets `StatelessWidget`, `StatefulWidget`, `InheritedWidget`.
- `ProxyElement`
- `StatelessElement`
- `StatefulElement`

`RenderObjectElement` is a display element that is explicitly involved in drawing components on the screen. Contains a `RenderObject` and inherits from the `Element` class. It is formed when creating widgets `Padding`, `Column`, `Row`, `Center`, etc.
- `LeafRenderObjectElement`
- `ListWheelElement`
- `MultiChildRenderObjectElement`
- `RootRenderObjectElement`
- `SingleChildRenderObjectElement`
- `SliverMultiBoxAdaptorElement`
- `SlottedRenderObjectElement`

---
<!-- TOC --><a name="the-life-cycle-of-an-element"></a>
### The life cycle of an Element
1. The element is created by calling the `Widget.createElement` method and is configured by the widget instance from which the method was called.
2. Using the `mount` method, the created element is added to the specified position of the parent element. When calling this method, child widgets are also associated and objects of the rendering tree are mapped to the elements.
3. The widget becomes active and should appear on the screen.
4. If the widget associated with an element changes (for example, if the parent element has changed), there are several scenarios. If the new widget has the same `runtimeType` and `key`, then the element is associated with it. Otherwise, the current element is removed from the tree, and a new element is created and associated with the new widget.
5. If the parent element decides to delete a child element, or an intermediate one between them, this will delete the rendering object and move this element to the inactive list, which will deactivate the element.
6. When an item is considered inactive, it is not on the screen. An element can be inactive only until the end of the current frame, if it remains inactive during this time, it is dismantled, after that it is considered non-existent and will no longer be included in the tree.
7. When you re-include elements in the tree, for example, if an element or its ancestors have a global key, it will be removed from the list of inactive elements, the `activate` method will be called, and the render object associated with this element will again be embedded in the rendering tree. This means that the item should appear on the screen again.

---
<!-- TOC --><a name="globalkeys"></a>
### GlobalKeys
`GlobalKeys` are keys that provide access to widgets. For stateful widgets, global keys also provide access to the state. Allow widgets to change parents anywhere in the application without losing state. They must be unique to the entire application.

---
<!-- TOC --><a name="localkeys"></a>
### LocalKeys
`LocalKeys` are the keys that are needed to identify widgets in a collection with the same values and must be unique among widgets with the same parent widget. They can be used for tests:
- `ValueKey` is a key that uses a value of a certain type to identify itself. Overrides the comparison operator. If the value is the same, then the keys are the same
- `uniqueKey` is a key that is equal only to itself
- `ObjectKey` is the key that is used to bind the widget identifier to the identifier of the object used to create this widget

---
<!-- TOC --><a name="the-flutter-device-is-under-the-hood"></a>
### The Flutter device is under the hood
![image](https://user-images.githubusercontent.com/80569772/203052487-937d5923-9571-4752-9762-f0d6637b675e.png)

The `framework level` is everything we are working with at the time of writing the application, and all the service classes that allow us to interact with the engine level. Everything related to this level is written on Dart. The `Flutter Framework` interacts with the `Flutter Engine` through an abstraction layer called `Window`
  
The `engine level` is a lower level than the framework level, it contains classes and libraries that allow the framework level to work. Including the `Dart virtual machine`, `Skia` and so on.  
  
`Platform level` — specific mechanisms related to a specific launch platform.

The `Flutter Engine` notifies the `Flutter Framework` when:
- The event of interest occurs at the device level (orientation change, settings change, memory problem, application operation status...)
- Some kind of event occurs at the glass level (gesture)
- The platform channel sends some data
- But also mostly when the Flutter Engine is ready to render a new frame

---
<!-- TOC --><a name="execution-model-in-flutter"></a>
### Execution model in Flutter
1. A new process is created and launched — `Thread (Isolate)`. This is the only process in which your application will run.
2. Two queues with `MicroTask` and `Event` are initialized, the queue type is `FIFO` (note: first in first out, i.e. messages that arrived earlier will be processed earlier)
3. The `main()` function is executed
4. The `Event Loop` is started. It controls the order of execution of your code, depending on the contents of two queues: `MicroTask` and `Event`. It is an "endless" cycle. 
5. The `Event Loop` checks the `MicroTask` and `Event` with a certain frequency. If there is something in the `MicroTask`, then it is executed before the `Event` queue.

---
<!-- TOC --><a name="custompaint"></a>
### CustomPaint
`CustomPaint` is a class that creates a "canvas" for drawing. The `paint` method uses `canvas` as arguments, which allows you to draw various shapes

---
<!-- TOC --><a name="widgetsflutterbinding"></a>
### WidgetsFlutterBinding
`WidgetsFlutterBinding` is a specific implementation of application binding based on the widget infrastructure. In essence, it is the glue connecting the framework and the Flutter engine. The `WidgetsFlutterBinding` consists of many links: `GestureBinding`, `ServicesBinding`, `SchedulerBinding`, `PaintingBinding`, `SemanticsBinding`, `RendererBinding`, `WidgetsBinding`.

The `scheduleAttachRootWidget` method is a deferred implementation of `attachRootWidget`. This method belongs to `WidgetsBinding`. The description says that it attaches the passed widget to the `renderViewElement` — the root element of the element tree.

The `scheduleWarmUpFrame` method belongs to `SchedulerBinding` and is used to schedule the frame to start as soon as possible without waiting for the `Vsync` system signal.

---
<!-- TOC --><a name="bindings"></a>
### Bindings
![image](https://user-images.githubusercontent.com/80569772/203303949-aadb037a-c818-4f63-8ad8-67c3812a96ad.png)

`Bindings` are classes for exchanging data between the `Flutter Framework` and the `Flutter Engine`. Each binding is responsible for processing a set of specific tasks, actions, and events grouped by activity area.

`BaseBinding` is a basic abstract class, then let`s look at specific implementations of bindings. Among them we will see:  
  
`ServicesBinding` is responsible for redirecting messages from the current platform to the message data handler (`BinaryMessenger`);  
  
`PaintingBinding` is responsible for linking to the rendering library.  
  
`RenderBinding` is responsible for the connection between the rendering tree and the Flutter engine.  
  
`WidgetBinding` is responsible for the connection between the widget tree and the Flutter engine.  
  
`SchedulerBinding` — scheduler for the next tasks, such as:  
- calls of incoming callbacks that the system initiates in `Window.onBeginFrame` — for example, ticker events and animation controllers;
- calls of continuous callbacks initiated by the `Window.onDrawFrame` system, for example, events for updating the display system after incoming callbacks have worked out;
- post-frame callbacks that are called after continuous callbacks, before returning from `Window.onDrawFrame`;
- non-rendering tasks that must be completed between frames.

`SemanticsBinding` is responsible for linking the semantics layer and the Flutter engine.  
  
`GestureBinding` is responsible for working with the gesture subsystem.

---
<!-- TOC --><a name="platform-channels"></a>
### Platform Channels

![image](https://user-images.githubusercontent.com/80569772/202891758-b7cc7db9-3b4c-4ce3-9f91-37f9a1a614a1.png)
**(!)** Platform interactions are possible only in the main isolate. This is the isolate that is created when your application is launched. 

The `platform channel` is a two—way communication channel between the dart code and the native, which combines the channel name and codec to encode messages into binary form and back. The calls are asynchronous. Each channel must have a unique identifier.  
	
`Message channels` are platform channels designed for messaging between native code and a flutter application.  
`Message codecs`:
- `BinaryCodec` By implementing identifier mapping in byte buffers, this codec allows you to enjoy the convenience of channel objects in cases where you do not need encoding/decoding. Dart message channels with this codec are of the BasicMessageChannel<ByteData> type.
- `JSONMessageCodec` Works with "JSON-like" values (strings, numbers, boolean values, null, lists of these values and key string maps with this data). Lists and maps are heterogeneous and can be nested inside each other. During encoding, the values are converted to JSON strings and then to bytes using UTF-8. Dart message channels are of the BasicMessageChannel<dynamic> type with this codec.
- `StandardMessageCodec` Works with slightly more generalized values than the JSON codec, also supporting homogeneous data buffers (Uint8List, Int32List, Int64List, Float64List) and maps with non-string keys. Number processing differs from JSON in that Dart integers arrive on the platform as 32- or 64-bit signed integers, depending on the value never as floating-point numbers. The values are encoded in a special, fairly compact and extensible binary format. The standard codec is intended to be the default choice for the communication channel in Flutter. As for JSON, Dart message channels created using the standard codec are of the BasicMessageChannel<dynamic> type.  
	
`Method channels` are platform channels designed to call native code from a flutter application.    
`Method codecs`:
- `StandardMethodCodec` delegates encoding of payload values to `StandardMessageCodec`. Since the latter is extensible, the same can be said about the former.
- `JSONMethodCodec` delegates encoding of payload values to `JSONMessageCodec`.  
	
`Event channels` are specialized platform channels designed to be used in the case of representing Flutter platform events as a Dart stream. It works like a regular `Stream`

---
<!-- TOC --><a name="build-modes"></a>
### Build Modes
- `Debug` (`JIT`) for development
- `Release` (`AOT`) to publish the application
- `Profile` (`AOT`) for performance analysis

---
<!-- TOC --><a name="package-and-plugin"></a>
### Package and Plugin
- `Package` is written only in dart
- `Plugin` uses dart and platform-specific code

---
<!-- TOC --><a name="ffi-plugin"></a>
### FFI Plugin
- `FFI Plugin` is a plugin that uses [Dart FFI] to write platform-specific parts (https://dart.dev/guides/libraries/c-interop ). Allows you to run code in C/C++

---
<!-- TOC --><a name="animation-stages"></a>
### Animation stages
- `Ticker` asks `SchedulerBinding` to register a callback and tell `Flutter Engine` to wake it up when a new callback appears. 
- When the `Flutter Engine` is ready, it calls `SchedulerBinding` via the `onBeginFrame` request. 
- `SchedulerBinding` accesses the list of `ticker` callbacks and executes each of them.
- Each `tick` is intercepted by the "interested" controller to process it. 
- If the animation is completed, then `ticker` is "disabled", otherwise `ticker` requests `SchedulerBinding` to schedule a new callback. 
- ...
	
---
<!-- TOC --><a name="types-of-animations"></a>
### Types of animations
- `Tween animation`. The beginning, the end, the time, the speed are determined in advance  
- `Physics-based animation`. Imitate real behavior

---
<!-- TOC --><a name="what-is-a-tween"></a>
### What is a Tween
A `Tween` is an object that describes between which values the widget is animated and is responsible for calculating the current animation value
	
---
<!-- TOC --><a name="tween-animations"></a>
### Tween animations
- `Implicit Animations` is a set of `Implicitly Animated Widgets` that animate themselves when they are rebuilt with new arguments. (`AnimatedAlign`, `AnimatedContainer`, `AnimatedPadding`, etc.)
- `Explicit Animations` is a set of animation effects controls. They provide much more control over animation than `Implicit Animations`. To use it, you need to mix `SingleTickerProviderStateMixin` / `TickerProviderStateMixin` to the state of your widget, create an `AnimationController` and `Animation` depending on it, pass the animation to the `Transition Widget` (`AlignTransition`, `DecoratedBoxTransition`, `SizeTransition`, etc.)
`SingleTickerProviderStateMixin` / `TickerProviderStateMixin` creates ` Ticker`  
`Ticker` calls a callback for each animation frame  
`AnimationController` calculates all animation frames - controls animation (forward, reverse, repeat, stop, reset, etc.)
`Animation` gives the current animation value, and also allows you to subscribe to animation value/status updates  	

---
<!-- TOC --><a name="frame-construction"></a>
### Frame construction
1. Some external events lead to the need to update the display. 
2. The `Schedule Frame` is sent to the `Flutter Engine` 
3. When the `Flutter Engine` is ready to start updating the rendering, it creates a `Begin Frame` request
4. This `Begin Frame` request is intercepted by the `Flutter Framework`, which performs tasks related mainly to `Tickers` (for example, animation)
5. These tasks may re-create the request for later rendering (example: the animation has not finished its execution, and it will need to get another `Begin Frame` at a later stage to complete it)
6. Next, the `Flutter Engine` sends a `Draw Frame`, which is intercepted by the `Flutter Framework`, which will look for any tasks related to updating the layout in terms of structure and size
7. After all these tasks are completed, he moves on to tasks related to updating the layout in terms of rendering
8. If there is something on the screen that needs to be drawn, then a new scene for visualization is sent to the `Flutter Engine`, which will update the screen
9. Then the `Flutter Framework` performs all the tasks that will be performed after the rendering is completed (`PostFrame callbacks`), and any other subsequent tasks that are not related to rendering
10. …

---
<!-- TOC --><a name="layout-calculation"></a>
### Layout calculation
- Restrictions go down the tree, from parents to children.
- Sizes go up the tree from children to parents.
- Parents determine the position of the children.  

---
<!-- TOC --><a name="buildowner"></a>
### BuildOwner
`BuildOwner` is the manager for building and updating the element tree. He is actively involved in two phases — assembly and completion of assembly. Since the `BuildOwner` manages the tree assembly process, it stores lists of inactive items and lists of items that need updating.  
Methods:
- `scheduleBuildFor` makes it possible to mark an item as in need of updating.
- `LockState` protects the element from misuse, memory leaks and marking for updates during the destruction process.
- `buildScope` performs the reassembly of the tree. It works with items that are marked as in need of updating.
- `finalizeTree` completes the construction of the tree. Removes unused elements and performs additional checks in debugging mode, including for duplicating global keys.
- `reassemble` ensures the operation of the `HotReload` mechanism. This mechanism allows you not to rebuild the project with changes, but to send a new version of the code to `DartVM` and initiate a tree update.
	
---
<!-- TOC --><a name="pipelineowner"></a>
### PipelineOwner
`PipelineOwner` is an assembly manager that works with the display tree.

---
<!-- TOC --><a name="garbage-collector"></a>
### Garbage Collector
The `Garbage Collector` is an algorithm that monitors links and cleans up memory in order to prevent it from overflowing.

**(!)** During the garbage collection process, the Dart Framework layer creates a channel of interaction with the Flutter Engine layer, through which it learns about the moments of application downtime and lack of user interaction. At these moments, the `Dart Framework` starts the memory optimization process, which reduces the impact on the user experience and stability of the application. 

**Young garbage collector**  
![image](https://user-images.githubusercontent.com/80569772/203299873-834979fb-a548-476a-8f69-8be50c7ebd64.png)
	
The amount of memory used can be divided into two spaces: active and inactive. New objects are located in the active part, where, as it fills up, live objects are transferred from the active memory area to the inactive one, ignoring dead objects. Then the inactive half becomes active. This process is cyclical.

**Old garbage Collector (Parallel Marking and Concurrent Sweeping)**  
![image](https://user-images.githubusercontent.com/80569772/203300039-95a12d39-d502-4064-8a31-e903407fa04a.png)

1. The object tree is traversed, the objects used are marked with a special label. 
2. During the second stage, a repeated pass through the object tree occurs, during which the objects that were not marked in the first stage are processed
3. All labels are erased  

---
<!-- TOC --><a name="task-runners"></a>
### Task Runners
![image](https://user-images.githubusercontent.com/80569772/211004726-1eeef86f-cebf-41de-8bb3-a8485257565f.png)  
- `Platform Task Runner`: The main flow of the platform. The plugin code is executed here. For more information, see the UIKit documentation for iOS or the MainThread documentation for Android. This thread is not displayed in the performance overlay.
- `UI Task Runner`: The UI thread executes the Dart code in the Dart VM. This stream includes code written by you and code executed by the Flutter framework on behalf of your application. When your application creates and displays a scene, the UI thread creates a layer tree, a lightweight object containing device-independent drawing commands, and sends the layer tree to the raster stream for display on the device. Do not block this stream! Shown in the bottom row of the performance overlay.
- `Raster Task Runner`: The raster stream receives the layer tree and displays it by accessing the GPU (GPU). You cannot directly access the raster stream or its data, but if this stream is slow, then this is the result of what you did in the Dart code. The graphics libraries Skia and Impeller work in this stream. They are shown in the top row of the performance overlay. Previously, this stream was known as the "GPU stream" because it performs rasterization for the GPU. However, it is executed on the central processor. We renamed it the "raster stream" because many developers mistakenly (but quite reasonably) believed that this stream runs on the GPU.
- `IO Task Runner`: Performs expensive tasks (mainly I/O) that would otherwise block the operation of UI threads or raster threads. This stream is not displayed in the performance overlay.
	
[More details](https://www.programmersought.com/article/81813680395 /), [More details 2](https://medium.com/flutter-community/the-layer-cake-widgets-elements-renderobjects-7644c3142401 )

<!-- TOC --><a name="architecture"></a>
## Architecture
<!-- TOC --><a name="architecture-1"></a>
### Architecture
Architecture is a set of solutions for the organization of a program. Such as dividing the program into layers, building links between them, managing the state, and communicating with the UI. A good architecture makes the layers in the application loosely connected, which makes it easier to make changes, increases the testability of the code, and simplifies the system  

---
<!-- TOC --><a name="clean-architecture"></a>
### Clean architecture
Pure architecture is an architecture that follows `SOLID` and is divided into three independent layers:  
- `Data (datasources, models, repositories)` getting data from the outside
- `Domain (entities, repositories interfaces, usecases)` business rules
- `Presentation (bloc, pages, widgets)` display
	
[Example](https://github.com/ResoCoder/flutter-tdd-clean-architecture-course )		

---
<!-- TOC --><a name="state-management"></a>
### State Management

**Vanilla**   
	
`Advantages`  
- Low entry threshold.
- No third-party libraries are required.  

`Cons`  
- When the widget state changes, the widget tree is completely recreated each time.
- Violates the principle of sole responsibility. The widget is responsible not only for creating the UI, but also for loading data, business logic, and state management.
- Decisions on how to display the current state are made directly in the UI code. If the condition becomes more complex, then the readability of the code will decrease significantly.  

`Usage:`
- Widget State 

**BLoC**  
	
`Advantages`  
- Clear division of responsibility
- Predictable Event to State transformations
- Reactivity. There is no need to call additional methods
	
`Cons`
- Mandatory status in the Block 
- Frequent library changes
- Dependence on a third-party library

`Usage:`
- Widget State
- App State

**Redux**
	
`Advantages`  
- Unified state
- All actions are available to everyone  

`Cons`  
- Unified state
- Dependence on a third-party library
- A large amount of boilerplate code
- All actions are available to everyone  

`Usage:`
- Widget State
- App State

**Provider**
	
`Advantages`  
- Scopes for subtrees
- Flutter is oriented
- There is no static
- Ready-made providers

`Cons`  
- Link to the framework
- Only 1 provider of the same type
- Dependence on a third-party library

`Usage:`
- App State
- Partially DI

**Riverpod**  
	
`Advantages:`  
- Scopes for subtrees
- Flutter is oriented
- There is no static
- Ready-made providers

`Cons:`
- Dependence on a third-party library
- Cyclic dependencies fall in runtime

`Usage:`
- Widget State
- App State
- DI

---
<!-- TOC --><a name="dependency-injection"></a>
### Dependency Injection  
`Dependency injection (DI)` is a mechanism that allows you to make objects interacting in an application loosely coupled using interfaces. This makes the entire system more flexible, adaptable and extensible.

---
<!-- TOC --><a name="architectural-patterns"></a>
### Architectural patterns
![](https://fuzeservers.ru/wp-content/uploads/2/6/8/268a107e69309f0529c18aae72769bdb.png)
**MVVM** 

`Parts:`
- `Model` contains all the logic of the application, it stores and processes data, while not interacting with the user directly
- `View` displays the data that was passed to it
- `ViewModel` binds the model and the view (transfers data between them)

`Usage:`
- Used in a situation where data binding is possible without the need to enter special presentation interfaces (i.e. there is no need to implement IView);
- WPF technology is a common example.

[Example](https://github.com/jitsm555/Flutter-MVVM )

**MVC** 

`Parts:`
- `Model` contains all the logic of the application, it stores and processes data, while not interacting with the user directly
- `View` displays the data that was passed to it
- The `Controller` intercepts the event from the outside and, in accordance with the logic embedded in it, reacts to this event by changing the Model by calling the appropriate method. After the change, the Model uses the event that it has changed, and all subscribed to this View events, upon receiving it, access the Model for updated data, after which they are displayed 

`Usage:`
- Used in a situation where data binding is not possible (Binding cannot be used);

[Example](https://github.com/flutter-devs/Flutter_MVC )

**MVP**

`Parts:`
- `Model` contains all the logic of the application, it stores and processes data, while not interacting with the user directly
- `View` displays the data that was passed to it
- `Presenter` subscribes to presentation events, modifies the model on request, updates the view

`Usage:`
- Used in a situation where communication between the view and other parts of the application is not possible (and you cannot use MVVM or MVP);

---
<!-- TOC --><a name="ways-to-navigate"></a>
### Ways to navigate
**Navigator**
- It comes out of the box  

**Go Router**  
- Parsing of the path and query parameters (for example, "user/:id")
- Deep-links support
- Redirection support - you can redirect the user to another URL depending on the state of the application
- Named routes

**Auto Route**  
- Parsing of the path and query parameters (for example, "user/:id")
- Deep-links support
- Protected routes 
- Named routes
- Different animation options

---
<!-- TOC --><a name="databases"></a>
### Databases
**Non-relational (NoSQL):**  
**Hive** 

`Advantages:`
- Implementation on pure Dart, without platform code, due to which it works equally on different platforms
- Easy to use
- Fast write/read
- Little boilerplate code
- Availability of code generation
- Supported on all platforms

`Cons:`
- Links between objects must be maintained manually
- The limit on the number of adapters for objects is 224
- The limit on the number of fields in the adapter is 255
- Poorly suited for working with a large amount of data
- Uploads the entire database to memory
- You cannot access a box created in another isolate
- Availability of code generation
- There are no migrations

`Usage:`
- Small amount of data
- The need to save your data models

**Shared Preferences** 
	
`Advantages:`
- Easy to use 
- Synchronous reading from the in-memory cache
- Supported on all platforms

`Cons:` 
- Different implementations for Android/iOS and other platforms
- Accessing the platform code
- It is not guaranteed to write to disk after successful execution of the method
- It is impossible to save complex objects out of the box

`Usage:`
- Small amount of data
- The need for rapid implementation of the solution
- Saving application settings as primitive data

**Relational (SQL):**  
**SQFLite**
	
`Advantages`
- There are migrations
- Supports connections between entities
- Does not unload the database into RAM
- The ability to write complex SQL queries
	
`Cons:` 
- Difficult to use
- Not supported on Web, Linux, Windows
- The speed of operation is lower than that of NoSQL
- There may be different versions of SQLite on different OS and versions

`Usage:`
- Large amount of data
- Storage of complex structured data

**Drift**
- There are migrations
- Supports connections between entities
- Does not unload the database into RAM
- The ability to write complex SQL queries
	
`Advantages`
- There are migrations
- Fast
- Supported on all platforms

`Cons:` 
- Difficult to use
- The speed of operation is lower than that of NoSQL

`Usage:`
- Large amount of data
- Storage of complex structured data

<!-- TOC --><a name="testing"></a>
## Testing

<!-- TOC --><a name="types-of-tests"></a>
### Types of tests
- A `unit test` tests a single function, method, or class. Its purpose is to check the correctness of a certain function, method, or class. External dependencies for the module under test are usually passed as a parameter.
- `Widget test` tests one widget. The purpose of such a test is to make sure that the widget`s user interface looks and interacts as planned. Widget testing takes place in a test environment that provides the context of the widget`s lifecycle. Also, the widget under test should be able to receive user actions and events and respond to them. 
- The `integration test` tests the entire application or most of it. The purpose of the integration test is to make sure that all tested widgets and services work together as expected. In addition, you can use integration tests to check the performance of your application. As a rule, the integration test is performed on a real device or emulator.

---
<!-- TOC --><a name="tdd"></a>
### TDD
`TDD` is an application development technique in which first a test is written covering the desired change, and then the code that will allow the test to pass.

<!-- TOC --><a name="development-patterns"></a>
## Development patterns
*Generative*. They are responsible for convenient and safe creation of new objects or even entire families of objects.  
- Factory Method. A generative design pattern that defines a common interface for creating objects in a superclass, allowing subclasses to change the type of objects being created.
- Abstract Factory (Abstract Factory). A generative design pattern that allows you to create families of related objects without being tied to specific classes of objects being created.
- Builder (Builder). A generative design pattern that allows you to create complex objects step by step. The builder makes it possible to use the same construction code to get different representations of objects.
- Prototype. A generative design pattern that allows you to copy objects without going into the details of their implementation.
- Singleton (Single). A generative design pattern that ensures that a class has only one instance and provides a global access point to it.

*Structural*. They are responsible for building user-friendly class hierarchies.  
- Adapter (Adapter). A structural design pattern that allows objects with incompatible interfaces to work together.
- Bridge. A structural design pattern that divides one or more classes into two separate hierarchies — abstraction and implementation, allowing them to be changed independently of each other.
- Composite (Linker). A structural design pattern that allows you to group many objects into a tree structure, and then work with it as if it were a single object.
- Decorator (Decorator). A structural design pattern that allows you to dynamically add new functionality to objects by wrapping them in useful "wrappers".
- Facade. A structural design pattern that provides a simple interface to a complex class system, library, or framework.
- Flyweight (Lightweight). A design pattern that allows you to fit more objects into the allocated RAM. Lightweight saves memory by sharing the general state of objects among themselves, instead of storing the same data in each object.
- Proxy (Deputy). A structural design pattern that allows you to substitute special substitute objects instead of real objects. These objects intercept calls to the original object, allowing you to do something before or after transferring the call to the original.

* Behavioral*. They solve the tasks of effective and safe interaction between the objects of the program.  
- Chain of Responsibility. A behavioral design pattern that allows requests to be passed sequentially through a chain of handlers. Each subsequent handler decides whether it can process the request itself and whether it is worth passing the request further down the chain.
- Command (Command). A behavioral design pattern that turns requests into objects, allowing you to pass them as arguments when calling methods, queue requests, log them, and support the cancellation of operations.
- Iterator (Iterator). A behavioral design pattern that makes it possible to consistently bypass the elements of composite objects without revealing their internal representation.
- Mediator. A behavioral design pattern that allows you to reduce the connectivity of many classes to each other by moving these relationships into one intermediary class.
- Memento (Snapshot). A behavioral design pattern that allows you to save and restore the past states of objects without revealing the details of their implementation.
- Observer (Observer). A behavioral design pattern that creates a subscription mechanism that allows one object to monitor and respond to events occurring in other objects.
- State. A behavioral design pattern that allows objects to change behavior depending on their state. From the outside, it seems that the class of the object has changed.
- Strategy. A behavioral design pattern that defines a family of similar algorithms and places each of them in its own class, after which the algorithms can be interchanged right during program execution.
- Template Method (Template Method). A behavioral design pattern that defines the skeleton of an algorithm, shifting responsibility for some of its steps to subclasses. The pattern allows subclasses to redefine the steps of the algorithm without changing its overall structure.
- Visitor. A behavioral design pattern that allows you to add new operations to the program without changing the classes of objects on which these operations can be performed.

[More details](https://refactoring.guru/en/design-patterns/catalog )
