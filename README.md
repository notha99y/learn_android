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
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
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

<LinearLayout
    android:orientation="vertical"
    android:gravity="center_horizontal"
    android:layout_margin="8dp"
    android:layout_width="match_parent"
    android:layout_height="match_parent">
</LinearLayout>
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
## Classes
### Declaring Fields
Fields are also known as Class Variables. When declaring Fields, all we need to do is to write the type and the variable name right after the Class declaration. This would give the variable scope in the entire class.

```java

```
# Kotlin