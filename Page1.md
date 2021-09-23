**1) What is difference between static and non-static members ?**
- Both static and non static members are declared inside class block.
- Static members have prefix with static keyword.
- Both static and non-static members consist of block,variable and method.
-Static members gets it's memory inside static area. Before execution starts of main() method static members loaded inside static area.
- Non-static members creates it's object inside heap memory. To access non-static members we need to create an object.
- We can access static members directly, with the help of class name as a reference, object as a reference.
- We can access non-static members only with the help of object as reference. 
 <br> 
**2) Static Block**
- Static block is also called as static initializer block.
- static block get's its memory inside static area.
- Static block executed before execution of main() method. i.e. Loading process of the class.
- Static block does not have any name so programmer can not called it.
- Static block does not have any return type so it does not return any value to programmer.
- Static block gets executed top to bottom order.
- We can have more than one static block.
 <br>
 **3) Non-static Block**
 - Non-static block is also called as instance initializer block.
 - Non-static block get's it's memory inside object which is created in heap area.
 - Non-static block executed during the object creation.
 - Non-static block does not have any name so programmer cannot called it.
 - Non-static block does not have any return type so it does not return any value to programmer.
 - Non-static block executed top to bottom order.
 - We can have more than one non-static blocks. 
  <br>
  **4) What is use of constructor ?**<br>
  - With the help of constructor we can initillize non-static members during the object creation.
  - <br>
  
  **5) What is difference between constructor and method ?**
  <br>
| No |                               Constructor                              |                   Method                  |
|:--:|:----------------------------------------------------------------------:|:-----------------------------------------:|
| 1. |               Constructor must have same name as a class.              |    We can give any name to the method.    |
| 2. |               Constructor does not have any return type.               |          Method have return type.         |
| 3. | Constructor is called only once at the time of during object creation. | Method can be called any number of times. |

