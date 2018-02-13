# Chapter 1: What is a Scope?

**Scope**: A well-defined set of rules for storing variables in some location and finding those variables at a later time.

##### The 3 steps before execute
1. **Tokenizing/Lexing**: Breaking up a _string_  of characters into meaningful _chunks_, called **tokens**.  
  :     var a = 2;        -->     var, a, =, 2, ;.  
(Whitespace will only be persisted as a token when it is meaningful.)

2. **Parsing**: Taking a _stream_ (array) of tokens and turning it into a tree of nested elements, which collectively represent the grammatical structure of the program. This tree is called an "**AS**T" (**A**bstract **S**yntax **T**ree).  
  :     var a = 2;        -->     The tree for var a = 2; might start with a top-level node called VariableDeclaration, with a child node called Identifier (whose value is a), and another child called AssignmentExpression which itself has a child called NumericLiteral (whose value is 2).
