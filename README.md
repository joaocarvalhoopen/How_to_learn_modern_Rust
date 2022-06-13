# How to learn modern Rust
A guide to the adventurer.

Table of Contents
=================

   * [Learn Rust deeply one step after the other](#learn-rust-deeply-one-step-after-the-other)
   * [Text Processing in Rust](#text-processing-in-rust)
   * [How Rust maps to memory and lifetimes annotations in Rust](#how-rust-maps-to-memory-and-lifetimes-annotations-in-rust)
   * [How to deal with Circular References and Ownership](#how-to-deal-with-circular-references-and-ownership)
   * [Polymorphism in Rust](#polymorphism-in-rust)
   * [Rust Testing and TDD - Test Driven Development](#rust-testing-and-tdd---test-driven-development) 
   * [Background in systems programming](#background-in-systems-programming)
   * [Writing Compilers in Rust](#writing-compilers-in-rust)
   * [Contributing to the Rust Compiler rustc](#contributing-to-the-rust-compiler-rustc)
   * [WebAssembly in Rust - WASM](#webassembly-in-rust---wasm)
   * [Python extended with Rust and running a Python interpreter inside Rust](#python-extended-with-rust-and-running-a-python-interpreter-inside-rust)
   * [Rust with inline Python](#rust-with-inline-python)
   * [Rust on or for the Raspberry Pi](#rust-on-or-for-the-raspberry-pi)
      * [Developing on the Raspberry Pi and running Rust programs on the Raspberry Pi](#developing-on-the-raspberry-pi-and-running-rust-programs-on-the-raspberry-pi)
      * [Developing on the PC and cross-compiling to run Rust programs on the Raspberry Pi](#developing-on-the-pc-and-cross-compiling-to-run-rust-programs-on-the-raspberry-pi)
   * [Embedded Rust](#embedded-rust)
   * [Embedded Rust crates and code size optimization](#embedded-rust-crates-and-code-size-optimization)
   * [Embedded Rust with STM32 BluePill - STM32F103](#embedded-rust-with-stm32-bluepill---stm32f103)
   * [Embedded Rust with Raspberry Pi Pico - 4 dollars board](#embedded-rust-with-raspberry-pi-pico---4-dollars-board)
   * [Embedded Rust with ESP32](#embedded-rust-with-esp32)
   * [Links](#links)
   * [Rust Foundation](#rust-foundation)
   * [Rust Blogs](#rust-blogs)
   * [Rust Youtube Channels](#rust-youtube-channels)
   * [GUI programming in Rust](#gui-programming-in-rust)
   * [Audio in Rust](#audio-in-rust)
   * [Faster Compilation - Linker times in Linux and Unix ELF](#faster-compilation---linker-times-in-linux-and-unix-elf)
   * [Machine Learning for Rust](#machine-learning-for-rust)
   * [Rust VSCode plugins](#rust-vscode-plugins)
   * [Rust Debugger](#rust-debugger)
   * [Rust Error Handling](#rust-error-handling)
   * [Tips and Tricks](#tips-and-tricks)
   * [GC for Rust - Garbage Collector](#gc-for-rust---garbage-collector)
   * [Programming Parallel Computers - Optimization guide C Plus Plus and Rust](#programming-parallel-computers---optimization-guide-c-plus-plus-and-rust)
   * [Rust Optimization - Compilation modes and flags](#rust-optimization---compilation-modes-and-flags)
   * [Rust bounds check removal](#rust-bounds-check-removal)
   * [Notes - General](#notes---general)
   * [Notes on optimization](#notes-on-optimization)
   * [Rust substring processing](#rust-substring-processing)
   * [Macros in Rust](#macros-in-rust)
   * [Good way to learn about the topic of computers and programming](#good-way-to-learn-about-the-topic-of-computers-and-programming)
   * [For a good challenge do the NAND To Tetris in Rust](#for-a-good-challenge-do-the-nand-to-tetris-in-rust)
   * [All my other guides](#all-my-other-guides)
   * [Have fun!](#have-fun)  


## Learn Rust deeply one step after the other

Rust is an incredible powerful programming language. It is fast, compiled, without a runtime and it brings new concepts of safety to programming. <br>
It is the most beloved language for five years in a row in Stack Overflow users pool. <br> 
To learn Rust go through the following content **in the listed order**, the majority of the content is free. <br>

1. **Why Developers Love Rust** <br>
   [https://ibraheem.ca/writings/why-devs-love-rust/](https://ibraheem.ca/writings/why-devs-love-rust/)

2. **Video - Rust Crash Course - Rustlang** <br>
   [https://www.youtube.com/watch?v=zF34dRivLOw](https://www.youtube.com/watch?v=zF34dRivLOw)

3. **Video - Introduction to Rust Part 1** <br>
   [https://www.youtube.com/watch?v=WnWGO-tLtLA](https://www.youtube.com/watch?v=WnWGO-tLtLA)

4. **Video - Introduction to Rust Part 2** <br>
   [https://www.youtube.com/watch?v=lLWchWTUFOQ](https://www.youtube.com/watch?v=lLWchWTUFOQ)

5. **A half-hour to learn Rust** - **fasterThanLime Blog** <br>
   [https://fasterthanli.me/articles/a-half-hour-to-learn-rust](https://fasterthanli.me/articles/a-half-hour-to-learn-rust)

6. **Videos - Microsoft Beginner's Series to Rust** <br>
   [https://www.youtube.com/playlist?list=PLlrxD0HtieHjbTjrchBwOVks_sr8EVW1x](https://www.youtube.com/playlist?list=PLlrxD0HtieHjbTjrchBwOVks_sr8EVW1x) <br>
   GitHub Code <br>
   [https://github.com/microsoft/beginners-series-rust](https://github.com/microsoft/beginners-series-rust)

7. **The Tour of Rust** <br>
   [https://tourofrust.com/](https://tourofrust.com/)

8. A Rust experienced developer teaches a C++ experienced developer (Jason Turner) about Rust, from zero. <br>
   **Jonathan Teaches Jason Rust - Part 1 - C++ Weekly** <br>
   [https://www.youtube.com/watch?v=EzQ7YIIo1rY](https://www.youtube.com/watch?v=EzQ7YIIo1rY) <br>
   **Jonathan Teaches Jason Rust - Part 2 - C++ Weekly** <br>
   [https://www.youtube.com/watch?v=Y5-ZgxfQvpc](https://www.youtube.com/watch?v=Y5-ZgxfQvpc)

9. **The Rust Programming Language Book** <br>
   by Steve Klabnik and Carol Nichols, with contributions from the Rust Community <br>
   [https://doc.rust-lang.org/stable/book/](https://doc.rust-lang.org/stable/book/)

10. **Rust Language Cheat Sheet** <br>
    [https://cheats.rs/](https://cheats.rs/)

11. **Rustlings** <br>
    Small exercises to get you used to reading and writing Rust code. <br>
    [https://github.com/rust-lang/rustlings](https://github.com/rust-lang/rustlings)

12. **Videos - Intro to Rustlang - Tensor Programming** <br>
    [https://www.youtube.com/watch?v=EYqceb2AnkU&list=PLJbE2Yu2zumDF6BX6_RdPisRVHgzV02NW](https://www.youtube.com/watch?v=EYqceb2AnkU&list=PLJbE2Yu2zumDF6BX6_RdPisRVHgzV02NW)

13. **Videos - Rustlang Project - Tensor Programming** <br>
    [https://www.youtube.com/watch?v=-Jp7sabBCp4&list=PLJbE2Yu2zumDD5vy2BuSHvFZU0a6RDmgb](https://www.youtube.com/watch?v=-Jp7sabBCp4&list=PLJbE2Yu2zumDD5vy2BuSHvFZU0a6RDmgb)

14. **Standard collections - std info and how to choose the correct collection** <br>
    [https://doc.rust-lang.org/std/collections/index.html](https://doc.rust-lang.org/std/collections/index.html)

15. **Trivia About Rust Types: An Authorized Transcription of Jon Gjengset’s Twitter Thread** <br>
    [https://www.thecodedmessage.com/posts/trivia-rust-types/](https://www.thecodedmessage.com/posts/trivia-rust-types/)

16. **Video - Unsafe & FFI in Rust** <br>
    [https://www.youtube.com/watch?v=LFFbTeU25pE](https://www.youtube.com/watch?v=LFFbTeU25pE)

17. **Rust by Example Book** <br>
    [https://doc.rust-lang.org/rust-by-example/](https://doc.rust-lang.org/rust-by-example/)

18. **Study carefully the methods of ``` Option<T> ``` in the documentation, they are used in all Rust programs** <br>
    [https://doc.rust-lang.org/beta/std/option/index.html](https://doc.rust-lang.org/beta/std/option/index.html)

19. **Study carefully the methods of ``` Result<T, E> ``` in the documentation, they are used in all Rust programs** <br>
    [https://doc.rust-lang.org/beta/std/result/index.html](https://doc.rust-lang.org/beta/std/result/index.html)

20. **Command Line Applications in Rust - Book** <br>
    [https://rust-cli.github.io/book/in-depth/docs.html](https://rust-cli.github.io/book/in-depth/docs.html)

21. **The Rust Standard Library documentation** <br>
    [https://doc.rust-lang.org/std/](https://doc.rust-lang.org/std/)

22. **Learn Rust With Entirely Too Many Linked Lists - Book** <br>
    [https://rust-unofficial.github.io/too-many-lists/](https://rust-unofficial.github.io/too-many-lists/)

23. **Rust Design Patterns - Book** <br>
    [https://rust-unofficial.github.io/patterns/](https://rust-unofficial.github.io/patterns/)

24. **Effective Rust - Book** <br>
    [https://www.lurklurk.org/effective-rust/](https://www.lurklurk.org/effective-rust/)

25. **The Rust Cookbook - Book** <br>
    [https://rust-lang-nursery.github.io/rust-cookbook/](https://rust-lang-nursery.github.io/rust-cookbook/)

26. **The Cargo Book** <br>
    [https://doc.rust-lang.org/cargo/index.html](https://doc.rust-lang.org/cargo/index.html)

27. **Guide trough of the Advent of Code 2020** <br>
    [https://fasterthanli.me/series/advent-of-code-2020](https://fasterthanli.me/series/advent-of-code-2020)

28. **Rust API Guidelines Book** <br>
    [https://rust-lang.github.io/api-guidelines/about.html](https://rust-lang.github.io/api-guidelines/about.html)

29. **The Rust Reference Book** <br>
    [https://doc.rust-lang.org/stable/reference/](https://doc.rust-lang.org/stable/reference/)

30. **The Rustonomicon - The Dark Arts of Unsafe Rust - Book** <br>
    [https://doc.rust-lang.org/nomicon/](https://doc.rust-lang.org/nomicon/)

31. **The Little Book of Rust Macros - Book** <br>
    [https://veykril.github.io/tlborm/introduction.html](https://veykril.github.io/tlborm/introduction.html)

32. **Writing Interpreters in Rust: a Guide - Book** <br>
    [https://rust-hosted-langs.github.io/book/introduction.html](https://rust-hosted-langs.github.io/book/introduction.html)

33. **Video - Cheaply writing a fast interpreter - Neil Mitchell** <br>
    [https://www.youtube.com/watch?v=V8dnIw3amLA](https://www.youtube.com/watch?v=V8dnIw3amLA) <br>
    github <br>
    [https://github.com/ndmitchell/interpret](https://github.com/ndmitchell/interpret)

34. **Make A Language** <br>
    A series about making a programming language called **Eldiro** using the Rust programming language. <br>
    [https://arzg.github.io/lang/](https://arzg.github.io/lang/)

35. **Engineering Rust Web Applications - Book** <br>
    [https://erwabook.com/](https://erwabook.com/)

36. **Programming Rust: Fast, Safe Systems Development 2nd Ed** <br>
    by Jim Blandy, Jason Orendorff

37. **Rust for Rustaceans: Idiomatic Programming for Experienced Developers** <br>
    by Jon Gjengset

38. **Refactoring to Rust** <br>
    by Lily Mara

39. **Practical System Programming for Rust Developers** <br>
    Build fast and secure software for Linux/Unix systems with the help of practical examples <br>
    by Prabhu Eshwarla

40. **Hands-On Concurrency with Rust**: Confidently build memory-safe, parallel, and efficient software in Rust <br>
    by Brian L. Troutwine 

41. **GDB: The GNU Project Debugger** <br>
    [https://www.gnu.org/software/gdb/documentation/](https://www.gnu.org/software/gdb/documentation/)

42. **The LLDB Debugger** <br>
    [https://lldb.llvm.org/](https://lldb.llvm.org/)

43. **Valgrind User Manual** <br>
    [https://valgrind.org/docs/manual/manual.html](https://valgrind.org/docs/manual/manual.html)

44. **The perf Linux profiler - Examples of use** <br>
    [https://www.brendangregg.com/perf.html](https://www.brendangregg.com/perf.html)

45. **QuickCheck - QuickCheck is a way to do property based testing using randomly generated input.** <br>
    [https://github.com/BurntSushi/quickcheck](https://github.com/BurntSushi/quickcheck)

46. **American Fuzzy Lop - A good fuzzer** <br>
    [https://lcamtuf.coredump.cx/afl/](https://lcamtuf.coredump.cx/afl/)

47. **Criterion rs - Statistics-driven Microbenchmarking in Rust** <br>
    [https://github.com/bheisler/criterion.rs](https://github.com/bheisler/criterion.rs)

48. **The Complete Rust Programming Reference Guide**: Design, develop, and deploy effective software systems using the advanced constructs of Rust <br>
	 by Rahul Sharma, Vesa Kaihlavirta 

49. **Creative Projects for Rust Programmers**: Build exciting projects on domains such as web apps, WebAssembly, games, and parsing <br>
    by Carlo Milanesi

50. **Rust High Performance**: Learn to skyrocket the performance of your Rust applications <br>
    by Iban Eguia Moraza 

51. **Writing an OS in Rust Philipp Oppermann's blog** <br>
    [https://os.phil-opp.com/](https://os.phil-opp.com/)

52. **The Rust Unstable Book** <br>
    [https://doc.rust-lang.org/beta/unstable-book/](https://doc.rust-lang.org/beta/unstable-book/)


## Text Processing in Rust

1. **Text Processing in Rust** <br>
   by Mihalis Tsoukalos <br>
   [https://www.linuxjournal.com/content/text-processing-rust](https://www.linuxjournal.com/content/text-processing-rust) 

2. **Working with strings in Rust** - **fasterThanLime** Blog <br> 
   [https://fasterthanli.me/articles/working-with-strings-in-rust](https://fasterthanli.me/articles/working-with-strings-in-rust)

3. **String continuations** <br>
   The backslash, the newline and the starting spaces will disappear. <br>

``` Rust
println!(
    "... the {p}, by the {p}, for the {p}, \
    will never fall.",
    p = "people"
);

Will print: 
"... the people, by the people, for the people, will never fall."
```

4. For **ASCII Strings (value lower then 127) non UTF-8 strings**, one can process **much faster** the string if it is converted to bytes and then compared to bytes. <br>

``` Rust
let my_str = "Hello!".to_string();
for c in my_str.chars() {
    if c == 'l' {
        // Do something!
    }
}

// A faster implementation for ASCII characters would be.

let my_str_2 = "Hello!".to_string();
for b in my_str.bytes() {
    if b == b'l' {
        // Do something!
    }
}

// There is also a slice of bytes.

let my_str_3 = "Hello!".to_string();
let my_str_as_bytes_slice = my_str_3.as_bytes();

if my_str_as_bytes_slice[2] == b'l' {
        // Do something!
}
```

5. **Kibi - A text editor in ≤1024 lines of code, written in Rust** <br>
   [https://github.com/ilai-deutel/kibi](https://github.com/ilai-deutel/kibi)

6. [Rust substring processing](#rust-substring-processing) <br>
   My section below on it.


## How Rust maps to memory and lifetimes annotations in Rust

1. **Video - Visualizing memory layout of Rust's data types - Sreekanth** <br>
   **Incredible video!** <br>
   [https://www.youtube.com/watch?v=rDoqT-a6UFg](https://www.youtube.com/watch?v=rDoqT-a6UFg)

2. **Video - Understanding Rust Lifetimes - Ryan Levick** <br>
   [https://www.youtube.com/watch?v=MSi3E5Z8oRw](https://www.youtube.com/watch?v=MSi3E5Z8oRw)

3. **Video - Crust of Rust: Lifetime Annotations - Jon Gjengset** <br>
   [https://www.youtube.com/watch?v=rAl-9HwD858](https://www.youtube.com/watch?v=rAl-9HwD858)

4. **Implementing a HashMap in Rust.** <br>
   Video - Live-coding a linked hash map in Rust - **Jon Gjengset** <br>
   [https://www.youtube.com/watch?v=k6xR2kf9hlA](https://www.youtube.com/watch?v=k6xR2kf9hlA)


## How to deal with Circular References and Ownership

* **Rust data structures with circular references** <br>
  [https://eli.thegreenplace.net/2021/rust-data-structures-with-circular-references/](https://eli.thegreenplace.net/2021/rust-data-structures-with-circular-references/) <br>
  GitHub **code** <br>
  [https://github.com/eliben/code-for-blog/tree/master/2021/rust-bst](https://github.com/eliben/code-for-blog/tree/master/2021/rust-bst)

The previous link **demonstrated 3 ways to attack the problem**: <br>
<br>
**1-** Defer borrow checking to run-time, by using a reference-counted pointer (```std::rc::Rc```) to a ```std::cell:RefCell```. <br>
<br>
**2-** Centralize the ownership (e.g. all nodes are owned by a vector of nodes in the Tree), and then references become handles (indices into the a vector). <br>
<br>
**3-** Use raw pointers and unsafe blocks to go around the rules of safe Rust. <br>


## Polymorphism in Rust

* **Three Kinds of Polymorphism in Rust - Brandon Smith** <br>
  [https://www.brandons.me/blog/polymorphism-in-rust](https://www.brandons.me/blog/polymorphism-in-rust)

* **Polymorphism in Rust - Matt Oswalt** <br> 
  [https://oswalt.dev/2021/06/polymorphism-in-rust/](https://oswalt.dev/2021/06/polymorphism-in-rust/)

* **Anti-pattern - Deref polymorphism** <br>
  [https://rust-unofficial.github.io/patterns/anti_patterns/deref.html](https://rust-unofficial.github.io/patterns/anti_patterns/deref.html)


## Rust Testing and TDD - Test Driven Development

* Video - Rust Testing and TDD - **An Intro to Testing and Test Driven Development** <br>
  [https://www.youtube.com/watch?v=2vBQFIWl36k](https://www.youtube.com/watch?v=2vBQFIWl36k)


## Background in systems programming

1. **How to learn modern Linux** <br>
   [https://github.com/joaocarvalhoopen/How_to_learn_modern_Linux](https://github.com/joaocarvalhoopen/How_to_learn_modern_Linux)

2. **Safe Systems Programming in Rust** <br>
   By Ralf Jung, Jacques-Henri Jourdan, Robbert Krebbers, Derek Dreyer <br>
   [https://cacm.acm.org/magazines/2021/4/251364-safe-systems-programming-in-rust/fulltext](https://cacm.acm.org/magazines/2021/4/251364-safe-systems-programming-in-rust/fulltext)

3. **The Linux Command Line, 2nd Edition: A Complete Introduction Illustrated Edition** <br>
   by William Shotts

4. **How Linux Works, 3rd Edition: What Every Superuser Should Know 3rd Edition** <br>
   by Brian Ward

5. **Operating Systems: Three Easy Pieces** <br>
   Remzi H. Arpaci-Dusseau and Andrea C. Arpaci-Dusseau <br>
   [http://pages.cs.wisc.edu/~remzi/OSTEP/](http://pages.cs.wisc.edu/~remzi/OSTEP/)  

6. **The Linux Programming Interface: A Linux and UNIX System Programming Handbook** <br>
   by Michael Kerrisk <br>
   **Note:** Read this book from cover to cover!

7. **System Programming Vol I and Vol II** <br>
   by Jin-Jwei Chen <br>
   **Note:** Read this book from cover to cover!

8. **Linux Device Drivers, 3th Edition** <br>
   [https://lwn.net/Kernel/LDD3/](https://lwn.net/Kernel/LDD3/)

9.  **Linux Driver Development for Embedded Processors - 2th Edition**: Learn to develop Linux embedded drivers with kernel 4.9 LTS <br>
   by Alberto Liberal de los Ríos

10. **Computer Systems: A Programmer's Perspective 3rd Edition** <br>
   by Randal Bryant, David O'Hallaron

11. **Computer Networking: A Top-Down Approach** <br> 
   by James Kurose

12. **The Illustrated Network: How TCP/IP Works in a Modern Network 2nd Edition** <br>
   by Walter Goralski

13. **C Programming: A Modern Approach, 2nd Edition** <br>
    by K. N. King

14. **Extreme C: Taking you to the limit in Concurrency, OOP, and the most advanced capabilities of C** <br>
    by Kamran Amini

15. **C++ Crash Course: A Fast-Paced Introduction** <br>
    by Josh Lospinoso


## Writing Compilers in Rust

1. **Crafting Interpreters** <br>
   by Robert Nystrom <br>
   The book license is Creative Commons. <br>
   [https://craftinginterpreters.com/](https://craftinginterpreters.com/) <br>
   **Lox Implementations** <br>
   [https://github.com/munificent/craftinginterpreters/wiki/Lox-implementations](https://github.com/munificent/craftinginterpreters/wiki/Lox-implementations) <br>
   **Crafting Interpreters in Rust - tdp2110** <br>
   [https://github.com/tdp2110/crafting-interpreters-rs](https://github.com/tdp2110/crafting-interpreters-rs) <br>
   **Crafting A Lox Interpreter In Rust, Part 1 - Diego Freijo** <br>
   [https://www.diegofreijo.com/blog/rlox-vm-a-lox-interpreter-in-rust-part-1/](https://www.diegofreijo.com/blog/rlox-vm-a-lox-interpreter-in-rust-part-1/)

2. **Video Play List - Crafting Interpreters - Uncle Scientist** <br>
   [https://www.youtube.com/playlist?list=PLib6-zlkjfXluRjBgK8grQH2IUSZjn-YN](https://www.youtube.com/playlist?list=PLib6-zlkjfXluRjBgK8grQH2IUSZjn-YN) 

3. **LISP interpreter in Rust** <br>
   [https://vishpat.github.io/lisp-rs/](https://vishpat.github.io/lisp-rs/)

4.  **Writing An Interpreter In Go** <br> 
    by Thorsten Ball

5.  **Writing A Compiler In Go** <br>
    by Thorsten Ball

6. **Compilers: Principles, Techniques, and Tools** <br>
   by Alfred Aho, Monica Lam, Ravi Sethi


## Contributing to the Rust Compiler rustc

1. **Video - RustConf 2021 - Hacking rustc: Contributing to the Compiler by Esteban Kuber** <br>
   [https://www.youtube.com/watch?v=9H9SO2u6Q20](https://www.youtube.com/watch?v=9H9SO2u6Q20)

2. **Video - rustc - A talk by Mark Mansi about the Rust programming language and compiler** <br>
   [https://www.youtube.com/watch?v=68U8ZZ1EnEQ](https://www.youtube.com/watch?v=68U8ZZ1EnEQ)

3. **Video - Hacking on rustc - Negative literals in indexing expressions** <br>
   [https://www.youtube.com/watch?v=OGihuce8rl8](https://www.youtube.com/watch?v=OGihuce8rl8) 

4. **Rust Lang - Compiler Team** <br>
   [https://rust-lang.github.io/compiler-team/](https://rust-lang.github.io/compiler-team/)

5. **The Rust Compiler - rustc** <br>
   [https://github.com/rust-lang/rust](https://github.com/rust-lang/rust)

6. **rustc API docs - rustdoc documentation for the compiler** <br>
   [https://doc.rust-lang.org/nightly/nightly-rustc/rustc_middle/](https://doc.rust-lang.org/nightly/nightly-rustc/rustc_middle/)

7. **Zulip Chat - rust-lang** <br>
   [https://rust-lang.zulipchat.com/](https://rust-lang.zulipchat.com/)

8. **Forum Rust Internals** <br> 
   [https://internals.rust-lang.org/](https://internals.rust-lang.org/)

9. **Guide to Rustc Development - Book** <br>
   [https://rustc-dev-guide.rust-lang.org/](https://rustc-dev-guide.rust-lang.org/)

10. **Video Play List - rustc lecture series** <br>
    [https://www.youtube.com/playlist?list=PL85XCvVPmGQhOL-J2Ng7qlPvDVOwYpGTN](https://www.youtube.com/playlist?list=PL85XCvVPmGQhOL-J2Ng7qlPvDVOwYpGTN)


## WebAssembly in Rust - WASM

1. **Rust and WebAssembly - Book** <br>
   [https://rustwasm.github.io/docs/book/](https://rustwasm.github.io/docs/book/)

2. **Write Your First WASM Module using Rust** <br>
   [https://www.youtube.com/watch?v=nW71Mlbmxt8](https://www.youtube.com/watch?v=nW71Mlbmxt8)

3. **Getting Started with WebAssembly and Rust: A First Look** <br>
   [https://www.youtube.com/watch?v=YHJjmsw_Sx0](https://www.youtube.com/watch?v=YHJjmsw_Sx0)

4. **Crate wasm-bindgen** <br>
   Facilitating high-level interactions between Wasm modules and JavaScript. <br>
   GitHub <br> 
   [https://github.com/rustwasm/wasm-bindgen](https://github.com/rustwasm/wasm-bindgen) <br>
   **The wasm-bindgen guide** - Book <br>
   [https://rustwasm.github.io/docs/wasm-bindgen/](https://rustwasm.github.io/docs/wasm-bindgen/)

5. **Project WASM Fourier** <br>
   Example of **browser audio microphone data** passed to Rust WASM module. <br>
   Note: **Really cool example** to study and for example do APP's with audio processing on Rust. <br>
   [https://github.com/linanova/wasm-fourier](https://github.com/linanova/wasm-fourier)

6. **Video - Rust + Yew + WASM + Canvas - Vers Binarii** <br>
   [https://www.youtube.com/watch?v=7Smco8araSo](https://www.youtube.com/watch?v=7Smco8araSo)


## Python extended with Rust and running a Python interpreter inside Rust  

1. **PyO3 - GitHub** <br>
   [https://github.com/PyO3/pyo3](https://github.com/PyO3/pyo3)

2. **The PyO3 user guide - Book** <br>
   [https://pyo3.rs/master/](https://pyo3.rs/master/)

3. **Python Extensions in Pure Rust with PyO3** <br>
   [https://depth-first.com/articles/2020/08/10/python-extensions-in-pure-rust-with-pyo3/](https://depth-first.com/articles/2020/08/10/python-extensions-in-pure-rust-with-pyo3/)   

4. **RustPython - A Python-3 interpreter written in Rust** <br>
   [https://github.com/RustPython/RustPython](https://github.com/RustPython/RustPython)


## Rust with inline Python

In a program made in Rust, ```use a macro to insert inline Python``` and move easily data (variables) between the two. <br>
<br>

``` Python
// Example_1 

use inline_python::python;

fn main() {
    let who = "world";
    let n = 5;
    python! {
        for i in range('n):
            print(i, "Hello", 'who)
        print("Goodbye")
    }
}
```

``` Python
// Example_2 
// Creates the data in Rust and plots the plot with inline Python with the lib matplotlib.

use inline_python::python;

fn main() {
    let data = vec![(4, 3), (2, 8), (3, 1), (4, 0)];
    python! {
        import matplotlib.pyplot as plt
        plt.plot('data)
        plt.show()
    }
}
```

1. Crate **inline-python** <br>
   Inline Python code directly in your Rust code <br>
   [https://crates.io/crates/inline-python](https://crates.io/crates/inline-python)

The inner workings and all the development steps of this project are beautifully explained, in detail, on this sequence of blog posts. <br>

2. **Writing Python inside your Rust code - Part 1** - Mara's Blog <br>
   [https://blog.m-ou.se/writing-python-inside-rust-1/](https://blog.m-ou.se/writing-python-inside-rust-1/)

3. **Writing Python inside your Rust code - Part 1A** - Mara's Blog <br>
   [https://blog.m-ou.se/writing-python-inside-rust-1a/](https://blog.m-ou.se/writing-python-inside-rust-1a/)

4. **Writing Python inside your Rust code - Part 2** - Mara's Blog <br>
   [https://blog.m-ou.se/writing-python-inside-rust-2/](https://blog.m-ou.se/writing-python-inside-rust-2/)

5. **Writing Python inside your Rust code - Part 3** - Mara's Blog <br>
   [https://blog.m-ou.se/writing-python-inside-rust-3/](https://blog.m-ou.se/writing-python-inside-rust-3/)

6. **Writing Python inside your Rust code - Part 4** - Mara's Blog <br>
   [https://blog.m-ou.se/writing-python-inside-rust-4/](https://blog.m-ou.se/writing-python-inside-rust-4/)


## Rust on or for the Raspberry Pi

* There are **two modes** of using Rust with the Raspberry Pi. <br>
  The first one is **installing Rust development tools on the Raspberry Pi** it self, and the second one is **installing on the PC and making cross-compilation** to generate a executable that runs on the Raspberry Pi.


### Developing on the Raspberry Pi and running Rust programs on the Raspberry Pi

1. **How to Get Started With Rust on Raspberry Pi** <br>
   [https://www.muo.com/tag/getting-started-rust-raspberry-pi/](https://www.muo.com/tag/getting-started-rust-raspberry-pi/)


### Developing on the PC and cross-compiling to run Rust programs on the Raspberry Pi

1. **Cross Compiling Rust for the Raspberry Pi** <br>
   It also explains a method to automatically coping the file to the Raspberry Pi after compilation. <br> 
   [https://chacin.dev/blog/cross-compiling-rust-for-the-raspberry-pi/](https://chacin.dev/blog/cross-compiling-rust-for-the-raspberry-pi/)

2. **Cross compiling Rust for Raspberry Pi** <br>
   [https://dev.to/h_ajsf/cross-compiling-rust-for-raspberry-pi-4iai](https://dev.to/h_ajsf/cross-compiling-rust-for-raspberry-pi-4iai)


## Embedded Rust

1. **An Overview of the Embedded Rust Ecosystem** - end 2020 <br>
   [https://www.youtube.com/watch?v=vLYit_HHPaY](https://www.youtube.com/watch?v=vLYit_HHPaY)

2. **Awesome embedded rust - Github** <br>
   Everything you need to know including drivers to connect external devices to the micro-controller. <br>
   [https://github.com/rust-embedded/awesome-embedded-rust](https://github.com/rust-embedded/awesome-embedded-rust)

3. **The Embedded Working Group Newsletter or Blog** <br>
   [https://rust-embedded.github.io/blog/](https://rust-embedded.github.io/blog/)

4. **Discovery Book** <br>
   Good starting point for **MicroBit** and **STM32** <br>
   [https://docs.rust-embedded.org/discovery/](https://docs.rust-embedded.org/discovery/)

5. **PlayList - Embedded Rust course - JaJakub** - 2022 <br>
   [https://www.youtube.com/playlist?list=PLL2SCPK5xSRWBPj-nKOVYIhxRw7C4kYeI](https://www.youtube.com/playlist?list=PLL2SCPK5xSRWBPj-nKOVYIhxRw7C4kYeI) 

6. Live streams with a **good example of developing with Embedded Rust in STM32 BluePill** <br>
   Embedded Rust - Vers Binarii <br>
   [https://www.youtube.com/playlist?list=PLP_X41VhYn5X6Wwjnm0bRwI3n2pdaszxU](https://www.youtube.com/playlist?list=PLP_X41VhYn5X6Wwjnm0bRwI3n2pdaszxU)

7. **Embedded Hardware Development with Rust** - 2018 <br>
   [https://www.youtube.com/watch?v=g25xsK3HKkE](https://www.youtube.com/watch?v=g25xsK3HKkE)

8. **Embedded Programming is Getting Rust-y** - end of 2021 <br>
   Embedded Computing Design <br>
   [https://www.youtube.com/watch?v=sOTx5324nKI](https://www.youtube.com/watch?v=sOTx5324nKI)

9. **The Embedded Rust Book** <br>
   **Second fantastic book to read** <br>
   Generic for any type of chip brand. <br>
   [https://docs.rust-embedded.org/book/](https://docs.rust-embedded.org/book/)

10. **Workbook for Embedded Workshops - Book** <br>
    Using the **Nordic nRF52840** Development Kit. <br>
    [https://embedded-trainings.ferrous-systems.com/](https://embedded-trainings.ferrous-systems.com/)

11. **The Embedonomicon Book** <br>
    Deep dive into the inner workings. <br>
    [https://docs.rust-embedded.org/embedonomicon/](https://docs.rust-embedded.org/embedonomicon/)

12. **Video - How can we write the best device driver?** <br>
    [https://www.youtube.com/watch?v=z9z74VpqO9A](https://www.youtube.com/watch?v=z9z74VpqO9A)

13. **Video - RTIC - Real Time Interrupt driven Concurrency** <br>
    RTIC is a RTOS - Real Time Operating System. <br>
    [https://www.youtube.com/watch?v=saNdh0m_qHc](https://www.youtube.com/watch?v=saNdh0m_qHc)

14. **RTIC Book** <br>
    Real-Time Interrupt-driven Concurrency. <br>
    **A very efficient preemptive multitasking framework** that supports **task prioritization** and **dead lock free execution**. <br>
    [https://rtic.rs/1.0/book/en/](https://rtic.rs/1.0/book/en/)

15. **Github - rtic-rs - cortex-m-rtic** <br>
    [https://github.com/rtic-rs/cortex-m-rtic](https://github.com/rtic-rs/cortex-m-rtic)

16. **Video - Grepit about the Rust RTIC framework** <br>
    [https://www.youtube.com/watch?v=sSJ-Md8nwIM](https://www.youtube.com/watch?v=sSJ-Md8nwIM)

17. Good **RTIC** project **example** <br>
    **Rust firmware for IR thermometer in STM32 with LCD** - geomatsi - rust-ir-thermo <br>
    [https://github.com/geomatsi/rust-ir-thermo](https://github.com/geomatsi/rust-ir-thermo)

18. **Video - Bare Metal Audio Programming With Rust - Antoine van Gelder - ADC20** <br>
    [https://www.youtube.com/watch?v=udlK1LQ3f3g](https://www.youtube.com/watch?v=udlK1LQ3f3g) <br>
    **Slides** <br>
    [https://flowdsp.io/talks/talk-adc20/#1](https://flowdsp.io/talks/talk-adc20/#1)

19. **Video - Building a simple logic analyser in Rust** <br>
    Rust Linz, September 2020 - Roland Ruckerbauer - Embedded Rust <br>
    Board used **stm32** compatible **bluepill**. <br>
    [https://www.youtube.com/watch?v=xY342ACNXFg](https://www.youtube.com/watch?v=xY342ACNXFg) <br>
    **Slides** <br>
    [https://github.com/ruabmbua/rlogic/blob/master/presentation.pdf](https://github.com/ruabmbua/rlogic/blob/master/presentation.pdf) <br>
    **Github - ruabmbua - rlogic** <br>
    [https://github.com/ruabmbua/rlogic](https://github.com/ruabmbua/rlogic)


## Embedded Rust crates and code size optimization

1. **Crate heapless** <br>
   [https://github.com/japaric/heapless](https://github.com/japaric/heapless)

```
   Arc         - Thread-safe reference-counting pointer backed by a memory pool
   BinaryHeap  - Priority queue
   IndexMap    - Hash table
   IndexSet    - Hash set
   LinearMap
   Pool        - Lock-free memory pool
   String
   Vec
   mpmc::Q*    - Multiple producer multiple consumer lock-free queue
   spsc::Queue - Single producer single consumer lock-free queue
```

2. **Crate ufmt** <br>
   A (6-40x) smaller, (2-9x) faster and panic-free alternative to core::fmt <br>
   [https://github.com/japaric/ufmt](https://github.com/japaric/ufmt)

3. **LCD 16x2 - Crate hd44780-driver** <br>
   Implementation of the **embedded-hal traits for the HD44780**, 16x1, **16x2** and 16x4. <br>
   [https://github.com/JohnDoneth/hd44780-driver](https://github.com/JohnDoneth/hd44780-driver)

4. **Crate Embedded graphics** <br>
   It's a 2D graphics library that is focused on memory constrained embedded devices. <br>
   [https://github.com/embedded-graphics/embedded-graphics](https://github.com/embedded-graphics/embedded-graphics)

5. **Crate flip-link** <br>
   Adds zero-cost stack overflow protection to your embedded programs. <br>
   [https://github.com/knurling-rs/flip-link/](https://github.com/knurling-rs/flip-link/)

6. **Crate defmt** <br>
   defmt ("de format", short for "deferred formatting") is a highly efficient logging framework that targets resource-constrained devices, like micro-controllers. <br>
   [https://github.com/knurling-rs/defmt/](https://github.com/knurling-rs/defmt/)

7. **TOML compilation flag options to generate smaller code size**

```
....

[profile.release.package."*"]
opt-level = "z"

[profile.release]
codegen-units = 1
debug = true
opt-level = "z"
```


## Embedded Rust with STM32 BluePill - STM32F103

1. STM32 BluePill in Rust - **Project template and lot's of info** <br>
   This is the project template I use in my BluePill projects. <br>
   [https://github.com/joaocarvalhoopen/stm32_bluepill_in_rust__Template](https://github.com/joaocarvalhoopen/stm32_bluepill_in_rust__Template)


## Embedded Rust with Raspberry Pi Pico - 4 dollars board

1. **All relevant Info and a starting project Template.** <br> 
   Where I have put all the info that I consider to be relevant for Pico development in Rust. <br>
   **Raspberry Pi Pico in Rust Proj Template with RTIC USB-Serial and UF2** <br>
   [https://github.com/joaocarvalhoopen/Raspberry_Pi_Pico_in_Rust__Proj_Template_with_RTIC_USB-Serial_UF2](https://github.com/joaocarvalhoopen/Raspberry_Pi_Pico_in_Rust__Proj_Template_with_RTIC_USB-Serial_UF2)

2. Raspberry Pi **Pico** - **rp-HAL** <br>
   [https://github.com/rp-rs/rp-hal](https://github.com/rp-rs/rp-hal) <br>
   **rp2040-hal** - **Examples** <br>
   [https://github.com/rp-rs/rp-hal/tree/main/rp2040-hal/examples](https://github.com/rp-rs/rp-hal/tree/main/rp2040-hal/examples) <br>
   **Examples** for the **board rp-pico**. <br>
   [https://github.com/rp-rs/rp-hal/tree/main/boards/rp-pico](https://github.com/rp-rs/rp-hal/tree/main/boards/rp-pico) <br>
   **Documentation** <br>
   [https://docs.rs/rp2040-hal/latest/rp2040_hal/](https://docs.rs/rp2040-hal/latest/rp2040_hal/)

3. **Site - rp2040 - Chip documentation** <br>
   [https://www.raspberrypi.com/documentation/microcontrollers/](https://www.raspberrypi.com/documentation/microcontrollers/)

4. Getting Started with **Rust on a Raspberry Pi Pico - Part 1** <br>
   [https://reltech.substack.com/p/getting-started-with-rust-on-a-raspberry](https://reltech.substack.com/p/getting-started-with-rust-on-a-raspberry)

5. Getting Started with **Rust on a Raspberry Pi Pico - Part 2** <br>
   [https://reltech.substack.com/p/getting-started-with-raspberry-pi](https://reltech.substack.com/p/getting-started-with-raspberry-pi)

6. Getting Started with **Rust on a Raspberry Pi Pico - Part 3** <br>
   [https://reltech.substack.com/p/getting-started-with-rust-on-a-raspberry-a88](https://reltech.substack.com/p/getting-started-with-rust-on-a-raspberry-a88)

7. **Oleg Eterevsky comment on the previous page** - Slightly simpler setup. Instead of using a separate controller for handling the debug, he have just set up **debug logging via USB serial port**. This requires a bit more boilerplate (handling the USB interrupt and such), but is much simpler from the hardware perspective: you need to just plug in a single Pico board in your USB, flash it and you can immediately see the debug output. <br>
   **USB_Serial - repo** <br>
   [https://github.com/eterevsky/rp2040-blink](https://github.com/eterevsky/rp2040-blink)

8. **Crate usb-device** - Experimental device-side USB stack for embedded devices. <br>
   [https://crates.io/crates/usb-device](https://crates.io/crates/usb-device)

9. **Way to easily Reboot the Pico to USB-PEN mode to program it** <br>
   You can have a easy reboot without needing to disconnecting and while pressing the boot button reconnecting the cable. <br> 
   Just add a switch from pin RUN to GND and while pressing the Boot Button press the Run Button and release the Run switch and them the Boot Button. It will enter the USB-PEN mode, that allows you to program by just coping the Rust or C binary from the PC to the Raspberry Pico micro-controller. <br>
   See official documentation for details.

10. PlayList - **Rust Pico - Low Level Learning** <br>
    [https://www.youtube.com/playlist?list=PLc7W4b0WHTAUAEAguiqpNa5H0QqXJIJI6](https://www.youtube.com/playlist?list=PLc7W4b0WHTAUAEAguiqpNa5H0QqXJIJI6)

11. Play List - **Raspberry Pi Pico in C - Low Level Learning** <br>
    [https://www.youtube.com/playlist?list=PLc7W4b0WHTAV6EYRVayb9c9dEsq-NeXAt](https://www.youtube.com/playlist?list=PLc7W4b0WHTAV6EYRVayb9c9dEsq-NeXAt)

12. **PlayList - Intro to Raspberry Pi Pico and RP2040** - Digi-Key <br>
    **C/C++** and **MicroPython** <br>
    [https://www.youtube.com/playlist?list=PLEBQazB0HUyQO6rJxKr2umPCgmfAU-cqR](https://www.youtube.com/playlist?list=PLEBQazB0HUyQO6rJxKr2umPCgmfAU-cqR)

13. **In-depth: Raspberry Pi Pico's PIO - programmable IO** - stacksmashing <br>
    [https://www.youtube.com/watch?v=yYnQYF_Xa8g](https://www.youtube.com/watch?v=yYnQYF_Xa8g) 

14. **Site - Raspberry Pi Pico** <br>
    [https://www.raspberrypi.com/products/raspberry-pi-pico/](https://www.raspberrypi.com/products/raspberry-pi-pico/)

15. **Site - Getting started with Raspberry Pi Pico** <br>
    [https://projects.raspberrypi.org/en/projects/getting-started-with-the-pico/0](https://projects.raspberrypi.org/en/projects/getting-started-with-the-pico/0)

16. **Book - Get Started with MicroPython on Raspberry Pi Pico** <br>
    [https://hackspace.raspberrypi.com/books/micropython-pico](https://hackspace.raspberrypi.com/books/micropython-pico)

17. **Book - Adafruit - Getting Started with Raspberry Pi Pico and CircuitPython** <br>
    [https://cdn-learn.adafruit.com/downloads/pdf/getting-started-with-raspberry-pi-pico-circuitpython.pdf](https://cdn-learn.adafruit.com/downloads/pdf/getting-started-with-raspberry-pi-pico-circuitpython.pdf)

18. **Video - The Raspberry Pi Pico Review - $4 ARM Microcontroller** <br>
    [https://www.youtube.com/watch?v=dUCgYXF01Do](https://www.youtube.com/watch?v=dUCgYXF01Do)

19. **Video - Raspberry Pi Pico VGA video output using only resistors** <br>
    [https://www.youtube.com/watch?v=RmPWcsvGSyk](https://www.youtube.com/watch?v=RmPWcsvGSyk)


## Embedded Rust with ESP32

1. **esp-rs - Rust on ESP-IDF "Hello, World" template** <br>
   [https://github.com/esp-rs/esp-idf-template](https://github.com/esp-rs/esp-idf-template)

2. **Video - Embedded Rust: Wifi and I2C on a ESP32-C3 - Andrei Litvin** <br>
   [https://www.youtube.com/watch?v=CXm7NdBBegk](https://www.youtube.com/watch?v=CXm7NdBBegk) <br>
   **GitHub andy31415 - rust-esp32-c3-demos** <br>
   [https://github.com/andy31415/rust-esp32-c3-demos/tree/oled_wifi](https://github.com/andy31415/rust-esp32-c3-demos/tree/oled_wifi)

3. **ivmarkov - rust-esp32-std-demo** <br>
   A complex demo of ESP32 in Rust <br>
   [https://github.com/ivmarkov/rust-esp32-std-demo](https://github.com/ivmarkov/rust-esp32-std-demo)


## Links

1. **Rust site** <br>
   A language empowering everyone to build reliable and efficient software. <br>
   [https://www.rust-lang.org/](https://www.rust-lang.org/)

2. **Song - Rust 2021 Edition** <br>
   [https://www.youtube.com/watch?v=q0aNduqb2Ro](https://www.youtube.com/watch?v=q0aNduqb2Ro)

3. **Crate.io - The Rust community’s crate registry** <br>
  [https://crates.io/](https://crates.io/)

4. **Rust weekly news letter** <br>
   [https://this-week-in-rust.org/](https://this-week-in-rust.org/)

5. **The Little Book of Rust Books** <br>
   [https://lborb.github.io/book/title-page.html](https://lborb.github.io/book/title-page.html)

6. **Awesome-rust** <br>
   [https://github.com/rust-unofficial/awesome-rust](https://github.com/rust-unofficial/awesome-rust)

7. **Awesome-embedded-rust** <br>
   [https://github.com/rust-embedded/awesome-embedded-rust](https://github.com/rust-embedded/awesome-embedded-rust)

8. **Rust Analyzer - User manual and short cut keys** <br>
   [https://rust-analyzer.github.io/manual.html](https://rust-analyzer.github.io/manual.html)

9. **Jon Gjengset - Rust in depth Youtube channel.** <br> 
   [https://www.youtube.com/c/JonGjengset](https://www.youtube.com/c/JonGjengset)

10. **Tokio** <br>
    Tokio is an asynchronous runtime (**async** and **await**) for the Rust programming language. It provides the building blocks needed for writing network applications. It gives the flexibility to target a wide range of systems, from large servers with dozens of cores to small embedded devices. <br>
    See the tutorials. <br>
    [https://tokio.rs/](https://tokio.rs/)

11. Best **async** and **await** introduction video. <br>
   **Video - Crust of Rust: async e await - Jon Gjengset** <br>
   [https://www.youtube.com/watch?v=ThjvMReOXYM](https://www.youtube.com/watch?v=ThjvMReOXYM)

12. **Video - Creating a Chat Server with async Rust and Tokio – Lily Mara** <br>
    [https://www.youtube.com/watch?v=Iapc-qGTEBQ](https://www.youtube.com/watch?v=Iapc-qGTEBQ)

13. **Tracing - Log tracing platform** <br>
    [https://github.com/tokio-rs/tracing](https://github.com/tokio-rs/tracing)

14. **Actix Web** <br>
    Web Framework that's blazing fast, secure, asynchronous runs over Tokio and is "similar" to **Flask** of Python. <br>
    Can process **650.000 request per second**. <br>
    [https://actix.rs/](https://actix.rs/)

15. **Rocket** <br>
    Web Framework that's fast, secure and more "similar" to **Django** of Python. <br>
    [https://rocket.rs/](https://rocket.rs/)

16. **Serde** <br>
    Serde is a framework for **serializing** and **deserializing** Rust data structures efficiently and generically. <br>
    [https://serde.rs/](https://serde.rs/) <br>
    [https://crates.io/crates/serde](https://crates.io/crates/serde)

17. **BindGen** <br>
    Automatically generates Rust FFI bindings to C and C++ libraries. <br>
    [https://crates.io/crates/bindgen](https://crates.io/crates/bindgen) <br>
    Tutorial guide. <br>
    [https://rust-lang.github.io/rust-bindgen/](https://rust-lang.github.io/rust-bindgen/)

18. **Hacking rustc: Contributing to the Compiler by Esteban Kuber** - RustConf 2021 <br>
    [https://www.youtube.com/watch?v=9H9SO2u6Q20](https://www.youtube.com/watch?v=9H9SO2u6Q20)


## Rust Foundation

1. Video - **What Is Rust Foundation?** <br>
   [https://www.youtube.com/watch?v=AI4lPN0BqGc](https://www.youtube.com/watch?v=AI4lPN0BqGc)

2. **Site - Rust Foundation** <br>
   [https://foundation.rust-lang.org/](https://foundation.rust-lang.org/)


## Rust Blogs

1. **pretzelhammer's Rust blog** <br>
   [https://github.com/pretzelhammer/rust-blog](https://github.com/pretzelhammer/rust-blog)

   1. **RESTful API in Sync & Async Rust - pretzelhammer** <br> 
      [https://github.com/pretzelhammer/rust-blog/blob/master/posts/restful-api-in-sync-and-async-rust.md](https://github.com/pretzelhammer/rust-blog/blob/master/posts/restful-api-in-sync-and-async-rust.md)

   2. **Common Rust Lifetime Misconceptions - pretzelhammer** <br>
      [https://github.com/pretzelhammer/rust-blog/blob/master/posts/common-rust-lifetime-misconceptions.md](https://github.com/pretzelhammer/rust-blog/blob/master/posts/common-rust-lifetime-misconceptions.md)

   3. **Tour of Rust's Standard Library Traits - pretzelhammer** <br>
      [https://github.com/pretzelhammer/rust-blog/blob/master/posts/tour-of-rusts-standard-library-traits.md](https://github.com/pretzelhammer/rust-blog/blob/master/posts/tour-of-rusts-standard-library-traits.md)

   4. **Sizedness in Rust – pretzelhammer** <br>
      [https://github.com/pretzelhammer/rust-blog/blob/master/posts/sizedness-in-rust.md](https://github.com/pretzelhammer/rust-blog/blob/master/posts/sizedness-in-rust.md)

2. **fasterThanLime Blog** - Amos Wenger <br>
   [https://fasterthanli.me](https://fasterthanli.me)


## Rust Youtube Channels

1. **Channel Rust** <br>
   [https://www.youtube.com/c/RustVideos/videos](https://www.youtube.com/c/RustVideos/videos)

2. **Channel Rust Foundation** <br>
   [https://www.youtube.com/channel/UC0jzvznwtnsdXYIp415oC9g/videos](https://www.youtube.com/channel/UC0jzvznwtnsdXYIp415oC9g/videos)

3. **Channel fasterthanlime - Amos Wegner** <br>
   [https://www.youtube.com/c/fasterthanlime/videos](https://www.youtube.com/c/fasterthanlime/videos)

4. **Channel Jon Gjengset - Rust in depth Youtube channel.** <br> 
   [https://www.youtube.com/c/JonGjengset/videos](https://www.youtube.com/c/JonGjengset/videos)

5. **Channel Tensor Programming - Intro to Rust** <br>
   [https://www.youtube.com/playlist?list=PLJbE2Yu2zumDF6BX6_RdPisRVHgzV02NW](https://www.youtube.com/playlist?list=PLJbE2Yu2zumDF6BX6_RdPisRVHgzV02NW)

6. **Channel Tensor Programming - Rust Projects** <br>
   [https://www.youtube.com/playlist?list=PLJbE2Yu2zumDD5vy2BuSHvFZU0a6RDmgb](https://www.youtube.com/playlist?list=PLJbE2Yu2zumDD5vy2BuSHvFZU0a6RDmgb)

7. **Channel Let's Get Rusty** <br>
   [https://www.youtube.com/c/LetsGetRusty/videos](https://www.youtube.com/c/LetsGetRusty/videos)

8. **Channel Uncle Scientist** <br>
   [https://www.youtube.com/channel/UClnm0enwPt9iPWGZ5uh3Bfw/videos](https://www.youtube.com/channel/UClnm0enwPt9iPWGZ5uh3Bfw/videos)

9. **Channel Ryan Levick** <br>
   [https://www.youtube.com/c/RyanLevicksVideos/videos](https://www.youtube.com/c/RyanLevicksVideos/videos)

10. **Channel Tantan** <br>
    [https://www.youtube.com/c/Tantandev/videos](https://www.youtube.com/c/Tantandev/videos)

11. **Channel Crazcalm's Tech Stack** <br>
    [https://www.youtube.com/c/CrazcalmsTechStack/videos](https://www.youtube.com/c/CrazcalmsTechStack/videos)

12. **Channel Ferrous Systems GmbH** <br>
    Embedded Rust <br>
    [https://www.youtube.com/c/FerrousSystemsGmbH/videos](https://www.youtube.com/c/FerrousSystemsGmbH/videos)

13. **Channel JaJakub** <br>
    Embedded Rust <br>
    [https://www.youtube.com/c/JaJakubYT/videos](https://www.youtube.com/c/JaJakubYT/videos)

14. **Channel Vers Binarii** <br>
    Embedded Rust <br>
    [https://www.youtube.com/channel/UCgLxnJi8BU476a3uZO29H4w/videos](https://www.youtube.com/channel/UCgLxnJi8BU476a3uZO29H4w/videos)


## GUI programming in Rust

1. **GTK4 - Unlocking the GNOME stack for Rust** <br>
   [https://gtk-rs.org/](https://gtk-rs.org/)

2. **Book - GUI development with Rust and GTK 4** <br>
   [https://gtk-rs.org/gtk4-rs/stable/latest/book/](https://gtk-rs.org/gtk4-rs/stable/latest/book/)

3. **Relm4 for GTK4** <br>
   [https://github.com/AaronErhardt/relm4](https://github.com/AaronErhardt/relm4)

4. **Speedrunning GUI development in Rust** <br>
   **Hint:** 1.2 seconds compilation technic. <br>
   [https://aaronerhardt.github.io/blog/posts/gui_speedrun/](https://aaronerhardt.github.io/blog/posts/gui_speedrun/)

5. **egui: an easy-to-use GUI in pure Rust** <br>
   Normal **desktop** GUI and **WebAssembly** written entirely in Rust, **immediate mode**. <br> 
   [https://github.com/emilk/egui](https://github.com/emilk/egui)

6. **eGUI - Web Demo** <br>
   [https://emilk.github.io/egui/index.html](https://emilk.github.io/egui/index.html)

7. **eframe - It's the official framework library for writing apps using egui** <br>
   [https://github.com/emilk/egui/tree/master/eframe](https://github.com/emilk/egui/tree/master/eframe)

8. **egui - 7a. Building a GUI app in Rust - Part A - creativcoder** <br>
   [https://www.youtube.com/watch?v=NtUkr_z7l84](https://www.youtube.com/watch?v=NtUkr_z7l84)

9. **egui - 7b. Building a GUI app in Rust - Part B - creativcoder** <br>
   [https://www.youtube.com/watch?v=SvFPdgGwzTQ](https://www.youtube.com/watch?v=SvFPdgGwzTQ)

10. **egui - 8. Building a web app in Rust - WASM - creativcoder** <br>
    [https://www.youtube.com/watch?v=4MKcqR9z8AU](https://www.youtube.com/watch?v=4MKcqR9z8AU)

11. **Crate confy** <br>
    To maintain the state fo the APP in a config file. Serializes and deserializes automatically with Serde. <br> 
    [https://github.com/rust-cli/confy](https://github.com/rust-cli/confy)

12. **Crate tracing** <br>
    [https://github.com/tokio-rs/tracing](https://github.com/tokio-rs/tracing)

13. **pix_engine** <br>
    It's a cross-platform graphics & UI library for simple games, visualizations, digital art, and graphics applications. A kind of more simple **Processing** or **p5.js** but for Rust. Has a good collection of examples. <br>
    [https://github.com/lukexor/pix-engine](https://github.com/lukexor/pix-engine) 
   

## Audio in Rust

1. **RustAudio** <br>
   Free and useful Audio, DSP and music libraries written in Rust. <br>
   [https://github.com/RustAudio](https://github.com/RustAudio)

2. **CPAL - Cross-Platform Audio Library** <br>
   Low-level library for audio input and output in pure Rust. <br>
   Works aldo in WASM. <br>
   [https://github.com/RustAudio/cpal](https://github.com/RustAudio/cpal)

3. **Rodio - Audio playback library** <br>
   MP3, WAV, Vorbis, Flac, MP4 and AAC. <br>
   [https://github.com/RustAudio/rodio](https://github.com/RustAudio/rodio)

4. **dasp - Digital Audio Signal Processing in Rust** <br>
   [https://github.com/RustAudio/dasp](https://github.com/RustAudio/dasp)

5. **rust-portaudio - PortAudio bindings and wrappers for Rust.** <br>
   [https://github.com/RustAudio/rust-portaudio](https://github.com/RustAudio/rust-portaudio)   


## Faster Compilation - Linker times in Linux and Unix ELF

**mold** is optimized for **Linux**, **zld** only works on **macOS**. For **production** use, **lld** might be the most mature option. <br>
<br>
**mold** is a high-performance drop-in replacement for existing Unix linkers. It is **several times faster than LLVM lld linker** <br>
In the context of building a Relm4 for GTK-4 GUI application: <br>
"With mold I was able to **reduce my incremental compile times by factor 7 to only about 1.2 second**. With this, it’s really fun to play with the code of the UI as you can see the result of your changes almost immediately." by the author of Relm4 <br> 

1. **Mold** <br>
   https://github.com/rui314/mold

```
// After installing mold, all you need to do is add the
// prefix mold -run to the command you want to run.
// Most likely this will be:

mold -run cargo run
```

2. **Tips for Faster Rust Compile Times** <br>
   [https://endler.dev/2020/rust-compile-times/](https://endler.dev/2020/rust-compile-times/)


## Machine Learning for Rust

1. **Taking ML to production with Rust: a 25x speedup** <br>
   [https://www.lpalmieri.com/posts/2019-12-01-taking-ml-to-production-with-rust-a-25x-speedup/](https://www.lpalmieri.com/posts/2019-12-01-taking-ml-to-production-with-rust-a-25x-speedup/)

2. **Machine learning in Rust using Linfa** <br>
   [https://blog.logrocket.com/machine-learning-in-rust-using-linfa/](https://blog.logrocket.com/machine-learning-in-rust-using-linfa/)

3. **Crate Linfa** <br>
   linfa aims to provide a comprehensive toolkit to build Machine Learning applications with Rust. <br>
   Kin **in spirit to Python's scikit-learn**, it focuses on common preprocessing tasks and classical ML algorithms for your everyday ML tasks. <br>
   [https://crates.io/crates/linfa](https://crates.io/crates/linfa) <br>
   [https://github.com/rust-ml/linfa](https://github.com/rust-ml/linfa)

4. **Crate tch-rs** <br>
   Rust wrappers for the **PyTorch C++ api** (libtorch). <br>
   [https://crates.io/crates/tch](https://crates.io/crates/tch) <br>
   [https://docs.rs/tch](https://docs.rs/tch)

5. **Crate Rust TensorFlow** <br>
   TensorFlow Rust provides idiomatic Rust language **bindings for TensorFlow**. <br>
   [https://crates.io/crates/tensorflow](https://crates.io/crates/tensorflow) <br>
   [https://github.com/tensorflow/rust](https://github.com/tensorflow/rust)

6. **Crate rust-xgboost** <br>
   Rust bindings for the **XGBoost gradient boosting library**. <br>
   [https://crates.io/crates/xgboost](https://crates.io/crates/xgboost)


## Rust VSCode plugins

1. **rust-analyzer** <br>
   Code analyzer while editing <br>
   [https://marketplace.visualstudio.com/items?itemName=matklad.rust-analyzer](https://marketplace.visualstudio.com/items?itemName=matklad.rust-analyzer) <br>
   For **better warnings** in the same user interface, go into the VSCode **settings** > **Rust Analyzer** > **Check On Save**: Command and setting “**clippy**” instead of “check”.

2. **Better TOML** <br>
   .toml syntax hilight. <br>
   [https://marketplace.visualstudio.com/items?itemName=bungcip.better-toml](https://marketplace.visualstudio.com/items?itemName=bungcip.better-toml)

3. **Error Lens** <br>
   Better positioning of error messages in editor. <br>
   [https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)

4. **CodeLLDB** - Vadim Chugunov <br>
   Debugger plugin for Rust. <br>
   [https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb](https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb)

5. **Code Spell Checker** <br>
   [https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)

6. **Markdown All in One** <br>
   [https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)


## Rust Debugger

1. **How to Debug Rust with Visual Studio Code** <br>
   [https://www.forrestthewoods.com/blog/how-to-debug-rust-with-visual-studio-code/](https://www.forrestthewoods.com/blog/how-to-debug-rust-with-visual-studio-code/) 

2. **Debugging Rust with VS Code** <br>
   [https://dev.to/rogertorres/debugging-rust-with-vs-code-11dj](https://dev.to/rogertorres/debugging-rust-with-vs-code-11dj)

3. **CodeLLDB - Vadim Chugunov** <br>
   Plugin for VS Code <br>
   [https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb](https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb)


## Rust Error Handling

To define good error types that encapsulate other errors. In the case where you need to return from a function, multiple incompatible types, and you don't want to manually write conversion functions that implement the trait std::convert::From< > . <br>

1. Crate **Anyhow** <br>
   Use **Anyhow** if you don't care what error type your functions return, you just want it to be easy. This is common in application code. <br>
   [https://crates.io/crates/anyhow](https://crates.io/crates/anyhow)

2. Crate **thiserror** <br>
   Use **thiserror** if you are a library that wants to design your own dedicated error type(s) so that on failures the caller gets exactly the information that you choose. <br>
   [https://crates.io/crates/thiserror](https://crates.io/crates/thiserror)


## Tips and Tricks

* **12 Rust Tips and Tricks you might not know yet** - Federico Terzi <br>
  [https://federicoterzi.com/blog/12-rust-tips-and-tricks-you-might-not-know-yet/](https://federicoterzi.com/blog/12-rust-tips-and-tricks-you-might-not-know-yet/)

* **sccache - Shared Compilation Cache** <br>
  sccache includes support for caching the compilation of **C/C++** code, **Rust**, as well as NVIDIA's **CUDA** using nvcc. Avoiding compilation when possible. <br>
  [https://github.com/mozilla/sccache](https://github.com/mozilla/sccache)


## GC for Rust - Garbage Collector

“Cases where one needs to maintain a complicated, dynamic graph “(with cycles)” are where a GC becomes useful. Similarly, if one is writing an interpreter for a GCd language, having a GC in Rust would simplify things a lot.”

* **Designing a GC in Rust** <br>
  [https://manishearth.github.io/blog/2015/09/01/designing-a-gc-in-rust/](https://manishearth.github.io/blog/2015/09/01/designing-a-gc-in-rust/)

* **Crate rust-gc** <br>
  [https://crates.io/crates/gc](https://crates.io/crates/gc) <br>
  **Examples** <br>
  [https://github.com/Manishearth/rust-gc/tree/master/gc/tests](https://github.com/Manishearth/rust-gc/tree/master/gc/tests)


## Programming Parallel computers - Optimization guide C Plus Plus and Rust

1. **Programming Parallel Computers - In depth lectures notes** <br>
   [https://ppc.cs.aalto.fi/](https://ppc.cs.aalto.fi/)

2. **Comparing Parallel Rust and C++** <br>
   [https://parallel-rust-cpp.github.io/](https://parallel-rust-cpp.github.io/)

3. **Crossbeam - Tools for concurrent programming** <br>
   [https://crates.io/crates/crossbeam](https://crates.io/crates/crossbeam) <br>
   **Crossbeam - Learning Resources** <br>
   [https://github.com/crossbeam-rs/rfcs/wiki](https://github.com/crossbeam-rs/rfcs/wiki)

4. **Rayon - It is a data-parallelism library for Rust** <br>
   [https://crates.io/crates/rayon](https://crates.io/crates/rayon) <br>
   **Video** - Rayon: Data Parallelism for Fun and Profit — Nicholas Matsakis <br>
   [https://www.youtube.com/watch?v=gof_OEv71Aw](https://www.youtube.com/watch?v=gof_OEv71Aw) <br>
   Rayon: data parallelism in Rust <br>
   [https://smallcultfollowing.com/babysteps/blog/2015/12/18/rayon-data-parallelism-in-rust/](https://smallcultfollowing.com/babysteps/blog/2015/12/18/rayon-data-parallelism-in-rust/) <br>
   **Rayon docs** <br>
   [https://docs.rs/rayon/latest/rayon/](https://docs.rs/rayon/latest/rayon/)

5. **dpc-pariter - Parallel iterator processing** <br>
   [https://crates.io/crates/dpc-pariter](https://crates.io/crates/dpc-pariter) <br>
   **Adding parallelism to your Rust iterators** with dpc-pariter <br>
   [https://dpc.pw/adding-parallelism-to-your-rust-iterators](https://dpc.pw/adding-parallelism-to-your-rust-iterators)

6. **perf Examples** <br>
   See also the lecture. <br>
   [https://www.brendangregg.com/perf.html](https://www.brendangregg.com/perf.html)

7. **perf: Linux profiling with performance counters** <br>
   [https://perf.wiki.kernel.org/index.php/Main_Page](https://perf.wiki.kernel.org/index.php/Main_Page) 

8. **Systems Performance Enterprise and the Cloud 2nd Ed** <br>
	by Brendan Gregg

To **install Perf** on your Linux system you can do a simple package installation like apt-get if you are on a debian, then execute perf and it will tell you the package that you will have to install that is specific for your Linux kernel version. If your distribution automatically updates your kernel, you will need to download a new and correct version for your new kernel, and install it with your system package manager, ex: apt-get. <br> 
<br>
In the Rust .toml file add the 2 following lines, to add the debug symbols table to the Rust executable program file, compiled with ```--release``` flag: <br> 

```
[profile.release]
debug = true
```

To run **Perf profiling** on your Rust executable program. After that you can also use **flamegraph**. <br>

```
# Temporarily activate this flag perf_event_paranoid.

> echo -1 | sudo tee /proc/sys/kernel/perf_event_paranoid


# Record the executable program profiling data in a .data file.

> perf record -F99 --call-graph dwarf <path to the executable>


# To see the report use with Up/Down arrow keys, with "+"
# and with "a" to see the annotated assembly code with the Rust
# code correspondent code. The report will include the % of time in
# inside the function and in each group of assembly instructions.
# Press "tab" key in annotation mode to jump between hot spots.

> perf report
```

The **Perf profiler** has many command use the **stat** command to get the **IPC – Instruction Per Clock Cycle**, it's an average. <br>
<br>
To know **how much peak memory** your executable program uses do: <br>

```
> /usr/bin/time -v <path to the executable>
```

Note: There are 2 "time" executables and this is not the bash default time program. That's why you have to write the full path ```/usr/bin/time``` to execute it. <br>


9. **The Rust Performance Book** <br>
   [https://nnethercote.github.io/perf-book/title-page.html](https://nnethercote.github.io/perf-book/title-page.html)

10. **Guide to Optimization** <br>
    Achieving warp speed with Rust <br>
    [https://gist.github.com/jFransham/369a86eff00e5f280ed25121454acec1](https://gist.github.com/jFransham/369a86eff00e5f280ed25121454acec1) <br>
    Cheap tricks for high-performance Rust <br>
    [https://deterministic.space/high-performance-rust.html](https://deterministic.space/high-performance-rust.html)<br>
    Video - Optimizing Rust - Rust Oslo 2021-11-11 - Lily Mara <br>
    [https://www.youtube.com/watch?v=LQ2nIhj45vE](https://www.youtube.com/watch?v=LQ2nIhj45vE) <br>
    Optimization - Making Rust Code Go Brrrr <br>
    [https://aspenuwu.me/posts/rust-optimization.html](https://aspenuwu.me/posts/rust-optimization.html) <br>
    Profile Guided Optimization <br>
    [https://doc.rust-lang.org/rustc/profile-guided-optimization.html](https://doc.rust-lang.org/rustc/profile-guided-optimization.html) <br>
    Optimizations: the speed size tradeoff <br>
    [https://rust-embedded.github.io/book/unsorted/speed-vs-size.html](https://rust-embedded.github.io/book/unsorted/speed-vs-size.html)


## Rust Optimization - Compilation modes and flags

The best way to optimize your code is to choose the right algorithm and the right data structures. <br>

* **How to become dangerous in Algorithms** <br>
  [https://github.com/joaocarvalhoopen/How_to_become_dangerous_in_algorithms](https://github.com/joaocarvalhoopen/How_to_become_dangerous_in_algorithms)

* **The Algorithms - Rust** <br>
  [https://github.com/TheAlgorithms/Rust](https://github.com/TheAlgorithms/Rust)

* **The Algorithms - Python** <br>
  For a more complete list of implementations of algorithms <br>
  [https://github.com/TheAlgorithms/Python/blob/master/DIRECTORY.md](https://github.com/TheAlgorithms/Python/blob/master/DIRECTORY.md)


You can also apply several coding techniques that come from the underling knowledge of how the rust transforms your code structures in memory (stack and heap) and how they are executed, for example avoiding allocation, avoiding cloning large things that aren’t basic types and that are by nature cloned. (More info bellow.)
You can do profiling to guide you through optimization, identifying the hot-spots to pin point you to the exact code your program spends that 90% of his time. And to allow you to see where you can shave it in the number of instructions that are executed at the same time and to increase your IPC – Instructions Per Clock cycle of your superscaller CPU. And then you can also mess around with compilation flags like the following, see [https://nnethercote.github.io/perf-book/build-configuration.html](https://nnethercote.github.io/perf-book/build-configuration.html) :

* **rustc book - rustc is the Rust compiler** <br>
  [https://doc.rust-lang.org/rustc/](https://doc.rust-lang.org/rustc/)

* **Add debug symbols table to the release build for profiling.** In ```Cargo.toml```.

```
[profile.release]
debug = true
```

* **LTO - Link-Time Optimization** <br>
  Link-time optimization (LTO) is a whole-program optimization technique that can improve runtime performance by 10-20% or more, at the cost of increased build times. In ```Cargo.toml```. <br>

```
[profile.release]
lto = true
```

* **Codegen Units** <br>
  The Rust compiler splits your crate into multiple codegen units to parallelize (and thus speed up) compilation. However, this might cause it to miss some potential optimizations. This will optimize it as a all, not dividing into more than one units. You have to benchmark it, because it can run faster or in some cases slower. In ```Cargo.toml```. <br>

```
[profile.release]
codegen-units = 1
```

* Using CPU Specific Instructions - **Compiling to native CPU features**. <br>
  It identifies and optimizes for the features of your CPU used in the compilation machine. <br> 

```    
$ RUSTFLAGS="-C target-cpu=native" cargo build --release
```

* **PGO - Profile-Guided Optimization**
  Profile-guided optimization (PGO) is a compilation model where you compile your program, run it on sample data while collecting profiling data, and then use that profiling data to guide a second compilation of the program. <br>
  **Exploring PGO for the Rust compiler** <br>
  [https://blog.rust-lang.org/inside-rust/2020/11/11/exploring-pgo-for-the-rust-compiler.html](https://blog.rust-lang.org/inside-rust/2020/11/11/exploring-pgo-for-the-rust-compiler.html) <br>
  **Profile Guided Optimization** <br>
  [https://doc.rust-lang.org/rustc/profile-guided-optimization.html](https://doc.rust-lang.org/rustc/profile-guided-optimization.html)

* **BOLT - Linux ELF Layout Optimization**  
  BOLT (Facebook/Meta project) has merged into LLVM code tree. <br>
  The BOLT + LTO + PGO combination gives a impressive performance uplift (34 % to 68.5 %) to many Clang (LLVM) and GCC compiled programs, see article below. Including the Kernel, and even the Clang and GCC compilers execution. <br>
  **BOLT Merged Into LLVM To Optimize Binaries For Faster Performance** <br>
  [https://www.phoronix.com/scan.php?page=news_item&px=LLVM-Lands-BOLT](https://www.phoronix.com/scan.php?page=news_item&px=LLVM-Lands-BOLT) <br>
  **Facebook Has Been Working On BOLT'ing The Linux Kernel For Greater Performance** <br>
  [https://www.phoronix.com/scan.php?page=news_item&px=Facebook-BOLTing-The-Kernel](https://www.phoronix.com/scan.php?page=news_item&px=Facebook-BOLTing-The-Kernel) <br>
  **GitHub - BOLT** <br>
  [https://github.com/facebookincubator/BOLT/tree/main/bolt](https://github.com/facebookincubator/BOLT/tree/main/bolt)

* **Optimize for small executable binary size with no vectorization** <br>

```
[profile.release]
opt-level = z
```


## Rust bounds check removal

This forum thread shows well some ways to remove bounds check without the need to do a loop **for**  and **a iterator**, the case where bounds check are automatically removed, or without using the manual way ```get_unchecked()```. <br>

* **Is bound checking the only runtime cost of Rust?** <br>
  [https://users.rust-lang.org/t/is-bound-checking-the-only-runtime-cost-of-rust/66661](https://users.rust-lang.org/t/is-bound-checking-the-only-runtime-cost-of-rust/66661)

I have put here some examples from the previous forum thread of bounds check removal with a simple assert. Imagine that you have a loop with a index array that the compiler can’t easily know that it doesn’t need to bounds check a easy way to ensure that the bounds check will be removed is with the introduction of an **assert** **that will assure to the compiler it is safe**. In this case the assert only makes one bounds check outside a loop and all the bounds checks inside the look will disappear. <br>


``` Rust
// Instead of….
for i in array1.len() {
    println!("{} {}", array1[i], array2[i]);
}

// Do….
assert_eq!(array1.len(), array2.len());
for i in array1.len() {
    println!("{} {}", array1[i], array2[i]);
}
```


``` Rust
// This does three bounds checks
pub fn demo1(x: &[i32]) -> i32 {
    x[0] + x[1] + x[2]
}

// Whereas these two examples each only have one bounds check:
pub fn demo2(x: &[i32]) -> i32 {
    assert!(x.len() >= 3);
    x[0] + x[1] + x[2]
}

pub fn demo3(x: &[i32]) -> i32 {
    let x = &x[..3];
    x[0] + x[1] + x[2]
}
```

* **Removal of bounds checks in extreme cases.** <br>
  Rust has **slice**, **array** and **Vec** bounds checks for each indices. <br>
  If you **use iterators** there will be **no bounds check**. <br>
  But in the common case Rust uses LLVM, and **LLVM** does a very good job at **removing the bounds checks that aren't needed**. <br>
  But if you need the fastest code implementation and want to **remove bounds check**, you can use ```get_unchecked()``` and ```get_unchecked_mut()```, they must be inside a **unsafe** block. <br>

``` Rust
let x = &mut [1, 2, 4];

unsafe {
    let elem = x.get_unchecked_mut(1);
    *elem = 13;
}
assert_eq!(x, &[1, 13, 4]);

```

* For the use case of **2D Vec** ```get_unchecked_mut()``` see the following code and benchmarks. <br>
  Performance of naive matrices in rust <br>
  [https://gist.github.com/TianyiShi2001/7f83854b91a94f3eaf3145084db6d627](https://gist.github.com/TianyiShi2001/7f83854b91a94f3eaf3145084db6d627)

``` Rust
// Normal performance: 84,694,933 ns/iter (+/- 7,412,836)

// This optimization:  41,440,947 ns/iter (+/- 752,463)   [x2 times faster]

fn bench_vec_of_vec_unsafe(b: &mut Bencher) {
    let (m, n) = (10000, 10000);
    let mut matrix = vec![vec![0u8; n]; m];
    b.iter(|| {
        for i in 0..m {
            for j in 0..n {
                unsafe {
                    *matrix.get_unchecked_mut(i).get_unchecked_mut(j) = 1u8;
                }
            }
        }
    });
}
```


## Notes - General

* Enum Option - Option.copied() 

```rust
// y_copy is a new Option of the cloned char 'a'.
// x is Option<&T> and the y_copy is Option<T> . 
let c: char = 'a';
let x: Option<&char> = Some(&c);
let y_copy: Option<char>  = x.copied();  // =>  Option<char>
```

* Trait Iterator - Iterator.copied() <br>
  Example modified from std lib docs.

```rust
// Trait Iterator - Iterator.copied()
// Creates an iterator which copies all of its elements.
// This is useful when you have an iterator over &T, but you need an iterator over T.

let a = [1, 2, 3];

{
    // Vector of references &T , &i32
    let v_copied_ref: Vec<&i32> = a.iter().collect();
}

// Vector of copied items T , i32
let v_copied: Vec<i32> = a.iter().copied().collect();

// You should write the Vec type like this "vec<_>".
// let v_copied: Vec<_> = a.iter().copied().collect();

// Copied is the same as .map(|&x| x)
let v_map: Vec<_> = a.iter().map(|&x| x).collect();

assert_eq!(v_copied, vec![1, 2, 3]);
assert_eq!(v_map, vec![1, 2, 3]);

// Better and faster to just transform an array into a Vec.
let v_copied_2 = a.to_vec();
assert_eq!(v_copied_2, vec![1, 2, 3]);

```


## Notes on optimization

* A **good example of applying optimization technics** to a high performance Rust program. <br>
  **Writing the Fastest GBDT Library in Rust by Isabella Tromba** - RustConf 2021 <br>
  [https://www.youtube.com/watch?v=D1NAREuicNs](https://www.youtube.com/watch?v=D1NAREuicNs)

* **ndarray - N dimensional array** <br>
  Crate ndarray <br>
  [https://crates.io/crates/ndarray](https://crates.io/crates/ndarray) <br>
  **Rust by example** - N Dimensional arrays <br>
  [https://rust-by-example-ext.com/ndarray.html](https://rust-by-example-ext.com/ndarray.html) <br>
  ndarray for numpy users <br>
  [https://docs.rs/ndarray/0.12.1/ndarray/doc/ndarray_for_numpy_users/index.html](https://docs.rs/ndarray/0.12.1/ndarray/doc/ndarray_for_numpy_users/index.html) <br>
  Rust Cookbook - **Linear Algebra** <br>
  [https://rust-lang-nursery.github.io/rust-cookbook/science/mathematics/linear_algebra.html](https://rust-lang-nursery.github.io/rust-cookbook/science/mathematics/linear_algebra.html) <br>
  Multidimensional Arrays and Operations with NDArray <br>
  [https://datacrayon.com/posts/programming/rust-notebooks/multidimensional-arrays-and-operations-with-ndarray/](https://datacrayon.com/posts/programming/rust-notebooks/multidimensional-arrays-and-operations-with-ndarray/) <br>
  ndarray-examples <br>
  [https://github.com/rust-ndarray/ndarray-examples](https://github.com/rust-ndarray/ndarray-examples) <br>
  For examples of usage, see ndarray project **github** in the **folders examples** and **tests** <br>
  [https://github.com/rust-ndarray/ndarray](https://github.com/rust-ndarray/ndarray)

* **smallvec** - **"Small vector"** optimization for Rust: store up to a small number of items **on the stack**. <br>
  [https://crates.io/crates/smallvec](https://crates.io/crates/smallvec)

* The HashMap in Rust uses strong cryptographic hashing for security reasons, but if the developer needs the fastest HashMap performance it can use an external faster and less secure hash function. <br>
**HashMap.with_hasher() info** <br>
[https://doc.rust-lang.org/beta/std/collections/struct.HashMap.html#method.with_hasher](https://doc.rust-lang.org/beta/std/collections/struct.HashMap.html#method.with_hasher) <br>
Insert crate **fasthash** into ```.toml``` file <br>

```Rust
use std::collections::HashMap;
use fasthash::murmur2::Murmur2_x86_64;

let s = Murmur2_x86_64::new();
let mut map = HashMap::with_hasher(s);
map.insert(1, 2);
```

* **But for a even faster HashMap or HashSet use**, <br>
  **hashbrown** - **Faster drop in replacement for STD HashMap and HashSet**, a Rust port of Google's high-performance SwissTable hash map. <br>
  [https://github.com/Amanieu/hashbrown](https://github.com/Amanieu/hashbrown) <br>
  Insert crate **hashbrown** into ```.toml``` file <br>

```Rust
// The fastest HashMap for Rust. HashBrown a drop in replacement for std HashMap.
use hashbrown::HashMap;
```  

* **bstr** - A **fast string type** that is not required to be valid UTF-8. **No heavy UTF-8 validations.** <br>
  [https://crates.io/crates/bstr](https://crates.io/crates/bstr)

* **SmartString with LTO** (global Link-Time Optimization) <br>
  It’s a general faster (**2.5x faster**) string replace for small strings <= 23 bytes (23 ASCII characters ex: “Mary had a little lamb!”) that are only stack allocated, but with the same performance as String for longer strings that are heap allocated. <br>
  **Rust benchmark String vs SmartString and LTO** <br>
  [https://github.com/joaocarvalhoopen/Rust_benchmark_String_vs_SmartString_and_LTO](https://github.com/joaocarvalhoopen/Rust_benchmark_String_vs_SmartString_and_LTO) <br>
  **Crate SmartString** <br>
  [https://crates.io/crates/smartstring](https://crates.io/crates/smartstring)

```Rust
// In main do.
smartstring::validate();

{
   // In the scope, add the alias to replace normal Strings with SmartString.  
   use smartstring::alias::String;

   // When creating SmartString's from &str instead of doing:
   "blabla".to_string()

   // Do:
   String::from("blabla")
}
```

* **bumpalo - A fast bump heap allocation arena for Rust.** <br>
  [https://crates.io/crates/bumpalo](https://crates.io/crates/bumpalo)

* **How to use multiple variables in Rust's for loop?** <br>
  [https://stackoverflow.com/questions/43302808/how-to-use-multiple-variables-in-rusts-for-loop](https://stackoverflow.com/questions/43302808/how-to-use-multiple-variables-in-rusts-for-loop)

* **The ASM! macro to insert inline Assembly** <br>
  New inline assembly syntax <br>
  [https://blog.rust-lang.org/inside-rust/2020/06/08/new-inline-asm.html](https://blog.rust-lang.org/inside-rust/2020/06/08/new-inline-asm.html) <br>
  ASM! at the Unstable Book <br>
  [https://doc.rust-lang.org/beta/unstable-book/library-features/asm.html](https://doc.rust-lang.org/beta/unstable-book/library-features/asm.html)


## Rust substring processing

* Rust string processing is kind of hard, because text in a UTF-8 world has many complex details, and Rust exposes all that power and all that complexity to you, the programmer. Sometimes it can be over whelming. Sometimes you only want to have a simple substring or a slice and you don’t mind to pay it’s cost, because you really need this feature and the Standard Library doesn’t help you a lot there.

* Fortunately **carlomilanesi** made this code available to all <br>
[https://users.rust-lang.org/t/how-to-get-a-substring-of-a-string/1351/11](https://users.rust-lang.org/t/how-to-get-a-substring-of-a-string/1351/11)

* But if you have to do many text operations based on the positions of chars inside a strings this isn’t a really good option, because you have to scan all the strings to the correct position, from the start, to have the string divided it into the correct boundaries of the chars. In this context, you would happily pay a up front cost of transforming the string into a Vec<char>, Vec of chars with individual chars separated, and process it as positional chars with access cost of 1 and then, slice them, range them, append to them at the end (or if you need to append in the start or the middle paying the cost of copy to a new buffer, but you can do it if you need to). **The following code is my expansion** to the code of **carlomilanesi**. It will allow you to do it. <br>
You can find it also in my GitHub repository in… <br>

* **SubStrings, Slices and Random String Access in Rust** <br>
  [https://github.com/joaocarvalhoopen/SubStrings_Slices_and_Random_String_Access_in_Rust](https://github.com/joaocarvalhoopen/SubStrings_Slices_and_Random_String_Access_in_Rust) <br>
<br>


``` Rust
use std::ops::{Bound, RangeBounds};

trait StringUtils {
    fn substring(&self, start: usize, len: usize) -> &str;
    fn slice(&self, range: impl RangeBounds<usize>) -> &str;
    fn get_vec_chars(&self) -> Vec<char>;
}

impl StringUtils for str {
    fn substring(&self, start: usize, len: usize) -> &str {
        let mut char_pos = 0;
        let mut byte_start = 0;
        let mut it = self.chars();
        loop {
            if char_pos == start { break; }
            if let Some(c) = it.next() {
                char_pos += 1;
                byte_start += c.len_utf8();
            }
            else { break; }
        }
        char_pos = 0;
        let mut byte_end = byte_start;
        loop {
            if char_pos == len { break; }
            if let Some(c) = it.next() {
                char_pos += 1;
                byte_end += c.len_utf8();
            }
            else { break; }
        }
        &self[byte_start..byte_end]
    }
    fn slice(&self, range: impl RangeBounds<usize>) -> &str {
        let start = match range.start_bound() {
            Bound::Included(bound) | Bound::Excluded(bound) => *bound,
            Bound::Unbounded => 0,
        };
        let len = match range.end_bound() {
            Bound::Included(bound) => *bound + 1,
            Bound::Excluded(bound) => *bound,
            Bound::Unbounded => self.len(),
        } - start;
        self.substring(start, len)
    }
    fn get_vec_chars(&self) -> Vec<char> { self.chars().collect() }
}

trait StringUtilsVecChars {
    fn to_string(&self) -> String;
    fn to_string_buf<'a>(&self, buf: & 'a mut String) -> & 'a String;
}

impl StringUtilsVecChars for Vec<char> {
    fn to_string(&self) -> String { self.iter().collect() }
    fn to_string_buf<'a>(&self, buf: & 'a mut String) -> & 'a String {
        buf.clear();
        for c in self.iter() { buf.push(*c); }
        buf
    }
}

trait StringUtilsSlices {
    fn to_string(&self) -> String;
    fn to_string_buf<'a>(&self, buf: & 'a mut String) -> & 'a String;
}

impl StringUtilsSlices for [char] {
    fn to_string(&self) -> String { self.iter().collect() }
    fn to_string_buf<'a>(&self, buf: & 'a mut String) -> & 'a String {
        buf.clear();
        for c in self.iter() { buf.push(*c); }
        buf
    }
}

fn main() {
    let s = "abcdèfghij";
    // All three statements should print:
    // "abcdè, abcdèfghij, dèfgh, dèfghij."
    println!("{}, {}, {}, {}.",
        s.substring(0, 5),
        s.substring(0, 50),
        s.substring(3, 5),
        s.substring(3, 50));
    println!("{}, {}, {}, {}.",
        s.slice(..5),
        s.slice(..50),
        s.slice(3..8),
        s.slice(3..));
    println!("{}, {}, {}, {}.",
        s.slice(..=4),
        s.slice(..=49),
        s.slice(3..=7),
        s.slice(3..));

    // Allocating a string from Vec<char>.
    let mut vc = s.get_vec_chars(); 
    println!("{}, {}, {}, {}.",
        vc[..5].to_string(),
        vc.to_string(),
        vc[3..8].to_string(),
        vc[3..].to_string());

    // Reusing a String buffer from a Vec<char>.
    let mut buf = String::new();
    print!("{}, ", vc[..5].to_string_buf(& mut buf));
    print!("{}, ", vc[..].to_string_buf(& mut buf));
    print!("{}, ", vc[3..8].to_string_buf(& mut buf));
    print!("{}.\n", vc[3..].to_string_buf(& mut buf));
    
    // Random access to the Vec<char>. 
    for i in 0..(vc.len() - 2) {
        print!("{} ", vc[i..i+3].to_string_buf(& mut buf));
    }
    println!("");
    
    // Random modifications to the Vec<char>.
    for i in (0..(vc.len() / 3) + 1).rev() {
        vc.insert(i*3, '#');
    }
    println!("{} ", vc.to_string());
    println!("{} ", vc.to_string_buf(& mut buf));
}

// Output:
//    abcdè, abcdèfghij, dèfgh, dèfghij.
//    abcdè, abcdèfghij, dèfgh, dèfghij.
//    abcdè, abcdèfghij, dèfgh, dèfghij.
//
//    abcdè, abcdèfghij, dèfgh, dèfghij.
//    abcdè, abcdèfghij, dèfgh, dèfghij.
//    abc bcd cdè dèf èfg fgh ghi hij 
//    #abc#dèf#ghi#j
//    #abc#dèf#ghi#j
```

## Macros in Rust

1. **Macro file visibility rules** <br>
   [https://users.rust-lang.org/t/3-things-that-the-rust-standard-library-should-have/68825/11](https://users.rust-lang.org/t/3-things-that-the-rust-standard-library-should-have/68825/11)

2. **Macros for hashMap, hashset, btreeMap, btreeSet to look similar to Python** <br>
  Crate **maplit** <br>
  [https://crates.io/crates/maplit](https://crates.io/crates/maplit)

```Rust
#[macro_use] extern crate maplit;

let map = hashmap!{
    "a" => 1,
    "b" => 2,
};

let map1: HashMap<String, String> = convert_args!(hashmap!(
    "a" => "b",
    "c" => "d",
));

let map2 = convert_args!(keys=String::from, hashmap!(
    "a" => 1,
    "c" => 2,
));
```

3. **Macro for graph's** <br>
   See the following post from kaj, on the Rust user foruns. <br>
   [https://users.rust-lang.org/t/3-things-that-the-rust-standard-library-should-have/68825/9](https://users.rust-lang.org/t/3-things-that-the-rust-standard-library-should-have/68825/9)

```Python
# When you have the following dictionary Python code...

# Adjacency list of graph
data = {
    0: [1, 2],
    1: [0, 2],
    2: [0, 1, 3, 5],
}
```

```Rust
// And you implement it in Rust like this...

let data = HashMap::from([
    (0, vec![1, 2]),
    (1, vec![0, 2]),
    (2, vec![0, 1, 3, 5]),
]);

// ...but you can instead implement it like this...

let data2 = graph![
    0 => 1, 2;
    1 => 0, 2;
    2 => 0, 1, 3, 5
];

// ...using the following simple Macro...

use std::collections::HashMap;

macro_rules! graph {
    [$($k:expr => $($v:expr),*);*] => {
        HashMap::from([
            $(($k, vec![ $($v),* ])),*
        ])
    }
}
```


## Good way to learn about the topic of computers and programming

1. **Video - Computer Science - Crash Course** <br> 
   [https://www.youtube.com/playlist?list=PL8dPuuaLjXtNlUrzyH5r6jN9ulIgZBpdo](https://www.youtube.com/playlist?list=PL8dPuuaLjXtNlUrzyH5r6jN9ulIgZBpdo)


## For a good challenge do the NAND To Tetris in Rust

1. **From Nand to Tetris** <br>
   Building a Modern Computer From First Principles <br>
   [https://www.nand2tetris.org/](https://www.nand2tetris.org/)

2. **Video - Shimon Schocken: The self-organizing computer course** <br>
   [https://www.youtube.com/watch?v=iE7YRHxwoDs](https://www.youtube.com/watch?v=iE7YRHxwoDs)

3. **Video - From Nand to Tetris Part I Course Promo** <br>
   [https://www.youtube.com/watch?v=wTl5wRDT0CU](https://www.youtube.com/watch?v=wTl5wRDT0CU)

4. **Free Course - Build a Modern Computer from First Principles** <br>
   From Nand to Tetris (Project-Centered Course) <br>
   [https://www.coursera.org/learn/build-a-computer](https://www.coursera.org/learn/build-a-computer)

5. **Free Course - Build a Modern Computer from First Principles** <br>
   Nand to Tetris Part II (project-centered course) <br>
   [https://www.coursera.org/learn/nand2tetris2](https://www.coursera.org/learn/nand2tetris2)


# All my other guides

* The links to all my guides are in: <br>
  **Guides on Linux - Programming - Embedded - Electronics - Aeronautics** <br>
  [https://github.com/joaocarvalhoopen/Guides_Linux-Programming-Electronics-Aeronautics](https://github.com/joaocarvalhoopen/Guides_Linux-Programming-Electronics-Aeronautics)


# Have fun
Best regards, <br>
Joao Nuno Carvalho <br>


