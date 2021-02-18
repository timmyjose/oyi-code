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


Mon Feb  1 14:20:43 IST 2021

  * I have almost finalised on basing Oyi on LOGO. Basically, the core language will be a modified version of LOGO with static-typing, possibly no dynamic scoping,
    and strong type inference. Any or all of this is liable to change though. Reference: The History of LOGO.


Thu Feb 18 11:40:26 IST 2021

  * I will probably create a Stack Machine as a backend for Oyi first, and use that to flesh out the core language. The code generator should be modular enough to 
    easily swap out (retire/delete/maintain/update) this backend as Oyi is ported over to LLVM (and other backends in the future). 

    This is a bit of an initial cost, but I think it will actually help improve the quality of the core language.

  * To start off with, I plan to create a specification for Oyi in the spirit of the Triangle language specification (Watt & Brown, PLPJ, Appendices B and C).