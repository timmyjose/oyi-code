Tue Dec  1 19:16:27 IST 2020

* A minimal set of features I'd like to see in Oyi:
  - Java-like syntax (wouldn't mind changing to Pascal-like declaraion syntax if that makes things easier)
  - Refinement types
  - Linear Types
  - as much functional programming support as possible
  - a good module/package/namespace system

Sat Dec  5 20:15:45 IST 2020

* One of the biggest pain-points in other languages (C, Common Lisp, Haskell, and Idris in particular) is the module/package/namespace feature.
  Oyi needs to have a sane and workable module/package/namespace system.

* Parsing strategies (in order of preference from highest to lowest, based on extensive research):
  * PEG RD parsing
  * GLR
  * LALR
  * LL(k)

  In each case, there might be a need for an extra pass /multiple extra passes to resolve semantic context-sensitive conflicts.

  The idea is to study real-world programming languages - Zig, Python, C, Java, Dlang for inspiration and ideas.


Sun Dec 27 18:54:24 IST 2020

* Some additional must-have features:
  * Pattern Matching (a la Rust)
  * Iterators (a la Java/Rust)


Mon Jan  4 12:29:08 IST 2021

* Parsing is decided as a PEG-inspired ad-hoc RD parser.

* An FFI mechanism is absolutely needed for Oyi. This will, of course, be C-FFI.
  * LLVM bindings (or any other backend) will need native/C++ bindings. Even if the LLVM part of the 
    codebase is rewritten to use Oyi, that code will still need FFI to communicate with the C++ part.

* Instead of an OOP system, a trait-like system would be useful. This will also tie in nicely with the
  Iterators paradigm mentioned previously. This would be similar to Rust's traits system.