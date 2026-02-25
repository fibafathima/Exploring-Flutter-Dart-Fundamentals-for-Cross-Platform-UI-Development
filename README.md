# Flutter & Dart Fundamentals Assignment

## Understanding Flutter’s Architecture

Flutter's architecture consists of three main layers:

- **Framework Layer**: Written in Dart, includes widgets, rendering, and animation libraries.
- **Engine Layer**: Built in C++, handles rendering via Skia, text layout, and platform channels.
- **Embedder Layer**: Integrates Flutter with platform-specific APIs on Android, iOS, web, or desktop.

Flutter renders everything itself using the Skia engine, ensuring pixel-perfect consistency across devices without relying on native UI components.

## The Widget Tree

In Flutter, everything is a widget. The UI is built as a tree of widgets.

- **StatelessWidget**: For static UIs that don't change (e.g., labels, icons).
- **StatefulWidget**: For dynamic UIs that update based on user interaction or data changes (e.g., counters, forms).

The widget tree is rebuilt reactively when state changes, ensuring efficient updates.

## Dart Language Essentials

Dart is object-oriented and strongly typed, optimized for UI development.

Key concepts:
- **Classes & Objects**: Everything is an object.
- **Async/Await**: Handles asynchronous operations.
- **Null Safety**: Prevents null errors.
- **Type Inference**: Variables can be declared without explicit types.

Example Dart class:

```dart
class Student {
  String name;
  int age;

  Student(this.name, this.age);

  void introduce() {
    print('Hi, I’m $name and I’m $age years old.');
  }
}

void main() {
  var s1 = Student('Aanya', 20);
  s1.introduce();
}
```

## Reactive UI Demo

The app demonstrates a counter using StatefulWidget. When the button is pressed, `setState()` is called, triggering a rebuild of the widget tree and updating the UI efficiently.

## How Flutter’s Architecture Ensures Smooth Performance

Flutter’s widget-based architecture and Dart’s reactive rendering model ensure smooth cross-platform UI performance by:

- Rebuilding only the necessary parts of the widget tree when state changes, rather than the entire UI.
- Using a single codebase that compiles to native code, avoiding platform-specific inconsistencies.
- Leveraging Dart's efficient compilation and null safety to prevent runtime errors.

In the counter app:
- `StatelessWidget` would not update the count; it's static.
- `StatefulWidget` allows the count to change and the UI to reflect it instantly via `setState()`.

## Case Study: The Laggy To-Do App

Improper state management causes UI lag by triggering unnecessary rebuilds of the entire widget tree. Flutter’s reactive rendering rebuilds only affected widgets, maintaining consistent frame rates. Dart’s async model handles operations without blocking the UI.

In the demo, only the text displaying the count updates, not the whole screen.

## Screenshots

[Add screenshots here after running the app]

## Video Explanation

[Link to Google Drive video]
