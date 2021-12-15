# PDA Scanner
  
[![License][license-image]][license-url] 
[![Pub](https://img.shields.io/pub/v/pda_scanner.svg?style=flat-square)](https://pub.dartlang.org/packages/pda_scanner)

A Flutter plugin 🛠 to scanning. Ready for PDA 🚀 

[github](https://github.com/leyan95/pda_scanner)
[github](https://github.com/kazbekbet)

![pda_scanner.gif](https://upload-images.jianshu.io/upload_images/3646846-16ca17b573a765f2.gif?imageMogr2/auto-orient/strip%7CimageView2/2/w/320/format/webp)

## Installation

Add this to your package's pubspec.yaml file:

```
dependencies:
 pda_scanner:
    git:
      url: https://github.com/kazbekbet/pda_scanner
```

## Usage
```dart
/// Example
import 'package:pda_scanner/pda_source.dart';
import 'package:pda_scanner/pda_listener_mixin.dart';
import 'package:pda_scanner/pda_lifecycle_mixin.dart';

/// Automatically manage the pda life cycle (automatic initialization and automatic release), use PdaLifecycleMixin to mix into the app root component state.
/// If you encounter multiple mixing, please manually initialize the life cycle `super.initPdaLifecycle()` and release `super.disposePdaLifecycle()`
class RootWidgetState extends State<RootWidget> with PdaLifecycleMixin<RootWidget> {
  @override
  Widget build(BuildContext context) {
    // TODO
  }
}

/// Mix into PdaListenerMixin to monitor code scanning events
/// If you encounter multiple mixing, please manually initialize the life cycle `super.registerPdaListener()` and release `super.unRegisterPdaListener()`
class PageAlphaState extends State<PageAlpha> with PdaListenerMixin<PageAlpha> {
  var _code;

  @override
  Widget build(BuildContext context) {
    return null;
  }

  @override
  void onEvent(Object event) {
      // TODO: implement onEvent
  }
  
    @override
  void onError(Object error) {
      // TODO: implement onError
  }
}
```

## Contribute

We would ❤️ to see your contribution!

## License

Distributed under the MIT license. See ``LICENSE`` for more information.

## About

Created by Shusheng.

[license-image]: https://img.shields.io/badge/License-MIT-blue.svg
[license-url]: LICENSE
