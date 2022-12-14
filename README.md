# Along

**WIP! DRAFT!**

Along is the ideal programming language for me.


## Language design

- Designed to get along with program change and growth
- Interpreted and compiled (assembly or llvm)
- Produce fast programs with small memory footprint
- Fast compiler and feedback loop
- C interop?
- Repl or the tool to play with language with minimal hassle
- Debugging
- No preference to OOP or Func or other styles, but the tool for enabling those styles
- Powerful one liners
- Composable out of small primitives
- Async in mind; extensible to other effects in mind
- The syntax and other features should enable the DSLs
- Homoicony or lisp like simplified, but concise and explicit syntax without lispy brackets
- Get ideas for simplicity from the stack based languages e.g. Forth
- Low level and direct memory management with the gradual safety improvements
- Type inference
- Everything is expression - last result returned
- Multiple and named returns without tuples
- Extend everything and solved "expression problem"
- No semicolons!
- Pipeline operator and postfix variable binding in the midst of pipeline
- Generics
- Type aliases
- Functional types in std lib
- Macros and tools to extend the language by users
- Compile-time programing in itself
- No build system or the builds in itself
- Simple packages
- Pay-for-play - the simplest things should be simple
- Power-to-the-people - no blocking the unsafe features, just make them "guarded" by whatever means
- Prolog like solver as the natural language part
- Literate programming and docs with live examples


## Sample

main.alg
```

main:
 fib(4)@result | console("Fib 4th is ", result)

fib: n u32 -> result u32:
 result = if n < 1: n, fib(n - 1) + fib(n - 2)
 
fib2: n u32 -> u32:
 if n < 1: n, fib(n - 1) + fib(n - 2)

answer::42

*answer should be 42:
  answer ==? 42 // ==? is assert

*test small sequence:
  for(1, 1, 2, 3, 5, 8)@expected, i: expected ==? fib(i)
```

## TBD

- [ ] Interpret the sample program in rust
