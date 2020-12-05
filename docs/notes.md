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