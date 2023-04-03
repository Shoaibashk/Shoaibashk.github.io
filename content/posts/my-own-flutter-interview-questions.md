---
title: "My Own Flutter Interview Questions"
date: 2023-04-03T23:50:54+05:30
# draft: true
---
Here is my own collection of handpicked flutter interview questions for experienced flutter engineers.

## What is Flutter?

Flutter is an open-source mobile application development framework created by Google. It allows developers to build native-looking mobile applications for both Android and iOS platforms using a single codebase. Flutter uses the Dart programming language, which is also developed by Google, and offers a wide range of customizable widgets that can be used to create stunning user interfaces.

Flutter's main advantage is its ability to deliver high-performance, visually appealing, and responsive applications in a short amount of time. It also offers hot reload functionality, which means developers can see changes to the code in real-time without having to rebuild the entire application.

Flutter has gained popularity among developers due to its ease of use and flexibility, making it a preferred choice for building mobile applications across various industries. Additionally, Flutter has a growing community of developers who contribute to the framework's development and provide support to fellow developers.

## What is the Architecture of Flutter?

At a high level, Flutter uses a layered architecture to render user interfaces and handle application logic. Here's a brief overview of the layers involved in Flutter's operation:

1.  **Flutter framework:** This layer provides a set of core libraries and APIs that are used to build Flutter applications. It includes widgets for building user interfaces, networking APIs, and other tools that help developers create high-quality mobile applications.

2.  **Engine layer:** This layer is responsible for rendering user interfaces and handling platform-specific functionality such as touch events, input handling, and platform integration. The engine layer communicates with the platform-specific code using platform channels.

3.  **Platform-specific code:** This layer includes platform-specific code for Android and iOS platforms, which is responsible for handling low-level functionality such as accessing system resources and handling platform-specific events.

4.  **Dart runtime environment:** Flutter uses the Dart programming language, which has its own runtime environment. This layer is responsible for running Dart code and providing the necessary services for garbage collection, reflection, and other language features.

When a Flutter application is launched, the Flutter framework creates a widget tree, which represents the user interface of the application. Each widget in the tree is responsible for rendering a part of the user interface. As the application runs, Flutter updates the widget tree based on changes in the application's state. The engine layer then takes the widget tree and renders it to the screen.

Overall, Flutter's architecture is designed to provide developers with a high-performance, flexible, and easy-to-use platform for building mobile applications.

## How many types of widget in flutter?

Flutter provides two types of widgets: StatelessWidget and StatefulWidget.

1.  **StatelessWidget:** A StatelessWidget is a widget that does not depend on any mutable state. It means that once the widget is built, it cannot be changed. The only way to change a StatelessWidget is to rebuild it. Stateless widgets are usually used for displaying static content, such as text or images.

2.  **StatefulWidget:** A StatefulWidget is a widget that can change its appearance based on mutable state. It means that a StatefulWidget can be updated dynamically, based on the data that it receives or changes that occur in the application. Stateful widgets are usually used for building complex user interfaces that require dynamic behavior, such as forms, animations, and interactive elements.


Both types of widgets have their own benefits and use cases. Stateless widgets are simpler and easier to manage, while Stateful widgets are more complex but offer more flexibility and interactivity. Flutter provides a wide range of built-in widgets for both types, which can be customized and combined to create complex user interfaces.

## What is Material in flutter?

In Flutter, "Material" is a design language developed by Google for building user interfaces. Material Design provides a set of guidelines and standards for creating visually appealing and responsive user interfaces that work well on both Android and iOS devices.

In Flutter, "Material" refers to a set of pre-built widgets and components that are designed to follow Material Design guidelines. These widgets include things like buttons, text fields, dialogs, navigation drawers, and more. Using these widgets can help ensure that your application follows Material Design principles, and can also speed up development time by providing pre-built components that you can use in your application.

Flutter's Material widgets are highly customizable, which means you can change things like colors, fonts, and spacing to match your application's branding and design. You can also create your own custom Material widgets if needed.

Overall, Material Design and the Material widgets in Flutter provide a powerful and flexible way to build high-quality user interfaces that follow established design principles and work well on a variety of devices.

## What is State management in flutter?

State management in Flutter refers to the process of managing the state of a Flutter application. In Flutter, the state refers to any data that can change during the lifetime of the application, such as user input, network responses, or changes in the application's data model.

State management is important in Flutter because it can affect the performance and behavior of the application. For example, if the state is not managed correctly, the application may become slow, unresponsive, or display incorrect information.

Flutter provides several options for managing state, including:

1.  **Stateful Widgets:** Flutter's built-in widgets include Stateful Widgets, which can hold mutable state that can change over time. When the state of a Stateful Widget changes, the widget is rebuilt to reflect the new state.

2.  **Inherited Widgets:** Inherited Widgets allow you to pass state down the widget tree to child widgets. This can be useful for sharing state between widgets that are not directly related.

3.  **Scoped Model:** Scoped Model is a third-party package that provides a way to manage state in a centralized way. It allows you to define a model class that holds the application's state, and then provides widgets with access to that state.

4.  **BLoC (Business Logic Component) pattern:** BLoC pattern is another third-party package that provides a way to separate business logic from presentation. It uses streams to handle state changes and provides a layer of abstraction between the UI and the application's data model.


There are several other state management solutions available in Flutter, each with its own advantages and disadvantages. Choosing the right state management solution depends on the complexity of your application and your specific needs.

## What is InheritedWidget?

InheritedWidget is a special type of widget in Flutter that allows data to be passed down the widget tree to its child widgets. It's designed to help manage state and simplify the process of passing data between widgets.

When an InheritedWidget is updated, all of its child widgets are rebuilt with the new data. This allows for efficient updates of the user interface and helps to prevent unnecessary rebuilds of unrelated widgets.

InheritedWidget is typically used when you have data that needs to be accessed by multiple widgets that are not directly related. For example, you might have an application theme that needs to be accessed by various parts of the application. Instead of passing the theme data down the widget tree manually, you can use an InheritedWidget to pass the data down automatically.

To use an InheritedWidget, you need to create a subclass of the InheritedWidget class and define a data object that you want to pass down the widget tree. You can then use the InheritedWidget's `of` method to retrieve the data object from anywhere in the widget tree.

InheritedWidget is a powerful tool for managing state in Flutter, but it should be used with care. Because InheritedWidget updates trigger a rebuild of all child widgets, it can be inefficient if used for data that changes frequently or doesn't need to be accessed by many widgets.

## What is Riverpod?

Riverpod is a state management library for Flutter that provides a simple and intuitive way to manage and share state between widgets in your application. It is an alternative to other popular state management solutions in Flutter, such as Provider, Scoped Model, and Redux.

One of the key features of Riverpod is its focus on dependency injection, which allows you to easily provide state to your widgets without needing to pass it down manually through the widget tree. Riverpod also provides a simple API for managing state, which makes it easy to create and update state objects and ensure that your application stays in sync.

Another advantage of Riverpod is that it supports asynchronous data loading, which means you can load data from a remote server or database without blocking the UI thread. This is accomplished using Riverpod's built-in support for Futures and Streams.

Riverpod is also highly customizable, which means you can adapt it to fit the specific needs of your application. For example, you can use Riverpod to create a centralized state store for your entire application, or you can use it to manage state for individual screens or widgets.

Overall, Riverpod is a powerful and flexible state management solution for Flutter that can help you build high-quality applications with less code and fewer bugs.


## what is AOT & JIT in flutter?

AOT (Ahead Of Time) and JIT (Just In Time) are two different ways that Flutter can compile and run Dart code.

JIT compilation involves compiling the Dart code into native machine code at runtime. This means that the Dart code is compiled and executed on the fly as the application is running. This approach is generally faster for development because it allows for faster iteration times and hot reloading, which allows you to see changes to your code in real-time.

AOT compilation involves compiling the Dart code ahead of time into native machine code before the application is deployed. This means that the Dart code is compiled into a binary that can be run directly on the device or emulator, without the need for a runtime environment. This approach is generally faster for production because the code is pre-compiled, which means it can be executed more quickly and with less overhead.

In Flutter, you can choose between AOT and JIT compilation depending on your specific needs. For example, JIT compilation is often used during development because it allows for faster iteration times and hot reloading, which can speed up the development process. AOT compilation, on the other hand, is often used in production because it provides faster startup times and better performance, which can result in a better user experience.

Flutter provides tools for both AOT and JIT compilation, which makes it easy to choose the right approach for your application.

## what is mixins in dart?

Mixins are a way to reuse a class's code in multiple class hierarchies without requiring that the class be inherited. In Dart, mixins are achieved by creating a new class that extends `Object` and then adding it to the inheritance hierarchy of other classes using the `with` keyword.

A mixin is essentially a way to add functionality to a class without modifying the class itself. The methods and properties defined in the mixin are made available to the classes that include the mixin via inheritance, but the mixin itself does not inherit from the classes that include it.

To create a mixin in Dart, you define a class that contains the code you want to reuse, and then you use the `with` keyword to mix the functionality into another class. For example:

```dart
class MyMixin {
  void doSomething() {
    print('Doing something...');
  }
}

class MyClass with MyMixin {
  // ...
}

void main() {
  var obj = MyClass();
  obj.doSomething(); // prints 'Doing something...'
}

```

In this example, the `MyMixin` class defines a `doSomething` method, and the `MyClass` class uses the `with` keyword to include the mixin in its inheritance hierarchy. As a result, instances of `MyClass` can use the `doSomething` method defined in the mixin.

Mixins are a powerful tool for code reuse in Dart, and they can help you to write more modular and maintainable code. However, it's important to use mixins judiciously and to avoid creating complex inheritance hierarchies that can be difficult to understand and maintain.

## What is Isolates?

In Flutter, isolates are independent workers that run in separate threads of execution. Each isolate has its own memory space and can run concurrently with other isolates, making it possible to perform multiple tasks at the same time without blocking the user interface.

Isolates in Flutter are based on the same concept as isolates in the Dart language, which are lightweight threads of execution that run in their own memory space. Isolates in Flutter are used to perform expensive operations in the background, such as network requests, file I/O, and heavy computations, without blocking the user interface.

Isolates in Flutter are created using the `Isolate.spawn()` function, which takes a callback function that will be executed in the new isolate. The `Isolate.spawn()` function returns a `Future` object that can be used to communicate with the new isolate and receive its results.

To communicate between isolates, Flutter provides the `SendPort` and `ReceivePort` classes, which are used to send and receive messages between isolates. Messages can be of any data type that can be serialized, such as strings, numbers, or custom objects.

Isolates in Flutter are a powerful tool for writing high-performance and responsive applications, and they can help to improve the user experience by reducing the amount of time that the user spends waiting for the application to respond. However, it's important to use isolates judiciously and to avoid creating too many isolates, which can cause performance issues and consume too much memory.

## What is Future?

In Flutter, `Future` is a class that represents a value or error that will be available at some point in the future. Futures are used to perform asynchronous operations, such as network requests, file I/O, and animations, without blocking the user interface.

When you perform an asynchronous operation that returns a `Future`, the operation is started in a separate thread of execution, and the `Future` is immediately returned to the caller. The `Future` represents the result of the asynchronous operation, which may not be available immediately.

To use a `Future` in Flutter, you typically create a new instance of the `Future` class and provide a callback function that will be executed when the result of the operation is available. You can use the `then()` method to register a callback function that will be called with the result of the operation.

Here's an example that shows how to use a `Future` to perform a network request and display the result in a Flutter widget:

```dart
import 'package:flutter/material.dart';
import 'package:http/http.dart' as http;

class MyWidget extends StatefulWidget {
  @override
  _MyWidgetState createState() => _MyWidgetState();
}

class _MyWidgetState extends State<MyWidget> {
  Future<String> _getData() async {
    final response = await http.get(Uri.parse('https://jsonplaceholder.typicode.com/todos/1'));
    return response.body;
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: FutureBuilder<String>(
          future: _getData(),
          builder: (context, snapshot) {
            if (snapshot.hasData) {
              return Text(snapshot.data!);
            } else if (snapshot.hasError) {
              return Text('Error: ${snapshot.error}');
            } else {
              return CircularProgressIndicator();
            }
          },
        ),
      ),
    );
  }
}
```


In this example, the `_getData()` method performs a network request using the `http` package and returns a `Future` that represents the result of the request. The `FutureBuilder` widget is used to display the result of the `Future` in the widget tree. The `builder` callback function is executed when the `Future` completes, and it can display the result or an error message, or a loading indicator until the result is available.

Futures are an essential part of writing asynchronous code in Flutter, and they provide a powerful and flexible way to handle asynchronous operations and update the user interface when the results are available.

## What is fastlane CLI?

Fastlane is an open-source toolset for automating the release process of mobile applications on both the iOS and Android platforms. It provides a collection of pre-built tools, scripts, and integrations that help mobile app developers to automate their build, testing, and deployment workflows.

Fastlane supports a wide range of tasks, including building and signing your app, running unit and UI tests, generating screenshots, distributing beta builds, and submitting your app to the app stores. It also integrates with a variety of third-party services, such as Crashlytics, Slack, and Git, to further automate your workflow.

Fastlane is designed to be highly configurable and customizable, so you can easily set up your own workflows to fit your team's specific needs. It also has a large and active community of developers who contribute plugins, scripts, and integrations to make the tool even more powerful.

Overall, Fastlane is a powerful tool that can help mobile app developers to streamline their release process, reduce manual errors, and save time and effort. It's a popular choice among mobile app developers, and it's widely used by both large and small companies.

## How to use fastlane in flutter?

Fastlane can be used to automate the release process of Flutter apps for both iOS and Android platforms. Here are the general steps to use Fastlane in Flutter:

1.  Install Fastlane: You can install Fastlane on your development machine using RubyGems by running the following command in your terminal:

```sh
sudo gem install fastlane -NV
```

2. Initialize Fastlane: Run the following command in your Flutter project's root directory to initialize Fastlane:

```sh
fastlane init
```

  This will create a `fastlane` directory in your project's root directory and generate some basic configuration files.
3. 1.  Set up Fastlane lanes: A Fastlane lane is a set of commands that automate a specific task in your release process, such as building your app, running tests, or uploading it to the app store. You can define your lanes in the `Fastfile` in the `fastlane` directory.
4. 1.  Add Fastlane plugins: Fastlane has a large collection of plugins that can help you automate specific tasks in your release process. You can add plugins to your Fastfile by specifying them in the `Gemfile` in the `fastlane` directory and running the `bundle install` command.
5. Run Fastlane: Once you have set up your lanes and added any necessary plugins, you can run Fastlane by running the following command in your project's root directory:
```sh
fastlane <lane_name>
```

	Replace `<lane_name>` with the name of the lane you want to run.

Fastlane can be a powerful tool to automate the release process of your Flutter app, and it can save you a lot of time and effort in the long run. However, setting up Fastlane and configuring your lanes can be complex and time-consuming, so it may take some effort to get started.




## How to use Isolates in flutter with riverpod?

Isolates in Flutter are used to run expensive operations in a separate background thread, keeping the UI thread free to respond to user interactions. Riverpod is a state management library for Flutter that allows you to manage your application state in a simple, scalable, and testable way.

To use isolates with Riverpod, you can create a `FutureProvider` or `StateNotifierProvider` that returns a `Future` or `StateNotifier` that runs on a separate isolate. Here is an example of how to use an isolate with `FutureProvider`:

```dart
import 'dart:isolate';
import 'package:flutter/foundation.dart';
import 'package:flutter_riverpod/flutter_riverpod.dart';

Future<int> expensiveOperation() async {
  int result = 0;

  await compute((int value) {
    for (var i = 0; i < value; i++) {
      result += i;
    }

    return result;
  }, 100000000);

  return result;
}

final expensiveFutureProvider = FutureProvider<int>((ref) async {
  final receivePort = ReceivePort();
  await Isolate.spawn(_isolate, receivePort.sendPort);
  final int result = await receivePort.first;
  return result;
});

void _isolate(SendPort sendPort) async {
  final result = await expensiveOperation();
  sendPort.send(result);
}

```


In this example, the `expensiveOperation` function runs on a separate isolate using the `compute` function from the `foundation` package. The `expensiveFutureProvider` returns a `FutureProvider` that runs on a separate isolate, and it returns the result of the expensive operation.

To use the `expensiveFutureProvider` in your widget, you can use the `Consumer` widget from `flutter_riverpod`:

```dart
Consumer(
  builder: (context, watch, _) {
    final result = watch(expensiveFutureProvider);
    return Text('$result');
  },
);

```
This will update the widget with the result of the expensive operation when it becomes available.

Note that using isolates may not always be necessary and can add complexity to your application. It's important to weigh the benefits and drawbacks before using them.