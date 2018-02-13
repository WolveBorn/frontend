# Chapter 1: What is a Scope?

**Scope**: A well-defined set of rules for storing variables in some location and finding those variables at a later time.

##### The 3 steps before execute
1. **Tokenizing/Lexing**: Breaking up a _string_  of characters into meaningful _chunks_, called **tokens**.


  :     var a = 2;        -->     var, a, =, 2, ;.  
(Whitespace will only be persisted as a token when it is meaningful.)

2. **Parsing**: Taking a _stream_ (array) of tokens and turning it into a tree of nested elements, which collectively represent the grammatical structure of the program. This tree is called an "**AST**" (**A**bstract **S**yntax **T**ree).


  :     var a = 2;        -->     The tree for **var a = 2;** might start with a top-level node called _VariableDeclaration_, with a child node called _Identifier_ (whose value is **a**), and another child called _AssignmentExpression_ which itself has a child called _NumericLiteral_ (whose value is **2**).
  
  3. **Code-Generation**:


# Les

v.b.    = var a = 2;

**LHS** = **L**eft **H**and **S**ide  
v.b.    = var a

**RHS** = **R**ight **H**and **S**ide  
v.b.    = 2
