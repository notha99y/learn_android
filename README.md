# Learn Android

# XML
```
xmlns: xml name space
```
## Commonly used Components
```xml
<ImageView
    android:layout_width="100dp"
    android:layout_height="100dp"
    android:src="@drawable/something" />

<TextView
    android:id="@+id/text_view_blahblah"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:textSize="24sp"
    android:fontFamily="sans-serif-light"
    android:textColor="@color/colorPrimaryDark"
    android:text="my text"/>

<EditText
    android:inputType="number"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:hint="hint"/>

<Button
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Text"/>

<RadioButton
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="text"/>

<CardView/>

/// <comment> Layouts </comment>

<LinearLayout
    android:orientation="vertical"
    android:gravity="center_horizontal"
    android:layout_margin="8dp"
    android:layout_width="match_parent"
    android:layout_height="match_parent">
</LinearLayout>

<RelativeLayout
    android:layout_width="match_parent"
    android:layout_height="match_parent">
</RelativeLayout>


```

# Java
## Variables
```java
String myString = "Literally anything you like";
int myRegularNumber = 57;
double myDecimalNumber = 14.6;
boolean myTrueOrFalse = true;

// Randomizer
Random myRandomizer = new Random();
int randomNumber = myRandomizer.nextInt(i:10) + 1; // because java start from 0 so we add a +1

// Decimal Formatter
DecimalFormat myDecimalFormatter = new DecimalFormat(pattern:"0.00");
String textResult = myDecialFormatter.format(result);
```

## Printing
```java
System.out.println(myString);
```

## Maths
```java
int a = 6;
int b = 7;
int result = a + b;
System.out.println(result)
```

## Methods
```java
// greet name
static void greetPerson(String name){
    System.out.println("Hello there " + name);
}

// combine names
static String combineName(String firstName, String lastName){
    return firstName + " " + lastName;
}

// Object is a type for anything
static void log(Object anything){
    System.out.printlin(anything);
}

```
### Commonly used methods
```java
String ageText = ageEditText.getText().toString(); // getting text from EditText widget

int age = Integer.parseInt(ageText); // converting string to int

String ageText = String.valueOf(age); // converting int to string

// Getting user input from commandline
Scanner userInputScanner = new Scanner(System.in);
int guess = userInputScanner.nextInt(); // program waits until user give an input
```


## Conditional Logic (IF Statements)
```java

if (guess == solution){
    System.out.println("You guessed the answer!");
} else if (guess < solution){
    System.out.println("Your guess is too low");
} else {
    System.out.println("Your guess is too high");
}
```

## Arrays
```java
// We can declare an array with the type, followed by square brackets

String[] aStringArray;
int[] aIntArray;

// we can't put things inside the array until we initialize it

// we can initialize it a few different ways.

// one way is to create an empty array, but we must specify how big it is

aStringArray = new String[4];
aIntArray = new int[3];

// Then we can start to put things inside it
aStringArray[0] = 'Hello';
aStringArray[1] = 'i am cool';

// another way is to provide the array contents at the point we initialize it

String[] names = {"Rachel",  "Simon", "Jane"};
double[] decimalNumbers = {0.3, 12.78, 143.9};

```

## Loops
### For loops
```java
String[] animals = {"cat", "dog", "horse", "sheep"};
for (int count =0; count <animals.length; count++){
    System.out.println(animals[count]);
}

for (String animal: animals){
    System.out.println(animal);
}
```
## Classes
```java
class Dog {
    // Fields or Attributes
    String name;
    String greeting;
    String breed;
    int size;

    // Methods
    void sayHello() {
        System.out.println(greeting + "! " + "My name is ...");

    }

    // Classes can specify how they are to be built. This is the class Constructuor
    Dog(String name, String greeting, String breed, int size){
        this.name = name;
        this.greeting = greeting;
        this.breed = breed;
        this.size = size;
    }
}

// Empty Constructor
Dog dog1 = new Dog();
Dog dog2 = new Dog();

dog1.name = "Fido";
dog1.greeting = "woof woof";
dog1.breed = "Great Dane";
dog1.size = 8;


```
### Declaring Fields
Fields are also known as Class Variables. When declaring Fields, all we need to do is to write the type and the variable name right after the Class declaration. This would give the variable scope in the entire class.

```java

```
# Kotlin

# Activity, Intent and the Android Manifest
- Activities are a single, focused thing that the user can do.
- Almost all activies interact with the user
- The 'Activity' class takes care of creating a window for you, in which you can place your UI, with setContentView(R.layout.your_layout)
- Intent allow you to change to new screen
- "Implicit" Intents allow you to move to another app

# Gradle
## Build files
`build.gradle` files is written in `groovy` language.

# Android Activity Lifecycle
The `Activity` class provides a number of callbacks that allow the activity to know that a state has changed: that the system is creating, stopping, or resuming an activity, or destroying the process in which the activity resides.
## 6 Lifecycle callbacks methods
1. onCreate()
1. onStart()
1. onResume()
1. onPause()
1. onStop()
1. onDestory()