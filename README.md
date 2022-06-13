# flutter_masonry_view
A Flutter Masonry Grid Layout. Simple to use and easy to understand

## Getting started

In the `pubspec.yaml` of your flutter project, add the following dependency:

```yaml
dependencies:
  ...
  flutter_masonry_view: <latest_version>
```

In your library add the following import:

```dart
import 'package:flutter_masonry_view/masonry_view.dart';
```

For help getting started with Flutter, view the online [documentation][flutter_documentation].

## Layouts

This package contains various grid layouts. In the following section, you'll discover each one of them.
The explanation of the layout will always considered a top-to-bottom and left-to-right directions to simplify the description. However it is possible to change these directions in the code. 


### **Masonry**

This layout facilitates the browsing of uncropped peer content. Container heights are sized based on the widget size.


#### **Example**

![Masonry example][masonry_example]

```dart
class Home extends StatelessWidget {
  Home({Key? key}) : super(key: key);

  final _items = [
    'assets/images/1.jpeg',
    'assets/images/2.jpeg',
    'assets/images/3.jpeg',
    'assets/images/4.jpeg',
    'assets/images/5.jpeg',
    'assets/images/6.jpeg',
    'assets/images/7.jpeg',
    'assets/images/8.jpeg',
    'assets/images/9.jpg',
    'assets/images/10.jpg',
  ];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Flutter Masonry View'),
      ),
      body: SingleChildScrollView(
        child: MasonryView(
          listOfItem: _items,
          numberOfColumn: 2,
          itemBuilder: (item) {
            return Image.asset(item);
          },
        ),
      ),
    );
  }
}
```
<!-- Links -->
[flutter_documentation]: https://docs.flutter.dev/
[masonry_example]: example/assets/images/example.jpeg