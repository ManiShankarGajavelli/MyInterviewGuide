# MyInerviewGuide

### Comment
- Single Line Comments
  - Single line comments Start with //
- multi Line Comments
  - multi line comments Start with /* and ends with */
- Doc Comments
  - Doc Comments starts with /** and ends with */

~~~java
/**
* This is a Doc Comment
* @author  Mani Shankar G
* @version 1.0
*/
public class HelloWorld {

   public static void main(String[] args) {
      System.out.println("Hello World!");//this is single line comment
	  /*public int add(int a, int b){ -> this is multi line comment
		return a+ b;
	  }*/ 
   }
}

~~~

### Data Types
DataTypes define the size and type of value that it stores.

There are two types of datatypes
- Primitive Data types
- Reference data types

### Primitive Data Types

- boolean 
- byte
- short
- int
- float 
- long
- double
- char

### Reference data types

- Reference data types are reference to the dynamically created Objects.
  - reference objects are generally created with **new** keyword.

### Type Casting
there two types

-   implicit type casting
-   explicit type casting

```java

long x = 1;
byte b = (byte)x;	//Explicit Type Casting.
System.out.println(b);


```

### Varaibles
- A Variable is a memory location with holds the value and a variables will be create with any datatype.
~~~java
  ex: int a  = 20; // datatype variableName = value;
~~~
Different types of variables are:
- Instance Variables
  - A variables that is declared in a class but outside a method,constructor.
- Static Variables
  - a variable that is declared with **static** keyword is static variable and there will be a single copy of static variable to all instances of a class.
- Local Variables
  - A variable that is declared inside a method is called local variable, a local variable cannot be static.

### Package
- Package is notting but grouping of classes.

```java
 package com.java.test;//name of package

 import com.smallpdf.PdfReader;//requred packages.
class pdfreader {

    int pdfReader(String path){
        PdfReader.read(path);
    }
}

```
### Access Modifiers:
- public 
  - public members are accessible every where in our application
- private 
  - private members are accessible within the class only
- default
  - it is default one if notting was specified and it was accessible within the package.
- protected - 
  -  it was accessible within the package and sub packages.
-  static
   -  is to declare a member of a class as static, by this we don't need to create a object , we can call directly.


### Flow Controls

- if

```java

	public static void checkVoteEligibility(int age){
        if(age > 18)
        System.out.print("you are eligible to vote");
    }

```

- if else

```java

	public static void checkVoteEligibility(int age){
        if(age > 18) {        	
        	System.out.println("you are eligible to vote");
        }
        else {        	
        	System.out.println("you are not eligible to vote");
        }
    }

```
- nested if ... else

```java

class flow1 { 
  	public void checkDay(String day) {
		if (day.equals("sunday")) {
			System.out.println("today is holiday");
		} else if (day.equals("monday")) {
			System.out.println("today is not a holiday");
		} else if (day.equals("tuesday")) {
			System.out.println("today is not a holiday");
		} else
			System.out.println("invalid day");

	}
}

```


- Switch

```java

class flow1 { 
	public void checkDay1(String day) {

		switch (day) {
		case "sunday":
			System.out.println("today is holiday");
			break;
		case "monday":
			System.out.println("today is not a holiday");
			break;
		case "friday":
			System.out.println("today is not a holiday");
			break;
		default:
			System.out.println("it is invalid");
			break;
		}
	}
}

```


### Loops in java
Three types of Loops
-   for loop
-   while loop
-   do while loop

### For Loop :
~~~java
for(int Count = 100; Count >0; Count =Count -1) {
			System.out.println("Hello world " + Count);	
		}
~~~


### While Loop

~~~java
	int Count = 0;
		while (Count < 100) {
			System.out.println("Hello world " + Count);
			Count = Count + 5;
		}
~~~


### do ... while loop
~~~java
int Count = 1000;
		do {
			System.out.println("Hello world " + Count);
			Count = Count + 1;
		} while (Count < 100);

	}
 ~~~   


### OOPS(Object Oriented Programming System) :
-   A natural way of writing a program is called OOPS.

Threre are 4 main Concepts of OOPS

- Encapsulation
- Inheritance
- Polymorphism
- Abstraction


- Encapsulation
  - Wrapping of Member variables ad member methods into a single unit is called Encapsulation. few Examples are :
  
  -   Packages
  -   Class
  -   access modifiers


~~~java

	Class XYZcompany {
		int Salary;
		int getTDSDeduction();
	}
	
	class Developer extends company {
		int role;
		String getTechDetails();
	}

	public static void main(){
		Developer d = new Developer();
		d.Salary = 2222;
		d.getTDSDeduction();
	}
~~~

### Polymorphism

- Static polymorphism(compiletime/overloading)
	-	improve readability
	-	specific to a class
	-	inputs must be different
-	dyanamic polymorphism(runtime/overriding)
	-	For Specific Implementation to Child Class.
	-	it occurs in inheritance/parent-child relationship.
	-	Inputs should be same as parent class.

### Constructors 
-	Constructor is used to create an object in java.
-	Constructor is specific to a class.
-	Constructor name and class name should be same and it should not return any value.
-	every class wil have a default Constructor.

### Abstraction
The process of hiding the implementaion details and showing only the functionality to the user is called Abstraction.
- it is just a layer which hides what happens inside the api.
- Abstraction in java can achived with Abstact class and inerface.
- Abstract Class
	-	abstract class can have both abstract methods and not-abstract(Non static) methods.
	-	abstract class does not provide 100% Abstraction. 
-	Interface.
	- an interface can have only abstract methods and static final variables only.


### Final Keyword
-	Final keyword can be added before a variable,method and class.
-	Final Variables are **constant** and cannot be modified throughout the execution.
	-	Ex PAN,Aadhar.			
- Final Methods cannot be overridden.
  - Methods cannot be overriden by child class.
- Final Class cannot be inherited.
  - Final, then we cannot extends that class.
    - Ex:String,StringBuffer etc.,



### String
-	Sequence of Character is called String.

 ~~~java

 String s = "JAVA";//Literal 
 string s1 = new String("JAVA");//object.

 string s2 = new String("JAVA");//object.


 String x = "JAVA"

 String s = "JAVA is Programming Langugae"


 ~~~

### StringBuffer
 

### StringBuilder




### Object Class
Object is a super class of all classes in java.
 -	public String toString()
 	- it was used to represent any object as a String.		
 -	public class getClass();
 	- returns the runtime class of an object.
 -	public int hashCode()
	- it computes the hash values of given input objects
 -	public boolean equals(o)
 	- compares two objects.
 -	public Object clone()
	- it was a way to create an exact copy of the same object.
-	public void finalize()
	- it will be called just before the garbage collector is called.
-	public void wait()
-	public void notify()
-	public void notifyAll();

### Wrapper classes
- wrapper classes are reference types to primitive datatypes.
- Wrapper classes are used to convert a primitive data type to an object or an object to primitive data type.
- Collections doesn't support priimitive data types, so, we need to use Wrapper classes.
- All Wrapper classes already implements toString,hashcode and equals methods.
- Wrapper classes are :
  - boolean - Boolean 
  - char	- Charater
  - byte 	- Byte
  - short	- Short
  - int 	- Integer
  - long	- Long
  - float	- Float
  - double 	- Double

### Exceptions 
- An abnormal programme condition or termination is called Exception.
- All Exceptions are runtime errors.
- if we don't follow JVM rules then exceptions will be raised.
- In Java API, under Object class, we have 
  - Throwable Class
    - Exception
      - Checked Exception
        - FileNotFoundException
        - SqlException
      - UnChecked Exception
        - NullPointerException
    - Errors
      - IndexOutOfBound Exception
      - MemoryOutOfBoud Exception

- Exception
  - Exceptions that are handled by try-Catch block are called Exceptions.
- Errors
  - Exceptions that are not handled by try-Catch block are called Exceptions.
- Checked Exceptions
  - Exceptions that are identified by Compiler are called Checked Exceptions.
- UnChecked Exceptions
  - Exceptions that are identified by Compiler are called UnChecked Exceptions.
