# practice-kallam
# Poornima Kallam
### Favorite Band : Coldplay
Coldplay is my favorite band because their music is **meaningful**. I personally feel like they have very much **relatable and inspiring lyrics** in their songs. And thier music also serves like therapy for some people.

---
## Favorite Musicians

1. A. R. Rahman  
2. Taylor Swift  
3. Ed Sheeran

---
### Favorite Books

- The power of your subconscious mind
- Atomic Habits  
- Breath by James Nestor 

---
### More About Me

 My favorite travel destination :  
[My Favorite Location – Switzerland](MyLocation.md)

---
## Places I want to Visit

These are the places I want to atleast visit in my life and the reasoning why I want to visit.

| Places | Reason | Distance | Budget |
|--------|--------|----------|--------|
| Italy | To explore historic cities, art, and food| ~5,100 miles|$3000 |
| Australia| To see kangaroos and other wildlife in the city| ~9,300 miles | $4500 |
|  China | To experience the modern technologies, updated cities  | 6,700 miles  | $5000  |
| Bali  | To experience the nature and peace | 9,600 miles  | $2000  |
|  Bahamas | To experience clear water and beaches  | 1500 miles  | $2500 |

---
## Favorite Quotes

> "One day you'll leave this world behind, so live a life you will remember"  
*— Avicii*

> "What doesn't kill you makes you stronger"  
*— Kelly Clarkson*

---

##  Dart Singleton Example

The following Dart code demonstrates the **Singleton design pattern**.  
A singleton ensures that only **one instance of a class** is created and shared
throughout the program. This is useful when a single, consistent state is needed
across the application.

[Snippet Source – Dart Collection](https://pieces.app/collections/dart)


```dart
class SingletonClass {
  static final SingletonClass _instance = SingletonClass._internal();

  factory SingletonClass() {
    return _instance;
  }

  SingletonClass._internal();

  String property1 = 'Default Property 1';
  String property2 = 'Default Property 2';
}

/// Example consuming the singleton class and accessing/manipulating properties
/// To evaluate the difference between a normal class and a singleton class, comment
/// out the factory constructor and _instance in SingletonClass and re-run.
void main() {
  /// Properties before
  String property1Before = SingletonClass().property1;
  String property2Before = SingletonClass().property2;

  print('property1Before: $property1Before');
  print('property2Before: $property2Before');

  /// Updating the properties
  SingletonClass().property1 = 'Updated Property 1';
  SingletonClass().property2 = 'Updated Property 2';

  /// Properties after
  print('property1After: ${SingletonClass().property1}');
  print('property2After: ${SingletonClass().property2}');
}

