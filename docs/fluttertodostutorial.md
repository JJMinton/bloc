# Flutter Todos Tutorial

![advanced](https://img.shields.io/badge/level-advanced-red.svg)

> In the following tutorial, we're going to build a Todos App in Flutter using the Bloc library.

![demo](./assets/gifs/flutter_todos.gif)

## Setup

We'll start off by creating a brand new Flutter project

```bash
flutter create flutter_todos
```

We can then go ahead and replace the contents of `pubspec.yaml` with

```yaml
name: flutter_todos
description: A new Flutter project.

environment:
  sdk: ">=2.0.0 <3.0.0"

dependencies:
  meta: ">=1.1.0 <2.0.0"
  equatable: ^0.2.0
  flutter_bloc: ^0.7.0
  flutter:
    sdk: flutter

dependency_overrides:
  todos_app_core:
    git:
      url: git://github.com/brianegan/flutter_architecture_samples
      path: todos_app_core
  todos_repository_core:
    git:
      url: git://github.com/brianegan/flutter_architecture_samples
      path: todos_repository_core
  todos_repository_simple:
    git:
      url: git://github.com/brianegan/flutter_architecture_samples
      path: todos_repository_simple

flutter:
  uses-material-design: true
```

and then install all of our dependencies

```bash
flutter packages get
```

?> **Note:** We're overriding some dependencies because we're going to be reusing them from [Brian Egan's Flutter Architecture Samples](https://github.com/brianegan/flutter_architecture_samples).
