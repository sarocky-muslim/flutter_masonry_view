# flutter_masonry_view
A Flutter Masonry Grid Layout. Simple to Use and Easy to Understand

## Getting started
In the `pubspec.yaml` of your flutter project, add the following dependency:

```yaml
dependencies:
  ...
  flutter_masonry_view: <latest_version>
```

In your library add the following import:

```dart
import 'package:flutter_masonry_view/flutter_masonry_view.dart';
```

For help getting started with Flutter, view the online [documentation][flutter_documentation].

## Masonry
It works by placing elements in optimal position based on available vertical space, sort of like a mason fitting stones in a wall. You've probably seen it in use all over the Internet. 


### **Example**
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
[masonry_example]: https://raw.githubusercontent.com/Ai-Rocky/flutter_masonry_view/main/example/assets/images/example.jpeg