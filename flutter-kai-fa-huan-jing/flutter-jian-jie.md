---
description: >-
  Dart程式語言是一種新的程式語言，Dart是一種適用於全球資訊網的開放原始碼程式語言，由Google主導開發，目標在於成為下一代結構化Web開發語言。類似JavaScript，Dart也是一種物件導向語言，但是它採用類別為基礎的程式設計。它只允許單一繼承，語法風格接近C語言。
---

# Dart簡介

在介紹Dart之前，大部分的人都先聽到Flutter，Flutter也是由Google所提供，將大部分的元件完成，因此只要引用Flutter，Dart就能迅速的建立移動設備、電腦及伺服器、Web等應用程式。並以Dart編譯成原生的本機代碼或JavaScript。在安裝之前，不妨試試[Dart的線上編譯器](https://dartpad.dev/?)，可以迅速的測試簡單語法。

### 就從Hello World開始吧！

不免俗的我們也從Hello World開始這課程

```dart
void main（）{
  print ('Hello World!');
}
```

* Dart要以`main()`函式為起點
* Dart跟C語言一樣，不需要Calss
* Dart依照約定使用兩個字符的縮排 使用兩字元的縮排，讓程式碼更為緊湊。當開始創建FlutterApp時，會非常有用，因為FlutterApp基於

### 精簡的Dart程式碼

```dart
class Person {
  String name;
  int age;
 
  Person(this.name, this.age);
  
  int lieAboutMyAge() {
    print("My name is $name, my age is ${age - 10}");
  }
  
}void main() {
  final me = Person("Erik", 38);
  var girlfriend = Person("Shannon", 30);
  me.lieAboutMyAge();
}
```

作為現代新的程式語言，Dart有著需多新程式語言的特性，能夠實際精簡程式碼的大小，從上面的例子中可以發現幾個特性：

* 您只需在無體建構器中引用實例變量即可自動為其分配值
* 字符串具有類似模板的功能，使您可以直接使用變數甚至表達式 `${age - 10}`
* 創建物件時，不需要使用`new`關鍵字，但是如果你想要的話也可以喔。
* Dart同時支持頂級函式`main()`及物件方法。
* 


## Type Inference <a id="4f73"></a>

Dart is strongly typed. But did you notice that Dart uses type inference? We didn’t need to specify the type \(`Person`\) of the variables `me` and `girlfriend`. Instead, Dart inferred the type for us at compile time. This is in line with other modern languages like Kotlin.

## Final and Const <a id="134e"></a>

If you are sure a variable won’t change, you can declare it `final`. If you’re not sure — perhaps you’ll find another girlfriend next week — you use `var`.

There’s also a `const` modifier, which is a bit more difficult to grasp and has effect on the value.

A final variable can be assigned after compile time, like storing the response of an HTTP request, while a const must be known and defined before compilation.

If a collection or object is a const, it’s complete state is immutable at compile-time, hence it must be created from data that is available at compile time. In contrast, if a variable is final, you can’t reassign a new object to it, but you can still change the collection or object that it points to.

## Objects <a id="2141"></a>

Everything that can be assigned to a variable, is an object. Even numbers, functions, and `null` are objects. All objects are based on a class, and all objects inherit from a base object with the unsurprising name [Object](https://api.dart.dev/stable/2.9.1/dart-core/Object-class.html).

I like languages that do this because it allows numbers to have convenience methods like `isNegative` and `isOdd` , resulting in pleasant code that almost reads like a good novel:

```text
if (age.isNegative) {
  print("The age can not be negative, you fool!")
}
```

Speaking about numbers, Dart make life easier by only offering two types of numbers: integers and doubles \(both 64 bits and signed\).

## Private and public <a id="bad5"></a>

All identifiers are public by default. Dart doesn’t have keywords for public, private, or protected.

[A library in Dart](https://dart.dev/guides/language/language-tour#libraries-and-visibility) is everything that is in a single file. So library privacy means that the identifier is visible only inside the file that the identifier is defined in. To mark a Dart identifier private to its library, start its name with an underscore.

## Expressions and statements <a id="06a5"></a>

Dart has both expressions that result in a value and statements like `if… else` that don’t. This doesn’t differ from most other languages. Some of the usual suspects that are available in Dart too:

* while loops and for loops
* if…else statements
* The switch statement
* The construct `condition ? [expression if true] : [expression if false]`
* Exceptions

## Lists, Sets, and Maps <a id="6342"></a>

Dart supports these data types natively. Let’s look at some examples to get a feel for these data types, starting with lists:

```text
var myList = [1, 2, 3];
assert(myList.length == 3);
assert(myList[1] == 2);
var constantList = const [1, 2, 3];
constantList[1] = 1; // This causes an error!
```

Sets are unordered collections of unique items:

```text
var mySet = {'john', 'eric', 'martha'};
var elements = <String>{};
elements.add('fluorine');
```

Something that will bite you sometime: if you forget the type annotation on a set definition like the above one for `elements`, a map will be created. This is simply because maps also use accolades, and maps appeared first in the Dart language.

A map associates keys and values that can be any type. The following map is inferred to the type `Map<String, String>`:

```text
var gifts = {
  'first': 'partridge',
  'second': 'turtledoves',
  'fifth': 'golden rings'
};gifts['fourth'] = 'calling birds';
```

## Dart Package Manager <a id="4f5c"></a>

The website [https://pub.dev/](https://pub.dev/) contains publicly available packages that can be installed easily with Dart’s package manager, pub. The website, as of writing this, contains more than twelve thousand packages, some for Dart and many specifically for Flutter.

You can also use pub to install locally downloaded packages or packages hosted on GitHub.

## Conclusion <a id="9fb8"></a>

Dart is a modern, easy to learn language. If you want to dive in deeper, I recommend one or more of the following sites:

* [The Dart Language Tour](https://dart.dev/guides/language/language-tour)
* [Dart language samples](https://dart.dev/samples)
* [A guide to effective Dart programming](https://dart.dev/guides/language/effective-dart)

