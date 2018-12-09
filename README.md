# Material ColorPicker

Color picker for Flutter, based on the Google Docs color picker.

![alt text](https://raw.githubusercontent.com/long1eu/material_color_picker/master/res/extras/demo.png)

## Getting Started

You can embed into your material app or use it on a Dialog like this:

```dart
Future<Color> colorPicker() async {
  return showDialog<Color>(
    context: context,
    barrierDismissible: false, // user must tap button!
    builder: (BuildContext context) {
      return SimpleDialog(
        children: <Widget>[
          ColorPicker(
            type: MaterialType.transparency,
            onColor: (color) {
              Navigator.pop(context, color);
            },
            currentColor: Colors.amberAccent,
          ),
        ],
      );
    },
  );
}
```

For help getting started with Flutter, view our online [documentation](http://flutter.io/).
