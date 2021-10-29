#My insight how the JavaScript engine works. By Samuel Abebe
  
  
  we all know JavaScript is a higher-level language which means it is written by using human language instead of machine languages which is used by lower- level programing languages like C and assembly. So how our language(syntax) can be changed in the way that the machine can understand? That is where JS Engine comes. JS Engine is an interpreter of human language to machine language or bytecode. Different web-browser engine companies use their own JS Engine for example Chrome uses V8 Mozilla uses Spider Monkey and so on.
 Now let see how JS Engine works and the layouts of each component. When we write our code on our IDE, we use example.js file which is still documented in human readable language. After this point there are so many components that makes our document readable to our machine for now let us see each of them in short.

Parser:-
This part of the JS Engine is documented by JS Tokens (this are kind of syntax) and the parser monitor if our JS file holds a token as a variable name because it can make it complicated to understand for the next fundamental step which generating AST (abstract syntax tree) which is very helpful documentation of the document for the next step. AST is generated in some fixed parameters in such a way that every syntax will have its own parameter values. After this stage the data will to the most interesting parts of JS Engine that is compilation. let see this magic below

Compilation:-
  JS Engine compilation is mostly known as Just in Time Compilation which uses both interpreter and compiler at the same time. I think this makes JavaScript special because as we all know some programing languages use only interpreter so that our code file will be executed right away but line by line which makes is very slow along the way and it is not efficient. On the other hand, programing languages that uses only compiler on their Engines will execute efficiently but it is too slow because it needs to read all the file first and send to executor. So how this incredible JS compilation work?
  In JS Engine compilation after the data pass the parser it will enter to an interpreter, the interpreter  will do two jobs here that is sending the code to the executor line by line (as it always do) and send the data to the compiler so that the compiler will optimize the code and if the compiler did not finish reading the data form the interpreter it will send back optimized code to the interpreter until it finishes reading and send its optimized code to executor. Optimized code is nothing but a code file without the space and comment and other non-useful codes which completely break their links with their family node.
  After this stage the optimized data will go to its final stage called execution stage. Let see this stage in little detail.

Execution:-
This part has two main parts which is heap memory and call stack. On JS execution process all our interpreted optimized data will store in heap memory, here the most interested part for me is garbage collector. It is on the heap memory that stored all left-out information from the optimization process (off course they are information too). And JS use its execution process in call-stack method which means first in last out. Alright this all about JS Engines see you next time.







