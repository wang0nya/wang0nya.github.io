---
title: How you turn a string into a number (or vice versa) with Dart
updated: 2018-10-04
---
When you're so used to one language and you're trying to learn a new one, its likely that you'll find yourself always looking back to what you already know to find out if the new language matches up. I know I do. If I find similarities, I'm happy 🙂. If I find more features, I'm excited 😄. If the new language is lacking, I'm like, how come something so important (however trivial the thing may be) is missing 🤨 I can't work with this.

Say I needed to turn a string into a number with Javascript, there's a number of ways I could do it:
* using [`parseInt()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/parseInt)
* using [`parseFloat()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/parseFloat)
* using [`Number()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)

Dart has almost similar functions to achieve the same results.

### Turning a string into a number (or vice versa) with Dart

You can try out the code snippets on [dartpad](https://dartpad.dartlang.org/)

#### String to int
```dart
// String -> int
main () {
    var one = int.parse('1');
    print(one == 1); // prints true
}
```

#### String to double
```dart
// String -> double
main () {
    var onePointOne = double.parse('1.1');
    print(onePointOne == 1.1); // prints true
}
```

#### int to String
```dart
// int -> String
main () {
    String oneAsString = 1.toString();
    print(oneAsString == '1'); // prints true
}
```

#### double to String
```dart
// double -> String
main () {
    String piAsString = 3.14159.toStringAsFixed(2);
    print(piAsString == '3.14'); // prints true
}
```

I've been wanting to take up mobile app development with flutter so I thought I'd get comfortable with dart first before diving into flutter. So far, I'm happy. Coming from Javascript, Dart is easy to pick up, and fun to learn.