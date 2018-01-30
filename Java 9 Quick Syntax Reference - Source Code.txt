Java 9 Quick Syntax Reference - Source Code

*** Hello World ***
 
package myproject;
public class MyApp 
{
  public static void main(String[] args) 
  {
    System.out.print("Hello World");
  }
}
 
*** Compile and Run ***
 
// single-line comment
 
/* multi-line
   comment */

/** javadoc
    comment */
 
*** Variables ***

public class MyApp 
{
  public static void main(String[] args) 
  {
    // Declaration
    int myInt;

    // Assignment
    myInt = 10;

    // Output
    System.out.print(myInt); // "10"
  }
}
 
public class MyApp 
{
  public static void main(String[] args) 
  {
    byte  myInt8  = 2;  // -128   to +127
    short myInt16 = 1;  // -32768 to +32767
    int   myInt32 = 0;  // -2^31  to +2^31-1
    long  myInt64 = -1; // -2^63  to +2^63-1

    int myHex = 0xF;  // hexadecimal (base 16)
    int myOct = 07;   // octal (base 8)
    int myBin = 0b10; // binary (base 2) 

    int bigNumber = 10_000_000;

    double myDouble = 3.14;
           myDouble = 3e2; // 3*10^2 = 300

    float myFloat = 3.14F;
          myFloat = (float)3.14;

    char myChar = 'A';
         myChar = '\u0000'; // \u0000 to \uFFFF

    boolean myBool = false;
  }
}

 
// Anonymous block
public static void main(String[] args) 
{
  // Anonymous code block
  {
    int localVar = 10;
  }
  // localVar is unavailable from here
}

*** Operators ***
 
// Arithmetic operators
float f = 3+2; // 5 // addition
      f = 3-2; // 1 // subtraction
      f = 3*2; // 6 // multiplication
      f = 3/2; // 1 // division
      f = 3%2; // 1 // modulus (division remainder)

// Combined assignment operators
int i = 0;
    i += 5; // i = i+5;
    i -= 5; // i = i-5;
    i *= 5; // i = i*5; 
    i /= 5; // i = i/5;
    i %= 5; // i = i%5;

// Increment and decrement operators
++i; // i += 1
--i; // i -= 1

++i; // pre-increment
--i; // pre-decrement     
i++; // post-increment
i--; // post-decrement

int j;
i = 5; j = i++; // j=5, i=6   
i = 5; j = ++i; // j=6, i=6

// Comparison operators
boolean b = (2==3); // false // equal to
        b = (2!=3); // true  // not equal to
        b = (2>3);  // false // greater than
        b = (2<3);  // true  // less than
        b = (2>=3); // false // greater than or equal to
        b = (2<=3); // true  // less than or equal to

// Logical operators
b = (true && false); // false // logical and
        b = (true || false); // true  // logical or
        b = !(true);         // false // logical not

// Bitwise operators
i = 5 & 4; // 101 & 100 = 100 (4) // and
i = 5 | 4; // 101 | 100 = 101 (5) // or
i = 5 ^ 4; // 101 ^ 100 = 001 (1) // xor
i = 4 << 1;// 100 << 1  =1000 (8) // left shift
i = 4 >> 1;// 100 >> 1  =  10 (2) // right shift
i = 4 >>>1;// 100 >>>1  =  10 (2) // zero-fill 
                                  // right shift
i = ~4;    // ~00000100 = 11111011 (-5) // invert

i=5; i  &= 4; // 101 & 100 = 100 (4) // and
i=5; i  |= 4; // 101 | 100 = 101 (5) // or
i=5; i  ^= 4; // 101 ^ 100 = 001 (1) // xor
i=5; i <<= 1; // 101 << 1  =1010 (10)// left shift
i=5; i >>= 1; // 101 >> 1  =  10 (2) // right shift
i=5; i>>>= 1; // 101 >> 1  =  10 (2) // zero-fill
                                     // right shift
 
*** String ***
 
String a = "Hello";
String b = new String(" World");

String c = a+b; // Hello World
       a += b;  // Hello World

// String compare
boolean x = a.equals(b); // compares string
boolean y = (a == b);    // compares address
boolean z = "Hello".equals(a);

// StringBuffer class
StringBuffer sb = new StringBuffer("Hello");

sb.append(" World");   // add to end of string
sb.delete(0, 5);       // remove 5 first characters
sb.insert(0, "Hello"); // insert string at beginning

String s = sb.toString();
 
*** Arrays ***
 
// Array declaration 
int[] x;
int y[];

// Array allocation
int y[] = new int[3];

// Array assignment
y[0] = 1;
y[1] = 2;
y[2] = 3;

int[] x = new int[] {1,2,3};
int[] x = {1,2,3};

// Array access
System.out.print(x[0] + x[1] + x[2]); // "6"

// Multi-dimensional arrays
String[][] x = {{"00","01"},{"10","11"}};
String[][] y = new String[2][2];
 
y[0][0] = "00";
y[0][1] = "01";
y[1][0] = "10";
y[1][1] = "11";
 
System.out.print(x[0][0] + x[1][1]); // "0011"

int x[] = new int[3];
int size = x.length; // 3

// ArrayList class
java.util.ArrayList a = new java.util.ArrayList();

a.add("Hi");       // add an element
a.set(0, "Hello"); // change first element
a.remove(0);       // remove first element

a.add("Hello World");
String s = (String)a.get(0); // Hello World
 
*** Conditionals ***
 
// If statement 
if (x < 1) {
  System.out.print(x + " < 1");
}
else if (x > 1) {
  System.out.print(x + " > 1");
}
else {
  System.out.print(x + " == 1");
}

if (x < 1)
  System.out.print(x + " < 1");
else if (x > 1)
  System.out.print(x + " > 1");
else
  System.out.print(x + " == 1");

// Switch statement
switch (y)
{
  case 0:  System.out.print(y + " is 0"); break;
  case 1:  System.out.print(y + " is 1"); break;
  default: System.out.print(y + " is something else");
}

String fruit = "apple";
switch (fruit)
{ 
  case "apple": System.out.println("apple"); break;
  default: System.out.println("not an apple"); break;
}

// Ternary operator (?:)
x = (x < 0.5) ? 0 : 1;

*** Loops ***
 
int i = 0;
while (i < 10) { 
  System.out.println(i++); 
}

int i = 0;
do {
  System.out.println(i++); 
} while (i < 10);

for (int i = 0; i < 10; i++) { 
  System.out.println(i); 
}

for (int k = 0, l = 10; k < 10; k++, l--) { 
  System.out.println(k + l); 
}

for (int k = 0, l = 10; k < 10;) {
  System.out.println(k + l); k++; l--; 
}

int[] array = { 1,2,3 };
for (int element : array) { System.out.print(element); }

// Break and continue
myLoop: for (int i = 0, j = 0; i < 10; i++)
{
  while (++j < 10)
  {
    break myLoop;    // end for
    continue myLoop; // start next for                
  }
}
 
 
// Labeled block
validation:
{
  if(true)
    break validation;
}
 
*** Methods ***

class MyApp
{
  void myPrint()
  {
    System.out.print("Hello");
  }

  void myPrint(String s)
  {
    System.out.print(s);
  }

  public static void main(String[] args)
  {
    MyApp m = new MyApp();
    m.myPrint();        // "Hello"
    m.myPrint("Hello"); // "Hello"
  }
}
 
 
String getPrint()
{
  return "Hello";
}

public static void main(String[] args)
{
  MyApp m = new MyApp();
  System.out.print( m.getPrint() ); // "Hello"
}
 
 
void myPrint(String s)
{
  // Abort if string is empty
  if (s == "") { return; }

  System.out.println(s);
}


// Passing arguments
public static void main(String[] args)
{
  MyApp m = new MyApp();
  int x = 0;              // value data type
  m.set(x);               // value is passed
  System.out.print(x);    // "0"
 
  int[] y = {0};          // reference data type
  m.set(y);               // address is passed
  System.out.print(y[0]); // "10"
}
 
void set(int a) { a = 10; }
void set(int[] a) { a[0] = 10; }
 
*** Class ***
 
class MyRectangle
{
  public int x = 10, y = 20;
  public int getArea() { return x * y; }

  public MyRectangle()      { this(10,20);  }
  public MyRectangle(int a) { this(a,a);    }

  public MyRectangle(int x, int y)
  {
    this.x = x; 
    this.y = y;
  }

}

class MyApp
{
  public static void main(String[] args)
 {
    // Create an object of MyRectangle
    MyRectangle r = new MyRectangle();
    r.x = 10;
    r.y = 5;
    int z = r.getArea(); // 50 (5*10)
  }
}


class MyApp
{ 
  int x; // field is assigned default value 0
 
  int dummy() { 
    int x; // local variable must be assigned if used
  }
}


class MyApp
{ 
  public static void main(String[] args)
  { 
    MyApp a = new MyApp();

    // Make object available for garbage collection
    a = null;
  } 
} 

*** Static ***
 
class MyCircle
{
  float r = 10;            // instance field
  static float pi = 3.14F; // static/class field
 
  // Instance method
  float getArea() { return newArea(r); }
 
  // Static/class method
  static float newArea(float a) { return pi*a*a; }
}

class MyApp
{
  public static void main(String[] args)
  {
    float f = MyCircle.pi;
    MyCircle c = new MyCircle();
    float g = c.r;
    double pi = Math.PI;
  }
}
 
 
// Static fields
class MyCircle
{
  static void dummy() { count++; }
  static int count = 0;
}
 
 
// Static initialization blocks
class MyClass
{
  static int[] array = new int[5];

  // Static initialization block
  static
  { 
    int i = 0;
    for(int element : array)
      element = i++;
  }
}
 
 
// Instance initialization blocks
class MyClass
{
  int[] array = new int[5];

  // Initialization block
  { 
    int i = 0;
    for(int element : array) element = i++;
  }
}

*** Inheritance ***
 
// Superclass (parent class)
class Fruit
{
  public String flavor;
}
 
// Subclass (child class)
class Apple extends Fruit
{
  public String variety;
}

class MyApp
{
  public static void main(String[] args)
  {
    // Upcast and downcast
    Apple a = new Apple();
    Fruit f = a;
    f.flavor = "Sweet";
    Apple b = (Apple)f;
    Apple c = (f instanceof Apple) ? (Apple)f : null;
  }
}

*** Overriding ***
 
class Rectangle
{
  public int w = 10, h = 10;

  public int getArea() { 
    return w * h; 
  }

  public static int newArea(int a, int b) {
    return a * b;
  }
}
 
class Triangle extends Rectangle
{
  @Override public int getArea() {
    return w * h / 2;
  }

  public static int newArea(int a, int b) {
    return a * b / 2;
  }
}

class MyApp
{
  public static void main(String[] args)
  {
    Triangle o1 = new Triangle();
    o1.getArea(); // (50) calls Triangle's version

    Rectangle o2 = new Triangle();
    o2.getArea(); // (50) calls Triangle's version

    Triangle o3 = new Triangle();
    o3.newArea(10,10); // (50) calls Triangle's version
 
    Rectangle r = o3;
    r.newArea(10,10); // (100) calls Rectangle's version
  }
}
 
 
// Preventing method inheritance
public final int getArea() { return w * h; }
 
 
// Accessing overridden methods
class Triangle extends Rectangle
{ 
  @Override public int getArea() { 
    return super.getArea() / 2;
  }
}
 
 
// Calling parent constructor
public Triangle(int a, int b) { super(a,b); }
public Triangle() { super(); }
 
*** Packages and Import ***

package mypackage; // this file belongs to mypackage

// Import specific class
import mypackage.sub.MyClass;
// …
MyClass m;

// Import package
import java.util.*;

// Import static
import static java.lang.Math.*;
// …
double pi = PI; // Math.PI

*** Access Levels *** 
 
package mypackage;
public class MyApp
{
  public    int myPublic;   // unrestricted access
  protected int myProtected;// package or subclass access
            int myPackage;  // package access
  private   int myPrivate;  // class access
 
  void test()
  {
    myPublic    = 0; // allowed
    myProtected = 0; // allowed
    myPackage   = 0; // allowed
    myPrivate   = 0; // allowed
  }
}

class MyClass
{
  void test(MyApp m)
  {
    m.myPublic    = 0; // allowed
    m.myProtected = 0; // allowed
    m.myPackage   = 0; // allowed
    m.myPrivate   = 0; // inaccessible
  }
}
 

package newpackage;
import mypackage.MyApp;
 
class MyClass extends MyApp
{
  void test()
  {
    myPublic    = 0; // allowed
    myProtected = 0; // allowed
    myPackage   = 0; // inaccessible
    myPrivate   = 0; // inaccessible
  }
}

class MyClass
{
  void test(MyApp m)
  {
    m.myPublic    = 0; // allowed
    m.myProtected = 0; // inaccessible
    m.myPackage   = 0; // inaccessible
    m.myPrivate   = 0; // inaccessible
  }
}

 
// Accessible only from containing package
class PackagePrivateClass {}
 
// Accessible from any package
public class PublicClass {}
 
 
// Nested class access
class MyClass
{
  // Only accessible within MyClass
  private class PrivateNestedClass {}
}

*** Constants ***
 
class MyApp
{
  public static void main(String[] args)
  {
    // Local constant
    final double PI = 3.14;
  }
}

// Constant fields
class MyClass
{
  final double E;
  static final double C;
 
  public MyClass() { E = 2.72; }
  static { C = 3e8; }
}

class MyClass
{ 
  // Compile-time constant (static and known at compile-time)
  final static double C = 3e8;
 
  // Run-time constant (not static)
  final double E = 2.72;
 
  // Run-time constant (not known at compile-time)
  final static int RND = (new
  java.util.Random()).nextInt();
}  

*** Interface ***
 
interface MyInterface 
{
  int myMethod(); // method signature

  int c = 10; // constant

  // Types
  class Class {}
  interface Interface {}
  enum Enum {}
}
 
 
// Functionality interface
interface Comparable
{
  int compare(Object o);
}

class Circle implements Comparable
{
  public int r;

  public int compare(Object o) {
    return r - ( (Circle)o ).r;
  }

  public static Object largest(Comparable a, Comparable b)
  {
    return (a.compare(b) > 0) ? a : b;
  }
}
 
 
// Class interface
interface MyInterface
{
  void exposed();
}
 
class MyClass implements MyInterface
{
  public void exposed() {}
  public void hidden() {}
}

class MyApp
{
  public static void main(String[] args)
  {
    MyInterface i = new MyClass();
  }
}


interface MyInterface
{ 
  default void defaultMethod() {
    System.out.println("default");
  } 

  static void staticMethod() {
    System.out.println("static");
  }

  private static String getString() {
    return "string";
  } 

  default void printString() {
    System.out.println(getString());
  }
}

class MyClass implements MyInterface 
{
  public static void main(String[] args) { 
    MyInterface i = new MyClass();
    i.defaultMethod(); // "default"

    MyInterface.staticMethod(); // "static"
  } 
} 

*** Abstract ***
 
abstract class Shape
{
  public int x = 100, y = 100;
  public abstract int getArea();
}

class Rectangle extends Shape
{
  @Override public int getArea() 
  { 
    return x * y; 
  }
}

abstract class Shape
{
  public int x = 100, y = 100;
  public Shape(int a, int b) { 
    x = a; 
    y = b; 
  }
}

class Rectangle extends Shape
{
  public Rectangle(int a, int b) { 
    super(a,b); 
  }
}

*** Enum ***
 
enum Speed
{
  STOP, SLOW, NORMAL, FAST
}
 
 
enum Speed
{
  STOP(0), SLOW(5), NORMAL(10), FAST(20);
  public int speed;
 
  Speed(int s) { speed = s; }
}

class MyApp
{
  public static void main(String[] args)
  {
    Speed[] a = Speed.values();
    Speed s = Speed.valueOf(a[0].toString()); // Speed.STOP
  }
}

*** Exception Handling ***
 
import java.io.*;

class MyApp
{
  public static void main(String[] args)
  {
    try 
    {
      FileReader file = new FileReader("missing.file");
    }
    catch(FileNotFoundException e) 
    {
      System.out.print(e.getMessage());
    }
    catch(Exception e) 
    {
      System.out.print(e.getMessage());
    }
  }
}
 
 
// Finally block
import java.io.*;

class MyApp
{
  public static void main(String[] args)
  {
    FileReader in = null;
    try {
      in = new FileReader("missing.file");
    }
    catch(FileNotFoundException e) {
      System.out.print(e.getMessage());
    }
    finally {
      if (in != null) {
        try { in.close(); }
        catch(IOException e) {}
      }
    }
  }
}


class MyApp
{
  public static void main(String[] args)
  {
    try(FileReader file = new FileReader("missing.txt")) {
      // Read file
    } 
    catch(FileNotFoundException e) {
      // Handle exception
    }

    // Final resource
    final FileReader file1 = new FileReader("file1.txt");

    // Effectively final resource
    FileReader file2 = new FileReader("file2.txt");

    try(file1; file2) {
      // Read files
    } 
    catch(FileNotFoundException e) {
      // Handle exception
    }
  }
}

 
// Throwing exceptions
static void MakeException() throws Throwable
{
  throw new Throwable("My Throwable");
}
 
 
// Specifying exceptions
import java.io.*;

class MyApp
{
  static void MakeException() throws IOException, ArithmeticException
  {
    // …
    throw new IOException("My IO exception");
    // …
    throw new ArithmeticException("Division by zero");
  }
}

*** Boxing and Unboxing ***
 
class MyApp
{
  public static void main(String[] args)
  {
    int iPrimitive = 5;
    Integer iWrapper = new Integer(iPrimitive); // boxing
    iPrimitive = iWrapper.intValue(); // unboxing

    Integer x = new Integer(1000);
    Integer y = new Integer(1000);
    boolean b = (x == y);    // false
            b = x.equals(y); // true

    Integer iWrapper2 = iPrimitive; // autoboxing
    iPrimitive = iWrapper2;         // autounboxing

    Integer iWrapper3 = Integer.valueOf(iPrimitive);
    iPrimitive = iWrapper3.intValue();

    java.util.ArrayList a = new java.util.ArrayList();
    a.add(Integer.valueOf(5)); // boxing
    a.add(10);                 // autoboxing
  }
}

*** Generics ***
 
// Generic class
class MyBox<T> { public T box; }

class MyApp
{
  public static void main(String[] args)
  {
    MyBox<Integer> iBox  = new MyBox<Integer>();
    MyBox<Integer> iBox2 = new MyBox<>();

    iBox.box = 5;
    Integer i = iBox.box;
  }
}
 
 
// Generic methods
class MyClass
{
  public static <T> void printArray(T[] array)
  {
    for (T element : array)
      System.out.print(element + " ");
  }
}

class MyApp
{
  public static void main(String[] args)
  {
    Integer[] iArray = { 1, 2, 3 };
    MyClass.printArray(iArray); // "1 2 3"
    MyClass.<Integer>printArray(iArray); // "1 2 3" 
  }
}

 
// Generic functionality interface
interface IGenericCollection<T>
{
  public void store(T t);
}
 
// Non-generic class implementing generic interface
class Box implements IGenericCollection<Integer>
{
  public Integer myBox;
  public void store(Integer i) { myBox = i; }
}
 
// Generic class implementing generic interface
class GenericBox<T> implements IGenericCollection<T>
{
  public T myBox;
  public void store(T t) { myBox = t; }
}
 
 
// Generic variable usages
class MyClass<T>
{
  public void myMethod(Object o)
  {
    T t1;                            // allowed
    t1 = null;                       // allowed
    System.out.print(t1.toString()); // allowed
    if (o instanceof T) {}           // invalid
    T t2 = new T();                  // invalid
  }
}
 
 
// Bounded type parameters
// T must be or inherit from superclass A
class B<T extends A> {}
class A {}

// T must be or implement interface I
class C<T extends I> {}
interface I {}

class D<T extends A & I> {}

class E<T extends A & I, U extends A & I> {}
 
 
class Fruit
{
  public String name;
}
 
class FruitBox<T extends Fruit>
{
  private T box;
  public void FruitBox(T t) { box = t; }
  public String getFruitName()
  {
    // Use of Fruit member allowed since T extends Fruit
    return box.name;
  }
}
 
 
// Generics and Object
import java.util.ArrayList;

class MyApp
{
  public static void main(String[] args)
  {
    // Object ArrayList
    ArrayList a = new ArrayList();
    a.add("Hello World");
    // …
    Integer b = (Integer)a.get(0); // run-time error
  }
}
 

import java.util.ArrayList;

class MyApp
{
  public static void main(String[] args)
  {
    // Generic ArrayList (recommended)
    ArrayList<String> a = new ArrayList<String>();
    a.add("Hello World");
    // …
    Integer b = (Integer)a.get(0); // compile-time error
  }
}

*** Lambda Expressions ***

interface Summable 
{
  public int combine(int a, int b);
}

public class MyApp 
{
  public static void main(String[] args) {
    Summable s = (x, y) -> x + y;
    s.combine(2, 3); // 5
}


import java.util.function.*;
public class MyApp
{
  public static void main(String[] args) {
    BinaryOperator<Integer> adder = (x, y) -> x + y;
    adder.apply(2, 3); // 5

    UnaryOperator<Integer> doubler = x -> x*2;
    doubler.apply(2); // 4

    static void starter(Runnable s) { s.run(); }

    public static void main(String[] args) {
      Runnable r = () -> System.out.println("Hello");
      starter(r); // "Hello"
    }
  }
}



