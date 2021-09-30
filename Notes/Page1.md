**1) What is difference between static and non-static members ?** 
<br>
- Both static and non static members are declared inside class block.
- Static members have prefix with static keyword.
- Both static and non-static members consist of block,variable and method.
-Static members gets it's memory inside static area. Before execution starts of main() method static members loaded inside static area.
- Non-static members creates it's object inside heap memory. To access non-static members we need to create an object.
- We can access static members directly, with the help of class name as a reference, object as a reference.
- We can access non-static members only with the help of object as reference. <br>

**2) Static Block** <br>
- Static block is also called as static initializer block.
- static block get's its memory inside static area.
- Static block executed before execution of main() method. i.e. Loading process of the class.
- Static block does not have any name so programmer can not called it.
- Static block does not have any return type so it does not return any value to programmer.
- Static block gets executed top to bottom order.
- We can have more than one static block. <br>

 **3) Non-static Block** <br>
 - Non-static block is also called as instance initializer block.
 - Non-static block get's it's memory inside object which is created in heap area.
 - Non-static block executed during the object creation.
 - Non-static block does not have any name so programmer cannot called it.
 - Non-static block does not have any return type so it does not return any value to programmer.
 - Non-static block executed top to bottom order.
 - We can have more than one non-static blocks. <br>
 
  **4) What is use of constructor ?**<br>
  - With the help of constructor we can initillize non-static members during the object creation. <br>
  
  **5) What is difference between constructor and method ?** <br>
  
| No |                               Constructor                              |                   Method                  |
|:--:|:----------------------------------------------------------------------:|:-----------------------------------------:|
| 1. |               Constructor must have same name as a class.              |    We can give any name to the method.    |
| 2. |               Constructor does not have any return type.               |          Method have return type.         |
| 3. | Constructor is called only once at the time of during object creation. | Method can be called any number of times. |


**What is OOPS (Object Oriented Programming) ?**
- Here we take all real time scenarius and convert it into a programming.
- Take real time scenarius of an object an identify it's properties and behaviour.
- properties(variable) and behaviour (methods)
  
**Which are pillers of OOP's ?**
1) Encapsulation
2) Inheritance
3) Polymorphism
4) Abstraction
5) Interface

**What is encapsulation ?**
- The process of binding proprties and behaviour of an object together is called as encapsulation.
- Advantage : Data hiding 
- Hiding the properties of class from outside the world is called as data hiding.
- To achive data hiding we use private keyword.
- If a member made as private we can not access it from another class (We can access them within it's own class only) 
- Even if the members are made as a private we should able to read it and modify it
- In order to achive this we need to create the methods
  i) Getter method (To read the private memebers)
  ii) Setter method (To modify the private members)
- In my project I use encapsulation concept to create Entity Class.

**What is Inheritance ?**
- The process of acquring the properties and behaviour of parent class to the child class is called as inheritance.
- Parent class is aslo called as superclass and child class is also called as subclass.
- Advantage : Reusability
- We can achive inheritance with the help of 'extends' keyword.
- Here non-static memebers of parent class are inherited to the child class object so that we can reuse members of parent class.
- static memebers do not inherited (static memebers stored in seprate block of memory i.e. in static area) but then they give us fell of inheritance by converting a statement.
- In my project I use inheritance concept for creating service layer.

**Which are the different types of inhertiance ?**
- 1) Single Inheritance
- 2) Muti-level Inheritance
- 3) Hirarchical Inheritance
- 4) Hybrid Inheritance
- 5) Multiple Inheritance
- A subclass consist of more than one superclass is called as multiple inheritance.
- Multiple inheritance is not possible in class level.

**Why multiple inheritance is not possible in class level ?**
**What is Diamand Problem ?**
- Here sub class 'C' extends two super classes A and B.
- And if we try to create object for sub class 'C'.
- During the object creation the constructor of class 'C' is been called.
- Since constructor consist of by default super call statement.
- So it is try to call the constructor of it;s super class but here class 'C' consist of two super classes so there will arrise ambiquity problem. (Which superclass constructor call first)
- Hence compiler will confuse because of this we can not achive multiple inheritance.
- Such a problem is called as diamond problem.

**What is polymorphism ?**
- An object exhibiting more than one form is called as polymorphism.
- Developing the feature such that it will take more than one form is called as polymorphism.
- We can achive polymorphism in two ways :
i) Compile Time Polymorphism
ii) Run Time Polymorphism

1) Compile Time Polymorphism 
- The binding between method calling statement and method implementation during compile time is called as compile time polymorphism.
- We can achive compile time polymorphism in two ways.
  __i) Method Overloading__
  - If our class having more than one methods which have same name and different number/types of arguments then method overloading is possible.
 __ii) Constructor Overloading__
  -  If our class having more than one constructors which have same name and different number/types of arguments then constructor overloading is possible.

2) Run Time Polymorphism 
- The binding between method calling statement and method implementation during run time is called as run time polymorphism.
- We can achive run time polymorphism in
i) Derived Type Casting/ Class Casting /Dynamic Dispatch
ii) Method Overriding 

**i) Derived Type Casting/ Class Casting/ Dynamic Dispatch**<br>
a) Upcasting :-
- In upcasting object of child class is created and that child class object referance is stored in parent class referance variable.
- In upcasting only parent class members are accessable.
- We can not access child class members.
- Upcasting is done by compiler automatically so it is also called as auto-upcasting.
- In upcasting if overriding is happends then overriding method is get called not overrideen.
b) Downcasting :-
- In downcasting object of parent class is created that parent class object referance is stored in child class referance variable.
- In downcasting we can not able to access any members (even parent class members)
- In order to perform downcasting we need take the help of cast operator.
- When we access the members ew will get run time exception (Class Cast Exception)
- This resoan to perform the downcasting we perform upcasting first and then do downcasting.

**ii) Method Overriding :-**
- Overriding the superclass method implementation by the subclass method implementation is called as method overriding.
- Here we inherited parent class method (non-static) in child class and in order to modify it's implementation we create the same method signature and provide the implementation.
- To perform method overriding it should have 
  a) same method name, same arguments
  b) They should have is a relationship (inheritance is mandatory)
  c) They should have same modifier.
  d) They should have same return type.
  i.e. Method signature should same.

**What is method hiding/ method shadowing ?**
- We can not achive method overriding with the help of static members.
- All static memebers will be allocated with the different block of memory.
- Here subclass implementation will be hidien by the superclass method implementation.
- Therefore we can call it as method hiding or method shadowing.
    
**What is interface ?**
- Interface is blueprint of the class.
- Interface is consist of following members
  i) Abstract(incomplete) non-static method.
  ii) concrete static method
  iii) static final variable.
- We can not create object for interface.
- Interface can not have constructor.
- We can create referance variable for interface.
- In java classes does not support multiple inheritance but interface support multiple inheritance.
- In my project I use interface concept for creating repository layer.

**final** 
- final is keyword in java.
- If we decalare the variable as final the value present inside the varibale becomes constant.
- We can not re-initillize a final variable.
- final varibale does not have any default value, we must initillize the value.
- It can be static/non-static.
- __Array :__ If you make array as a final then it's size can not be altered but we can re-initillize it's value.
- __Class:__ If you make class as a final we can not inherited that class.
- __Method:__ If you make method as a final then we can not override that method.
- *******************


