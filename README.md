# Chal

Chal was a native android application that allowed users to create a account; and track progression of goals within the app. It became a passion project with a group of friends; we are no longer supporting the project. 

## Tech Stack Used

Kotlin([View](https://kotlinlang.org))

### Prerequisites

Be sure to run `git clone https://github.com/rutherfn/Chal-Android`, on the given repo. From there, you will be able to check out the master branch to get the up to date version of features!

## Getting Started / Running The Project

This project uses the latest Gradle version. Gradle will update if a new version gets released.

To run this app, you will need to download [Android Studio](https://developer.android.com/studio).

To run the project open the folder `code`

You will need to create a new emulator otherwise can use your own android phone [Use Your Android Phone](https://javatutorial.net/connect-android-device-android-studio).

From there the gradle will build the project and after completed, hit the `run` green button on top of the screen.

The app will build and run starting from the splash screen. The app is currently in not a working state since updating Gradle versions; unless using a old version of Gradle and or Android Studio.

## Core Project

- **`code`**: Includes the folder structure and initial classes to help you get started. Classes are organized into modules to maintain clarity and keep the code concise.

## Defined Modules

- **`account:`**: Modules related to account functionality, including account creation, password recovery, login to an existing account, user sign-up, and credential validation to ensure accurate authentication

- **`app`**: Manages the main Dependency Injection across all modules by defining a `Application` type that uses Hilt to make a entry way for the app.
- **`app-center`**: Contains an instance of App Center, with a note to remove it in the future.
- **`buildSrc`**: Centralizes the definition of project dependencies and libraries, which are then referenced in the `build.gradle.kts` files of other modules.
- **`challenge:`**: Modules that relate to functionality of users creating and joining said challenges; within the app.
- **`challenge-manager`**: Functionality that relates to a user managing challenges within the application
- **`data`**: Handles defining Room data as well as UI data; that we use to display to the user.
- **`firebase`**: Handles all of the firebase functionality. This is mainly Firebase Authentication and Firebase Database, which users Realtime database to save user info.
- **`main`**: Defines the entry point of the application being the MainActivity. It also declares our navigation stack; which also includes entry screens such as the news feed and the splah screens.
- **`more`**: Functionality in the app that allows you to see more challenges and join them.
- **`network`**: Really defines a isConnected extension functionality; that tries to ping google to tell me if I am connected to the internet or not.
- **`profile`**: Extension functionality that handles managing a profile for the user.
- **`shared-preference`**: Manages stored preferences on the device, making them accessible for later use.
- **`ui`**: Defines a bunch of base setup extension classes; that makes us create less UI by reducing the boilerplate of the code.

## MVVM(Model-View-ViewModel) Structure

### Structure:

- **Model**: Handles the data and business logic of the application, such as API calls or database operations.
- **ViewModel**: Acts as a bridge between the View and Model. It holds UI-related data and exposes it as `State` or `Flow` objects for the View to observe.
- **View (XML)**: The UI layer built using XML. The XML state gets loaded into the Fragment; while the viewModel will give us a state that gets observed in the Fragment; which then will update the UI if it needs to.

### Why is it Useful?

- **Separation of Concerns**: Keeps the UI logic separate from the business logic, making the codebase easier to manage and test.
- **Scalability**: Useful for modularizing the code, making it easier to extend and maintain as the app grows.

More info can be found here [MVVM](https://developer.android.com/codelabs/basic-android-kotlin-compose-viewmodel-and-state#0).

## Dependencies Being Used For Project

- **AppCompat**: Provides backward-compatible support for modern Android UI components.
- **Core Testing**: Tools for writing and executing unit tests for Android applications.
- **Coroutines**: Kotlin library for managing asynchronous programming with structured concurrency.
- **Espresso**: UI testing framework for simulating and verifying user interactions.
- **Firebase**: Suite of tools and SDKs for backend services like authentication, database, and cloud messaging.
- **Google Truth**: Assertion library for writing cleaner and more expressive test assertions.
- **Gson**: A library for converting Java and Kotlin objects to and from JSON.
- **JUnit**: Framework for writing and running unit tests in Java and Kotlin.
- **JUnit Jupiter**: Next-generation JUnit framework for writing tests with more flexibility.
- **Hilt**: Dependency injection framework for Kotlin.
- **Room**: Jetpack library for local database storage with SQLite, built on top of SQLite.

## Live Google Play Store

N/A - Was Just a concept that is no longer supported.

## Project Status

:white_check_mark: Completed
