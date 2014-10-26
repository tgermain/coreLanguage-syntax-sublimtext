coreLanguage-syntax-sublimtext
===============================

core language syntax and snippet for sublime text


TODO
-----
- understand how the symbolList definition work
- Snippets, MORE snippets


Done but not perfect
----
- embedding C code highLighting



Grammar supported (yet):
----
```js
core:
  | top*
top:
  | "Task" ID ( C-params ) { stmt* }
  | "Reset" { stmt* }   
              
stmt:
  | #> C-code <#                                  
  | "async" after? before? ID ( C-params ) ;             
  | "sync" ID ( C-params ) ;
  
after:
  | "after" time                              

before:
  | "before" time          

time:
  | INTVAL tunit?

tuint:
  | "us" | "ms" | "s"    
  ```
