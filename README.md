# Quantity Input (README to be finished)

<a href="https://www.buymeacoffee.com/4inka" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-blue.png" alt="Buy Me A Beer" style="width: 150px !important;"></a>

A Flutter plugin that created 

## Preview
![Overview](https://raw.githubusercontent.com/m3uzz/select_form_field/master/doc/images/select_form_field.gif)

## Usage

In the `pubspec.yaml` of your flutter project, add the following dependency:

``` yaml
dependencies:
  ...
  quantity_input: "^0.0.1"
```

You can create a simple quantity input widget with the following example:

``` dart
import 'package:flutter/material.dart';
import 'package:quantity_input/quantity_input.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatefulWidget {
  @override
  State<MyHomePage> createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  int simpleIntInput = 0;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Example'),
      ),
      body: Center(
        Column(
          mainAxisSize: MainAxisSize.min,
          children: [
            QuantityInput(
              value: simpleIntInput,
              onChanged: (value) => setState(() => simpleIntInput = int.parse(value.replaceAll(',', '')))
            ),
            Text(
              'Value: $simpleIntInput',
              style: TextStyle(
                  color: Colors.black,
                fontWeight: FontWeight.bold
              )
            )
          ]
        )
      )
    );
  }
}
```

## API
| Parameter | Description |
|---------|---------|
| value `(required)` | Value as `int` or `double` |

## Issues & Feedback
If you encounter any issue you can report it by filling an issue. Thank you for the support!

## Contributing
Every pull request is welcome