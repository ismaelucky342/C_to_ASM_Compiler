# C to ASM_Compiler
Our own version of a C to assembly compiler

# **Project Structure:**

#### 1. Lexical Analysis (Lexer)
- lexer.c: Implements lexical analysis. This file contains the functions that read the source code and split the text into tokens.
- lexer.h: Header file to declare the functions and structures related to the lexer (for example, structures for the tokens).
#### 2. Syntactic Analysis (Parser)
- parser.c: Implements syntactic analysis (AST construction). This file contains the functions that process the tokens and generate the abstract syntax tree (AST).
- parser.h: Header file that contains the AST structures and the declarations of functions related to the parser.
#### 3.  Abstract Syntax Tree (AST)
- ast.c: Implements the functions that build and manipulate the AST (such as adding nodes, freeing memory, etc.).
- ast.h: Header file with the definition of the AST structures (nodes, operators, expressions, etc.) and the functions to work with it.

#### 4.  Semantic Analysis
- semantic_analysis.c: Implements functions to check types, detect semantic errors (e.g., using undeclared variables), and validate operations in the code.
- semantic_analysis.h: Header file for functions and structures related to semantic analysis.

#### 5. Intermediate Code Generation
- intermediate_code.c: Generates intermediate code that can be easier to manipulate and optimize before generating the final Assembly code.
- intermediate_code.h: Header file with the functions and structures to generate the intermediate code.

#### 6. Assembly Code Generation
- codegen.c: Converts the AST or intermediate code into Assembly code for the target architecture.
- codegen.h: Header file with the definitions of the Assembly code generation functions.
#### 7.  Optimization
- optimizer.c: Implements optimizations (e.g., removing redundant code, reducing unnecessary instructions, etc.).
- optimizer.h: Header file for the code optimization functions.

#### 8.  Error Handling
- error_handling.c: Handles error detection and reporting in both the lexical, syntactical, and semantic analysis phases.
- error_handling.h: Header file for declaring error-related functions and structures.

#### 9.  Main File
- main.c: Entry point of the compiler. Reads the input file, invokes the lexer, parser, semantic analysis, optimization, and code generation.

#### 10. Common Utilities and Structures
- utils.c: Common helper functions that can be used in different parts of the compiler (e.g., memory management, string handling, etc.).
- utils.h: Header file for common functions and definitions.

#### 11. Common Structures and Types
- types.h: Defines data types and structures used throughout the compiler, such as token structures, ASTs, and other common elements.

#### 12.  Makefile
- Makefile: Defines how to compile the project, dependencies between files, and cleanup and compilation commands.

#### 13. Test Files
- tests/: Directory where you can have several test C files to verify that the compiler works correctly.
test1.c, test2.c, etc.: C code files to validate the different phases of the compiler.
run_tests.sh: Script to run the tests automatically.
