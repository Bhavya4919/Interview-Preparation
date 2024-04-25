# C++ INTERVIEW QUESTIONS

### 1. What is C++?
C++ is an object-oriented programming language that was introduced to overcome the jurisdictions where C was lacking. By object-oriented we mean that it works with the concept of polymorphism, inheritance, abstraction, encapsulation, object, and class.  

### 2. What are the different data types in C++?
- Primititve Datatypes - Integer, Char, Float, Boolean, Double, Void, Wide Character
- Dervied Datatypes - Arrays, Pointers, Functions, Reference
- User Defined Datatypes - Strutures, Class, Union, Typedef, Enum

### 3. Difference Between C and C++
| C | C++ |
|:-------------|:--------------|
| C is a procedure-oriented programming language.         | C++ is an object-oriented programming language.        |
| C does not support data hiding.         | Data is hidden by encapsulation to ensure that data structures and operators are used as intended.        |
| C is a subset of C++         | C++ is a superset of C.        |
| Function and operator overloading are not supported in C         | Function and operator overloading is supported in C++        |
| Namespace features are not present in C         | Namespace is used by C++, which avoids name collisions.        |
| calloc() and malloc() functions are used for memory allocation and free() function is used for memory deallocation.         | new operator is used for memory allocation and deletes operator is used for memory deallocation.        |

### 4. What is Namespace? 
In C++, a namespace is a declarative region that provides a scope for identifiers (such as variables, functions, classes, etc.) to avoid naming conflicts and to organize code. The namespace keyword is used to define a namespace.

### 5. What is class and object?
A class is a user-defined data type that has data members and member functions. Data members are the data variables and member functions are the functions that are used to perform operations on these variables.
A class is a blueprint for creating objects (instances).

An object is an instance of a class. Since a class is a user-defined data type so an object can also be called a variable of that data type.

A class is defined as-
``` cpp
class A{
private:
 int data;
public:
 void fun(){

 }
};
```
### 6. What do you mean by abstraction in C++?
Abstraction is the process of showing the essential details to the user and hiding the details which we don’t want to show to the user or hiding the details which are irrelevant to a particular user.

### 7. What is polymorphism in C++?
Polymorphism in simple means having many forms. Its behavior is different in different situations. And this occurs when we have multiple classes that are related to each other by inheritance.

The two types of polymorphism in c++ are:

- Compile Time Polymorphism : Function Overloading, Operating Overloading
- Runtime Polymorphism : Virtual Functions, Function Overidding

### 8. Difference between struct and class
| Struct | Class |
|:-------------|:--------------|
| Members of the structure are public by default.         | Members of the class are private by default.        |
| When deriving a struct from a class/struct, default access specifiers for base class/struct are public.        |When deriving a class, default access specifiers are private.        |
| The memory in structures is stored as stacks. | The memory in classes is stored as heaps. |

### 9. Operator Overloading
Operator overloading is a feature in C++ that allows you to redefine the behavior of operators for user-defined types. This means you can use operators such as +, -, *, /, ==, !=, etc., with objects of your own classes.

### 10. Explain Constructors of C++
The constructor is a member function that is executed automatically whenever an object is created.

Constructors have the same name as the class of which they are members so that compiler knows that the member function is a constructor. 

And no return type is used for constructors.
``` cpp
class A{
 private:
  int val;
 public:
  A(int x){             //one argument constructor
   val=x;
  }
  A(){                    //zero argument constructor
  }
}
int main(){
 A a(3);     

 return 0;
}
```
There are 3 types of constructors:

A. Default constructor: It is the most basic type of constructor which accepts no arguments or parameters.
Even if it is not called the compiler calls it automatically when an object is created.

B. Parameterized constructor: It is a type of constructor which accepts arguments or parameters.
It has to be called explicitly by passing values in the arguments as these arguments help initialize an object when it is created. It also has the same name as that of the class. 

C. Copy Constructor: A copy constructor is a member function that initializes an object using another object of the same class. 
Also, the Copy constructor takes a reference to an object of the same class as an argument.
``` cpp
Sample(Sample& t) 
{ 
id = t.id; 
}
```

### 11. Tell me about virtual function
Virtual function is a member function in the base class that you redefine in a derived class. 

A virtual function is declared using the virtual keyword. 

When the function is made virtual, C++ determines which function is to be invoked at the runtime based on the type of the object pointed by the base class pointer.

### 12. Compare compile-time polymorphism and Runtime polymorphism
| Compile-time polymorphism | Runtime polymorphism |
|:-------------|:--------------|
| It is also termed static binding and early binding.         | It is also termed Dynamic binding and Late binding.        |
| It is fast because execution is known early at compile time.        | It is slow as compared to compile-time because execution is known at runtime.       |
| It is achieved by function overloading and operator overloading.         | It is achieved by virtual functions and function overriding.        |

### 13. What do you know about friend class and friend function?
A friend class can access private, protected, and public members of other classes in which it is declared as friends.

Like friend class, friend function can also access private, protected, and public members. But, Friend functions are not member functions.

### 14. What are the C++ access specifiers?
In C++ there are the following access specifiers:

Public: All data members and member functions are accessible outside the class.

Protected: All data members and member functions are accessible inside the class and to the derived class.

Private: All data members and member functions are not accessible outside the class.

### 15. What is a reference in C++?
A reference is like a pointer. It is another name of an already existing variable.
Once a reference name is initialized with a variable, that variable can be accessed by the variable name or reference name both.

For example-
``` cpp
int x=10;
int &ref=x;           //reference variable
```
If we change the value of ref it will be reflected in x. Once a reference variable is initialized it cannot refer to any other variable.
We can declare an array of pointers but an array of references is not possible.

### 16. Define inline function
If a function is inline, the compiler places a copy of the code of that function at each point where the function is called at compile time.
One of the important advantages of using an inline function is that it eliminates the function calling overhead of a traditional function.


### 17. What are the various OOPs concepts in C++?

Classes: It is a user-defined datatype

Objects: It is an instance of a class

Abstraction: It is a technique of showing only necessary details

Encapsulation: Wrapping of data in a single unit

Inheritance: The capability of a class to derive properties and characteristics from another class

Polymorphism: Polymorphism is known as many forms of the same thing

### 18. What do you mean by Call by Value and Call by Reference?
| Call by Value | Call by Reference |
|:-------------|:--------------|
| A copy of a variable is passed.        | It is also termed Dynamic binding and Late binding.        |
| Calling a function by sending the values by copying variables.        | Calling a function by sending the address of the passed variable       |
| the original value is never altered in Call by Value.         | The original value is altered in Call by reference.        |
| Passed actual and formal parameters are stored in different memory locations. Therefore, making Call by Value a little memory insufficient | Passed actual and formal parameters are stored in the same memory location. Therefore, making Call by Reference a little more memory efficient.|

### 19. Define token in C++
A token is the smallest individual element of a program that is understood by a compiler. A token comprises the following:

Keywords – That contain a special meaning to the compiler  

Identifiers – That hold a unique value/identity 

Constants – That never change their value throughout the program 

Strings – That contains the homogenous sequence of data 

Special Symbols – They have some special meaning and cannot be used for another purpose; eg: [] () {}, ; * = # 

Operators – Who perform operations on the operand

### 20. Difference between new and malloc
| New | malloc() |
|:-------------|:--------------|
| new is an operator which performs an operation          | malloc is a function that returns and accepts values       |
| new calls the constructors        | malloc cannot call a constructor       |
| new is faster than malloc as it is an operator         | malloc is slower than new as it is a function        |
| new returns the exact data type | malloc returns void*|

### 21. What is the difference between virtual functions and pure virtual functions?
| virtual functions |Pure Virtual Function |
|:-------------|:--------------|
|A Virtual Function is a member function of a base class that can be redefined in another derived class.| A Pure Virtual Function is a member function of a base class that is only declared in a base class and defined in a derived class to prevent it from becoming an abstract class.|
|A virtual Function has its definition in its respective base class.   |There is no definition in Pure Virtual Function and is initialized with a pure specifier (= 0).|
|The base class has a virtual function that can be represented or instanced; In simple words, its object can be made.|A base class having pure virtual function becomes abstract that cannot be represented or instanced; In simple words, it means its object cannot be made.|

### 22. What are destructors in C++?
Destructors are members of functions in a class that delete an object when an object of the class goes out of scope. Destructors have the same name as the class preceded by a tilde (~) sign. Also, destructors follow a down-to-top approach, unlike constructors which follow a top-to-down.

Syntax:
``` cpp
~constructor_name(); // tilde sign signifies that it is a destructor
```

### 23. Is destructor overloading possible? If yes then explain and if no then why?
The simple answer is NO we cannot overload a destructor. It is mandatory to only destructor per class in C++. Also to mention, Destructor neither take arguments nor they have a parameter that might help to overload.

### 24. What is an abstract class and when do you use it?
A class is called an abstract class whose objects can never be created. Such a class exists as a parent for the derived classes. We can make a class abstract by placing a pure virtual function in the class.

### 25. Multiple Inheritance:
In multiple inheritance, a derived class inherits from two or more base classes.

Example:
``` cpp
class Derived : public Base1, public Base2 {...};
```

Multiple inheritance can lead to the "diamond problem" where ambiguity arises if two base classes have a common base class. C++ provides ways to resolve this ambiguity, such as virtual inheritance.

### 26. What are the static members and static member functions?
When a variable in a class is declared static, space for it is allocated for the lifetime of the program. No matter how many objects of that class have been created, there is only one copy of the static member. So same static member can be accessed by all the objects of that class.

A static member function can be called even if no objects of the class exist and the static function are accessed using only the class name and the scope resolution operator ::



