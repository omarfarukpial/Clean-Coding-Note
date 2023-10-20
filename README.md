# Clean-Coding-Note
It's a basic notes and resource link for clean coding concepts and some example also.
## Code Conventions Oracle 

Resource Link: https://www.oracle.com/java/technologies/javase/codeconventions-introduction.html

1. Why clean coding is an important concept?
   - Clean code increases the coding readability, reusability and maintainability.
   - Maintaining the standard practice helps in the team work and also for further modification or extension.
2. Some basic conventions
   - A beginning comment can be given inside the class. It will contain **classname, version info, date, copyright notice**
   - Standard indentation should be maintained. Four space is the standard unit.
   - There should be less than 70 char in a line.
3. Wrapping Lines
   - Break after a comma.
   - Break before an operator.
   - Align the new line with the beginning of the expression at the same level on the previous line.
4. Comment Formats
   - Block Comments (provide descriptions of files, methods, data structures and algorithms)
     
         /*
            A block comment
         */
   - Single-Line Comments (descriptive comment in a single line)
     
           if (condition) {/* Handle the condition. */
           }
   - Trailing Comments (very short comment appears at the end of statement)
  
         if (a == 2) {
           return TRUE;            /* special case */
          } else {
           return isPrime(a);      /* works only for odd a */
          }
    - End-Of-Line Comments (single line comment starts with delimiter `//` )
      
          if (foo > 1) {// Do a double-flip.
          }

5. Declarations
    - One line should contain one declarations also contain comment if needed.
    - Local variable should be initialize where it declared. If no calculation needed to initialize.
    - Declaration should be at the beginning of a block. Except `for loop`.
    - For the Class and Interface Declarations following formatting rules are applicable:
        - No space between a method name and the parenthesis `(` starting its parameter list
        - Open brace `{` appears at the end of the same line as the declaration statement
        - Closing brace `}` starts a line by itself indented to match its corresponding opening statement
6. Statements
    - Each line should contain one statement
    - For compound statements the statements should be inside the braces `{ statements }`.
    - `return` statement should not use parentheses unless it is obvious.
    - Conditional statements example

          if (condition) {
            statements;
          }
      
          if (condition) {
            statements;
          } else {
            statements;
          }
      
          if (condition) {
            statements;
          } else if (condition) {
            statements;
          } else {
            statements;
          }
    - Loop statements example

          for (initialization; condition; update) {
            statements;
          }

          while (condition) {
            statements;
          }

          do {
            statements;
          } while (condition);
      
    - try-catch statements

          try {
          statements;
          } catch (ExceptionClass e) {
          statements;
          }
      
          try {
          statements;
          } catch (ExceptionClass e) {
          statements;
          } finally {
          statements;
          }

  7. White Space
      - Blank lines should be added where needed. Two blank line should be added between class and interface definitions and one blank line should be added between methods, variables and blocks.
      - Blank space also should be added to separate keywords inside the paranthesis and the operators.
  8. Naming Conventions
      - Packages (should maintain the oracle package naming convention, all lowercase, start with top-level domain)
        - Examples:  `com.sun.eng` `com.apple.quicktime.v2` `edu.cmu.cs.bovik.cheese`
      - Classes and Interfaces (should be a **noun**, **descriptive** and in  **PascalCase**)
        - Examples: `class ImageSprite;` `interface RasterDelegate;`
      - Methods (should be **verb** and in **camelCase**)
        - Examples: `runFast()` `getBackground()`
      - Variables (should be **self explanatory**, **short** and in **camelCase**)
        - Examples: `myWidth` `area`
      - Constants (should be in all **UPPERCASE**, separeated by **Underscorer**)
        - Examples: `MIN_WIDTH = 4` `MAX_WIDTH = 999`

  9. Programming Practices
      - Be carefull with access modifiers.
      - Avoid creating object of a class to use it's static variables or methods. They can be accessed with only the class name.
      - Use constants where needed.
      - Do not assign multiple variable in a single statement.
      - Use paranthesis inside the equations or conditions if needed.
      - Use ternary operator instade of `if-else`, if it is possible.
  10. Java Code Example by Oracle
      
           /*
           * @(#)Blah.java        1.82 99/03/18
           *
           * Copyright (c) 1994-1999 Sun Microsystems, Inc.
           * 901 San Antonio Road, Palo Alto, California, 94303, U.S.A.
           * All rights reserved.
           *
           * This software is the confidential and proprietary information of Sun
           * Microsystems, Inc. ("Confidential Information").  You shall not
           * disclose such Confidential Information and shall use it only in
           * accordance with the terms of the license agreement you entered into
           * with Sun.
           */
          
          
          package java.blah;
          
          import java.blah.blahdy.BlahBlah;
          
          /**
           *  
                  Class description goes here.
           *
           * @version      
                  1.82 18 Mar 1999  * @author          
                  Firstname Lastname  */
          public class Blah extends SomeClass {
            
                     /* A class implementation comment can go here. */ 
              /**  
                  classVar1 documentation comment */
              public static int classVar1;
          
              /** 
            
                      *  
                  classVar2 documentation comment that happens to be      *  
                  more than one line long      */
              private static Object classVar2;
          
              /**  
                  instanceVar1 documentation comment */
              public Object instanceVar1;
          
              /**  
                  instanceVar2 documentation comment */
              protected int instanceVar2;
          
              /**  
                  instanceVar3 documentation comment */
              private Object[] instanceVar3;
          
              /** 
               * ...
                  constructor Blah documentation comment...      */
              public Blah() {
            
                        // ...implementation goes here...     }
          
              /**
               * ...
                  method doSomething documentation comment...      */
              public void doSomething() {
            
                         // ...implementation goes here...      }
          
              /**
               * ...method doSomethingElse  
                  documentation comment...      * @param someParam  
                  description      */
              public void doSomethingElse(Object someParam) {
            
                         // ...implementation goes here...      }
          }



## Clean Code (A Handbook of Agile Software Craftsmanship) - Chapter 17 - Smells and Heuristics
Resource Link:  https://thixalongmy.haugiang.gov.vn/media/1175/clean_code.pdf

1. Comments
   - C1: Inappropriate Information
      - Meta-data such as authors, lastmodified-date, SPR number, and so on should not appear in comments.
      - If the inforamtion can be hold in different kinds of system such as source code control system, issue tracking system or any other record keeping system then it should not be in comment.
      - Comments should be reserved for technical notes about the code and design.
   - C2: Obsolete Comment
      - Old, irrelevant and incorrect commnet should not be present.
      - Such comment should be updated or removed.
   - C3: Redundant Comment
      - If the code describe itself then no need to write comment.
        
              i++; //increment i
   - C4: Poorly Written Comment
      - Choose words carefully.
      - Grammar and punctuation needs to be accurate.
   - C5: Commented-out code
      - If a code portion is commented out. Then that code should be removed.
      - Commented-out code's example

              //for (int i = 0; i < n; i++) {
              //   sum += i;
              //}
              // Remove this code portion...
2. Environment
   - E1: Build Requires More Than One Step
      - The building process should not be complicated, just one simple command should do the work.
      - Almost every environment has simple build cmd, if it is not there then we can create using bash script (.sh in Linux) or batch file (.bat or .cmd in Windows).
   - E2: Tests Requires More Than One Step
      - Test command should be also easy and simple.
      - Most of the case IDEs provide the button to run all the test. But if it is not there, then a simple shell command should be created to run all the test at once.
3. Functions
   - F1: Too Many Arguments
      - Function or method should not have more that three argument.
      - If it is more than three then try to pass all the argument inside as an object. 
      - Or break the function into separate function if it is possible.

        If your method looks like this,

               public void insertPersonData(String UUID, String name, String email, String phone, String address) {
                 // Logic to insert person data into database
                }

        Then change it to this,
        
              public void insertPersonData(Person person) {
                 // Logic to insert person data into database
              }
   - F2: Output Arguments
      - Generally arguments are expected to be used as input. Such as:

              public void addFooter(String footer) {
                 // footer will be added to a document or report.
              }

        In this example the argument footer is an input and it is going to add as a footer on a different file.
      - But in some cases arguments can act as a output. Then the state should be changed. Example:

              public void appendFooter(Report report) {
                 // A new footer will be added to report document.
              }

        In this example the argument report is acting as an output file. A footer is going to be added inside the report document.
        In this case, we can use something like this for clean code,
    
              Report report = new Report();
              report.appendFooter();

        The appendFooter method should be implemented in Report class.
   - F3: Flag Arguments 
      - If a function takes boolean arguments then it is doing more than one task. If the argument is `true` then one task and if `false` then another task.
      - For this scenerio we need to separate that function in two.
      - Example:

              public void person(boolean isTeacher) {
                 if(isTeacher) System.out.println("Lunch will be provided.");
                 else System.out.println("Lunch will not be provided.");
              }
        
              public static void main() {
                 person(true);
              }

        Indeed this is a bad practice. Inside the main() nobody will understand what the person(true) is doing.       
        We should modify this code as,

              public void personAsTeacher() {
              System.out.println("Lunch will be provided.");
              }
        
              public void personAsStudent() {
              System.out.println("Lunch will not be provided.");
              }
        
        Now we can call them separately.
   - F4: Dead Function
        - Functions that are no longer being used or called is known as dead function.
        - Dead functions should be discarded.

4. General
   - G1: Multiple Languages in One Source File
      - A single file can contain multiple language. But the standard practice is one file should contain only one language.
      - This README.md file supports Markdown and HTML both at the same time and it works fine. But I decide to use only Markdown for standard practice. 
   - G2: Obvious Behavior Is Unimplemented
      - What is obvious for a funtion, that should be implemented.
      - Example:
        Suppose I have a function that search by movie names,

              public List<Movie> searchByTitle(String title) {
              // Searching logic
              }
         
        Here title matching should not be case sensitive. User can search movies in uppercase, lowercase or how ever he want. But our function should handle this.
        And this is an Obvious behaviour that should be implemented.
   - G3: Incorrect Behaviour at the Boundaries
        - Boundary condition means basically the corner cases for a method or function.
        - We have to be carefull about every possible corner cases and exceptions.
        - Always write test cases that contains corner cases as much as possible.
        - Example:
      
                public void oddEven(int number) {
                   if (number % 2 == 1) System.out.println("Odd");
                   else System.out.println("Even");
                }
           This code snippet seems works fine. Even for test cases like `10`, `3`, `0`;
          But what about negative numbers? What if test case is like `-10`, `-3` ? Clearly this code won't show correct behaviour. We have to modify this code like,
  
                public void oddEven(int number) {
                   if (number % 2 == 0) System.out.println("Even");
                   else System.out.println("Odd");
                }
          Now this code behaves accurately.
          
   - G4: Overridden Safeties 
         - Don't ever override any method that is related to safety, unless you are an expert.
         - Turning off or ignoring the compiler warning is not a good thing either.
   - G5: Duplication
        - DRY (Don't repeate yourself).
        - If any code repeates again and again then separate the code inside a method or probably another class can be implemented.
        - In some cases like conditions `if-else` if the similar code repeats again and again then polymorphism can be applied.
        - Template or Strategy pattern can be implemented also. 
   - G6: Code at Wrong Level of Abstraction
        - Base class is known as higher level and derived class is known as lower level.
        - We have to choose the methods or variables smartly in higher level and lower level.
        - Higher level should contains only the general implementations and lower level should contains detail implementations.
        - Example (from book):
      
                public interface Stack {
                   Object pop() throws EmptyException;
                   void push(Object o) throws FullException;
                   double percentFull();
                }
          This is a higher level implemetntation but the percentFull() method should not be present here. It shows a wrong level abstraction.
          For example, if I use this Stack interface to keep books of a library then the percentFull() is needed,
          but if I use this Stack to keep some digital items like serial number, then the percentFull() has no need there.
          In simpler word percentFull() is sort of detail level implementation, so it should be in the lower level not in the heiger level.
   - G7: Base Classes Depending on Their Derivatives
      - Base class always should be independent.
      - Base class should not know anything about derived classes.
      - If it is needed to modify anything in the base class to make changes in derived class then it is a bad practice.
   - G8: Too Much Information
      - A class or interface should not have too much methods.
      - If there is a scope to create a separate class then create it.
   - G9: Dead Code
      - Delete all the dead codes.
      - If there is a statement inside the `if-else` or `try-catch` block that will never be executed, then that statement is known as a dead code.
   - G10: Vertical Separation
      - Variables and function should be defined close to where they are used.
      - Local variables should be declared just above their first usage and should have a small vertical scope.
      - Private functions should be defined just below their first usage. 
   - G11: Inconsistency
      - Always maintain the consistency of your coding style.
      - It is better to follow the standard practice to be consistent.
      - Variable or methods name can be consistent like, `getMovieByTitle()`, `getMovieByCategory()`.
   - G12: Clutter
      - Clutter means a file that is filled up with some unused code, unnecessary comments, or methods that is no longer in use.
      - Keep your source files clean, well organized, and free of clutter.
   - G13: Artificial Coupling
      - If a variable, method (e.g. static) or constant use in general purpose, then these things should not be declared in a specific purposed class.
      - Make sure that they are placed properly so that everyone can findout them easily.
      - For constants we can simply create a class named **Constants** where every constants will be placed.
   - G14: Feature Envy
      - A method should not be interested in other class's methods or variables.
      - But in some cases feature envy can be done.
      - Examples (from book):

              public class HourlyPayCalculator {
               public Money calculateWeeklyPay(HourlyEmployee e) {
                  int tenthRate = e.getTenthRate().getPennies();
                  int tenthsWorked = e.getTenthsWorked();
                  int straightTime = Math.min(400, tenthsWorked);
                  int overTime = Math.max(0, tenthsWorked - straightTime);
                  int straightPay = straightTime * tenthRate;
                  int overtimePay = (int)Math.round(overTime*tenthRate*1.5);
                  return new Money(straightPay + overtimePay);
                }
              }
          Here,  `calculateWeeklyPay` is frequently reaching the `HourlyEmployee` class to access its variables and methods. This should not be done.
        We can simply put the `calculateWeeklyPay` method inside the `HourlyEmployee` class.

         But there are some cases, where **Feature Envy** is acceptable. Let's see the following code,

        
              private HourlyEmployee employee ;
              public HourlyEmployeeReport(HourlyEmployee e) {
                this.employee = e;
              }
              String reportHours() {
                return String.format(
                "Name: %s\tHours:%d.%1d\n",
                employee.getName(),
                employee.getTenthsWorked()/10,
                employee.getTenthsWorked()%10);
              }

        Here, the `reportHours()` should not be placed inside the `HourlyEmployee` class, that breaks the principles of OOP concepts.
     
        So, here **Feature Envy** is okay.

  - G15: Selector Arguments
     - If a method behaves differently based on its argument then it is a bad practice and the argument is known as **Selector Arguments**
     - **Selector Arguments** can be `boolean`, `enums`, `Integer` or anything that controls the method's functionality.
     - Example (Same as **Boolean Argument** section):

             public void person(boolean isTeacher) {
                 if(isTeacher) System.out.println("Lunch will be provided.");
                 else System.out.println("Lunch will not be provided.");
              }
        
              public static void main() {
                 person(true);
              }
         In this example, `isTeacher` argument is controlling the `person` method's behaviour.
       Hence there is a scope to split the method like,

           public void personAsTeacher() {
              System.out.println("Lunch will be provided.");
           }
     
           public void personAsStudent() {
              System.out.println("Lunch will not be provided.");
           }
  - G16: Obscured Intent
     - A code should be expressive as possible. It should not be obscured.
     - Example(from book):

             public int m_otCalc() {
                return iThsWkd * iThsRte +
                (int) Math.round(0.5 * iThsRte * Math.max(0, iThsWkd - 400));
             }
       This code is a perfect example of Obscure, nothing can be understandable form here.

       We had to write the code like this,

             public int calculateOvertimePay() {
                int basePay = hoursWorked * hourlyRate;
                int overtimeHours = Math.max(0, hoursWorked - 400);
                int overtimePay = (int) Math.round(0.5 * hourlyRate * overtimeHours);
                int totalOvertimePay = basePay + overtimePay;
                return totalOvertimePay;
            }

   - G17: Misplaced Responsibility
      - Where a code block, variables or method should be placed is a concern.
      - Make the placement easily assumeable for code reader.
      - Example: Where the `PI` constant should be placed? Inside the `Math` class?
              Or in `Trigonometry` class? Naturally, `PI` should be with the trigonometry functions.

   - G18: Inappropriate Static
      - If a method can be polymorphic then it should not be **Static**.
      - If a method operates on a perticular object then it should not be **Static**.
      - Example:
   
              Animal myDog = new Dog();
              Animal myCat = new Cat();
        
              myCat.makeSound();
              myDog.makeSound();
        
         In this code, `makeSound` operates on `myCat` or `myDog`. Also it is polymhorphic.
        So, this method should not be **Static**.

   - G19: Use Explanatory Variables
      - Breaking a calculation into a intermediate values inside a variable is known as **Explanatory Variable**
      - Example:

              public int calculateOvertimePay() {
                int basePay = hoursWorked * hourlyRate;
                int overtimeHours = Math.max(0, hoursWorked - 400);
                int overtimePay = (int) Math.round(0.5 * hourlyRate * overtimeHours);
                int totalOvertimePay = basePay + overtimePay;
                return totalOvertimePay;
               }

        Here, the equation can be written in one line. But standard practice is to use such intermediate variables.

   - G20: Function Names Should Say What They Do
      - Write method such that reader can understand what the method do, by just seeing its name.
      - Example: `calculateBmi(height, weight)`, `addMovie(movie)`.
   - G21: Understand the Algorithm
      - Understand the problem first then think about algorithm.
      - Passing the test cases is not enough. (`if-else` statement can also work in some cases but it does not work everywhere).
      - If there is an scope to optimize, then try it.
      - If the feature can be extended then the algorithm should support that.
   - G22: Make Logical Dependencies Physical
      - If a module is dependent on other module. Then the dependent module should not make assumption rather it should ask that module explicitly.
      - Logical dependency:

              public class Rectangle {
                 double length;
                 double width;
                 public double calculateArea() {
                    return length * width;
                }
            }

       
        In this code, the Rectangle class is responsible for both storing the dimensions of the rectangle and calculating its area.
        This is a logical dependency because the Rectangle class assumes the responsibility of area calculation.
      - Physical dependency:

             public class Rectangle {
                double length;
                double width;
            }
            
            public class AreaCalculator {
                public static double calculateArea(Rectangle rectangle) {
                    double length = rectangle.getLength();
                    double width = rectangle.getWidth();
                    return length * width;
                }
            }

            
        In this code, the Rectangle class is only responsible for storing the dimensions of the rectangle, while the AreaCalculator class is responsible for calculating the area.
       This creates a physical dependency between the Rectangle and AreaCalculator classes, where the Rectangle class explicitly asks the AreaCalculator class to calculate the area when needed. 

   - G23: Prefer Polymorphism to `if-else` or `switch-case`
      - Always look if polymorphism can be applied instade of `if-else` or `switch-case`.
      - Example:
        Let's assume a code like this,

        
            public class ShapeCalculator {
                public double calculateArea(Object shape) {
                    if (shape instanceof Circle) {
                        Circle circle = (Circle) shape;
                        return Math.PI * circle.getRadius() * circle.getRadius();
                    } else if (shape instanceof Rectangle) {
                        Rectangle rectangle = (Rectangle) shape;
                        return rectangle.getWidth() * rectangle.getHeight();
                    } else return 0.0;
                }
            }

     We can easily use polymorphism here,

           class Circle implements Shape {
                @Override
                public double calculateArea() {
                    return Math.PI * radius * radius;
                }
            }


           class Rectangle implements Shape {
                @Override
                public double calculateArea() {
                    return width * height;
                }
            }

      - G24: Follow Standard Conventions
         - Everyone in a team should follow the standard coding conventions.
         - Team's previous code is an example to follow.
       
      - G25: Replace Magic Numbers with Named Constants
         - Where a number or text can be replaced with constants then it should be changed.
      - G26: Be Precise
         - In database query there can be multiple match instade of one.
         - Currency in float or double can lead precision error, so be carefull and handle the rounding effect. 
         - If `List` is enough then no need to apply `ArrayList` there.
         - If a method can return `null` take that in consideration.
      - G27: Structure over Convention
         - Enforce design decisions with structure over convention.
         - Naming conventions are good, but they are inferior to structures that force compliance.
      - G28: Encapsulate Conditionals
         - Use less `boolean` inside the `if-else` or `loop` conditions, as they are hard to understand.
         - Example(form book):
               If a code is like this,

                    
                    if (timer.hasExpired() && !timer.isRecurrent())

           Then we can modify it like this,

                    if (shouldBeDeleted(timer))

      - G29: Avoid Negative Conditionals
         - Most often negative conditionals makes a simple logic more complicated. Think in a simpler way.
         - Example(from book):

                    if (!buffer.shouldNotCompact())
           This code can be easily replaced with,
           
                    if (buffer.shouldCompact())
      - G30: Function Should Do One Thing
         - It is always tempting to write multiple logic into one method.
         - But if there is any scope to separate method then it should be done.
      - G31: Hidden Temporal Couplings
         - In some cases **Temporal Coupling** is needed, but that needs not be hidden.
         - Example(from book):

                  public class MoogDiver {
                      Gradient gradient;
                      List<Spline> splines;
                      public void dive(String reason) {
                         saturateGradient();
                         reticulateSplines();
                         diveForMoog(reason);
                      }
                  }  
           Here the order of the method call is important. `saturateGradient` needs to be called first, after that `reticulateSplines` needs to be called and at last the `diveForMoog` should be called.
           What we can do here is,

                 public class MoogDiver {
                   Gradient gradient;
                   List<Spline> splines;
                   public void dive(String reason) {
                      Gradient gradient = saturateGradient();
                      List<Spline> splines = reticulateSplines(gradient);
                      diveForMoog(splines, reason);
                   }
                  }

            Now all the three methods are in coupling properly.

      - G32: Don't Be Arbitrary
         - Every structure should have a reason.
         - A consistent structure is an example of following the convention.
      - G33: Encapsulate Boundary Conditions
         - If there is a Boundary variable that is appearing multiple time then we should encapsulate that variable.
         - Example:
       
           Look at this sample code,

                 while(index + 1 < upcomingMovieList.length) {
                    daysUntilMovieRelease(index + 1);
                 }

            Assume that the `daysUntilMovieRelease` calculates the remaining date for all the upcoming movies and update in the database.
           Here, `index + 1` indicates the next upcoming movie item.

           But in this code `index + 1` appears two time, hence we can easily encapsulate it like this,

                 nextUpcomingMovieIndex = index + 1;
                 while(nextUpcomingMovieIndex < upcomingMovieList.length) {
                    daysUntilMovieRelease(nextUpcomingMovieIndex);
                 }

        - G34: Function Should Descend Only One Level of Abstraction
           - The statements inside a method should be at the same level of abstraction.
           - If there is a scope to separate or extract new method or class from this then it should be done.
           - Example (from book):

                   public String render() {
                     StringBuffer html = new StringBuffer("<hr");
                     if(size > 0)
                      html.append(" size=\"").append(size + 1).append("\"");
                     html.append(">");
                     return html.toString();
                   }

             In this code there are lots of scope for abstraction.
             Basically, the code is creating a new string for `hr` html tag.
             But, a size attribute is present there.
             if the `size = 5` then the output of this code will be like,

                   <hr size = "6">

             Here the size defines the height of the `hr` tag. 
             But what we can do here,

                   public String render() throws Exception {
                      HtmlTag hr = new HtmlTag("hr");
                      if (extraDashes > 0)
                          hr.addAttribute("size", hrSize(extraDashes));
                      return hr.html();
                  }
                  
                  private String hrSize(int height) {
                      int hrSize = height + 1;
                      return String.format("%d", hrSize);
                  }


             Here the `HtmlTag` class handles all the syntax to create `hr` tag also the `hr.addAttribute` method is used to add attribute inside the `hr` tag.
             `addAttribute` takes two arguments one is the attribute name and another is it's value.
             Here the value of attribute is `hrSize(extraDashes)`. Here the value of size being calculated from `extraDashes` inside the `hrSize` method.

             So, the abstractions are applied in two position here,
             One is for constructing the `hr` tag, and another is for calculating the size of `hr`.

         - G35: Keep Configurable Data at High Levels
            - If the code have some configuration values (port number, database credintials, path etc) then place them in higher level.
            - Example:
          
                 Suppose we have some default value. So we can put it in a class, 

                     public class FitNesseConfig {
                         public static final String DEFAULT_PATH = ".";
                         public static final String DEFAULT_ROOT = "FitNesseRoot";
                         public static final int DEFAULT_PORT = 80;
                         public static final int DEFAULT_VERSION_DAYS = 14;
                     }

              Now, in the lower level we can use these,

                     public static void main(String[] args) {
                         Arguments arguments = parseCommandLine(args);
                         int port = (arguments.port == 0) ? FitNesseConfig.DEFAULT_PORT : arguments.port;
                     }

              Here we are using `DEFAULT_PORT` variable instade of using `80` directly.
              This approach help dramatically in the refactoring process. If we want to change anything in the configuration
              or in the default value, then we just need to change only once. 


         - G36: Avoid Transitive Navigation
            - Transitive Navigation means A module knows much about it's collaborators.
            - Example(from book):

                    a.getB().getC().doSomething();

              Here, Module A knows it's collaborator B and C. That should not be happen.
              Suppose if a new collaborator Q comes between B and C then it may need to convert like this,


                     a.getB().getQ().getC().doSomething();

              The architecture become rigid now.

              It's always better to code like,

                    myCollaborator.doSomething();


   
   5. Java
      - J1: Avoid Long Import Lists by Using Wildcards
         - We can use wildcards to import packages

                 import package.*;
           Here, `*` means all the packages.
           We can use

                 import java.utils.*;
           This line imports all the utility packages.

      - J2: Don’t Inherit Constants
         - Constants do not meant to be inherited.
         - We can import static to import constants.
       
      - J3: Constants versus Enums
         - Enums are very powerfull with it's built-in method or tools.
         - Enums attach a name with it, so it can not get lost.
         - Enums replaces `public static final` before the variable declaration.
   6. Names
      - N1: Choose Descriptive Names
         - Variable's name should be descriptive and self explanatory.
         - Descriptive names increases the readability and understandable.
      - N2: Choose Names at the Appropriate Level of Abstraction
         - For a variable inside higher level, names should be choosen carefully.
         - Example(from book):

                 public interface Modem {
                   boolean dial(String phoneNumber);
                   boolean disconnect();
                   boolean send(char c);
                   char recv();
                   String getConnectedPhoneNumber();
                  }

           Here the `dial` takes `phoneNumber` string but, as a modern modem it can connect without phone number, it can connect with wire or port number.
           So, instade of phone number we can use more generalize variable name here.

                 
                 public interface Modem {
                   boolean dial(String connectionLocator);
                   boolean disconnect();
                   boolean send(char c);
                   char recv();
                   String getConnectedLocator();
                  }

           Here we write it as a connection locator. Although the previuos code would work fine, but we just make the name generalized.
           Not limited to phone number only.


      - N3: Use Standard Nomenclature Where Possible
         - Java has some standard naming pattern, it's good to follow that.
         - Example(from book): 

              If you are using Decorator pattern in java, then `AutoHangupModemDecorator` can be used to decorate the `Modem` class.

      - N4: Unambiguous Names
         - Names should clearly say what it do.
         - Example:

                 public void rename() {
                    for (episode : episodesList) {
                        doRename(episode);
                    }
                 }

            Here the `rename` or `doRename` doesn't clearly says what it do mainly.
           But we can easily refactor these names like,


                 public void renameAllEpisodes() {
                    for (episode : episodesList) {
                        renameEpisode(episode);
                    }
                 }

      - N5: Use Long Names for Long Scopes
         - Name of a variable should related with the name of the length of the scope.
         - For small scope, we should think that if there is any need of large name?
         - Such as,

                 for (int i = 0; i < movie.length; i++) {
                     //Some small 1 or 2 line simple logic
                 }
            Here, `i` is dennting the index, as the scope is small so we can keep `i` here, no need to replace it with a long name.

      - N6: Avoid Encodings
         - Name should not be encoded with types or scope.
         - Previously some prefix like `m_` or `f` was handy but now it is useless.
      - N7: Names Should Describe Side-Effects
         - If a method do more than what it says in the name, then we need to modify that.
         - Names should describe the method's job in single word.
         - Example:

                  public void updateMovie(Movie updatedMovie) {
                     if (movieNotExistsById(updatedMovie.getId)) {
                        //Create a new Movie then set all the element form updatedMovie
                     } else {
                        // Update the movie
                     }
                  }
           This code not just updating movie, it first checks that if the movie exists or not by id,
           if not exits then create and save it.
           So the name should be like, `updateOrCreateMovie`

   7. Tests
      - T1: Insufficient Tests
         - There is no standard definition of sufficient test.
         - We should think about maximum corner cases.
       
      - T2: Use a Coverage Tool
         - Coverage tools creates some marks indicating that how much a test has covered.
         - It becomes handy to see if all the portion is tested or not.
       
      -  T3: Don’t Skip Trivial Tests
         - We should not every skip tests even if they are easy or obvious.
         - Keeping that test cases helps us in documentation and test coverage checking.
       
      - T4: An Ignored Test Is a Question about an Ambiguity
         - A test that is commented out or annoted with `@Ignore` can lead ambiguity.
         - We should get rid of these.
      - T5: Test Boundary Conditions
         - We should be more carefull about corner cases.
      - T6: Exhaustively Test Near Bugs
         - If we find a bug, we should run exhaustive test on that block. There is a high chance of finding multiple bug in that block.
      - T7: Patterns of Failure Are Revealing
         - Pattern of failed test cases can also help us in debug.
         - Such as, we have wrote a program that add two integer, but when we are testing the result is like,
           `(3, 5) = 15`, `(2, 7) = 14` or `(5, 6) = 30`.
           We can understand that we multiplied instead of summation. We need to check the equation again. 
(To be continued...)
