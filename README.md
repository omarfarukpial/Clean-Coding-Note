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
