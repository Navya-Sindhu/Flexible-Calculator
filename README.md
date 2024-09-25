**Flexible-Calculator**

**Overview:**      
This is a simple and extensible calculator application written in Java. It supports basic operations like addition, subtraction, multiplication, and division. Additionally, one can perform multiple operations in a sequence using the chaining functionality. This project follows clean coding practices and is structured to allow new operations to be added easily without modifying existing code.

**Features:**         
Basic Operations    : Supports ADD, SUBTRACT, MULTIPLY, and DIVIDE.   
Chaining Operations : Allows performing multiple operations one after another.   
Error Handling      : Handles invalid inputs and cases like division by zero gracefully.   
Extensibility       : New operations can be added without changing the existing logic.

**Project Structure:**      

FlexibleCalculator

├── src   

     └── main/
     
          └── java/
          
        -      └── com/
        
                    └── calculator/
                    
                         ├── Calculator.java
                         ├──  Operation.java
                         ├──  Main.java
                         ├──  operations/
                             - AddOperation.java
                             - SubtractOperation.java
                             - MultiplyOperation.java
                             - DivideOperation.java
                         ├── exceptions/
                               └──InvalidOperationException.java

├── test/
     
     └── java/
     
          └── com/
          
              └── calculator/
              
                   └── CalculatorTest.java

          
**How to Run:**
Prerequisites - Java 8+

**Steps:**

1. Clone the Repository:
   git clone <repository-url>
   cd FlexibleCalculator
2. Compile the Project: Navigate to the src/main/java folder and compile the classes
   javac com/calculator/*.java com/calculator/operations/*.java com/calculator/exceptions/*.java
3. Run the Application: Execute the Main class:
   java com.calculator.Main  
4. Choose Between Modes:
   You can perform single operations or use the chaining feature by selecting the desired mode in the terminal.

**Code Explanation:**   
1. Calculator.java    : The core logic to handle operations and chaining.   
2. Operation Enum     : Defines the operations like ADD, SUBTRACT, etc.   
3. Main.java          : Entry point for the application. It handles user input and interaction.   
4. Operations Package : Contains the implementation of each mathematical operation.   
5. Exceptions Package : Handles invalid operations.

**Time Complexity:**   
1. Basic Operations : Each operation (addition, subtraction, etc.) runs in constant time, i.e., O(1).
2. Chaining Mode    : Time complexity for chaining is O(n), where n is the number of operations in the chain.

**Testing:**    

I've written basic unit tests to cover normal and edge cases, like:   
1. Performing basic calculations.   
2. Chaining operations.  
3. Handling division by zero.

To run tests, simply use JUnit (or any testing framework) in your IDE or manually by running the CalculatorTest.java file.

**Testing Assumptions**   
1. JUnit tests are provided to ensure that each arithmetic operation works as expected.
2. Each operation class is tested for various inputs, including edge cases.
3. Input validation checks are in place to handle invalid operations gracefully.
