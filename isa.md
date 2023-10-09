# Instruction Set Architectures

## Instruction Sets

-   Reduced Instruction Set Computing (RISC)
    -   Example ISAs that are RISC-based: ARM, RISC-V
-   Complex Instruction Set Computing (CISC)
    -   Some ISAs that are CIRC-based: x86, x86_64

## Common Instruction Set Architectures

-   `x86`, `80x86` `IA-32`, `i386`, `i686`, `x86-32`
    -   `x86` refers to the Intel processor architecture that was used in PCs. Model numbers were 8088 (16-bit processor), 8086 (16-bit processor), 286, 386, 486.
    -   16-bit processors: 8086, 8088
    -   32-bit processors: 80386, 80486
        -   This is how the name `80x86` was born and over time the `80` was dropped, simplifying the name to just `x86`.
        -   32-bit processor implies a processor that is capable of addressing (accessing/working on) `2^32` bits of memory, which is around 4GB.
    -   Nowadays it roughly means any CPU with a 32-bit Intel compatible instruction set (usually anything from Pentium onwards). (Classic)
    -   Strictly speaking, `x86` covers all CPUs that are backwards-compatible with 8086 and all extensions to the architecture including `x86-32` and `x86-64`.
-   `x64`, `x86_64`, `x86-64`, `amd64`, `AMD64`
    -   `x64` is the architecture name for the extensions to the x86 instruction set that enable 64-bit code.
    -   `x64` means a CPU that is x86 compatible but has a 64-bit mode as well.
    -   The well-known 64-bit instruction set processors.
        -   64-bit processor implies a processor that is capable of addressing (accessing/working on) `2^64` bits of memory, which is around 16EB.
-   `IA64`, `IA-64`, `Itanium`
    -   **Not `x86`**, but is Intel's 64-bit architecture that failed to catch on unlike `amd64`.
-   `x32`
    -   `x32` is an [Application Binary Interface (ABI)](https://stackoverflow.com/questions/2171177/what-is-an-application-binary-interface-abi) for amd64/x86_64 CPUs using 32-bit integers, longs and pointers.
    -   Fairly new variant of `x86-64` and not widely used. Not to be confused with legacy/classic 32-bit instruction sets.
    -   Registers are 64 bits, but pointers are only 32 bits, saving a lot of memory in pointer-heavy workflows. It also ensures all the other 64-bit only processor features are available.

## Resources

-   RISC vs CISC
    -   [RISC vs. CISC](https://www.baeldung.com/cs/risc-vs-cisc)
    -   [risc vs. cisc](https://cs.stanford.edu/people/eroberts/courses/soco/projects/risc/risccisc)
-   [arm vs aarch64 vs amd64 vs x86_64 vs x86: What's the Difference?](https://itsfoss.com/arm-aarch64-x86_64)
    -   [Next-Gen CPU Acceleration: AVX For Generative AI](https://www.youtube.com/watch?v=bskEGP0r3hE)
-   [Difference between x86, x32, and x64 architectures?](https://stackoverflow.com/questions/7635013/difference-between-x86-x32-and-x64-architectures)
-   [The most correct way to refer to 32-bit and 64-bit versions of programs for x86-related CPUs?](https://stackoverflow.com/questions/53364320/the-most-correct-way-to-refer-to-32-bit-and-64-bit-versions-of-programs-for-x86)
-   [x86 vs x64 - Why is 32-bit called x86?](https://superuser.com/questions/179919/x86-vs-x64-why-is-32-bit-called-x86)
-   [What Is the Difference Between 32 Bit and 64 Bit (x86 vs x64)](https://www.partitionwizard.com/partitionmanager/x86-vs-x64.html)
-   [x64 vs. x86: Key Differences](https://phoenixnap.com/kb/x64-vs-x86)
-   [difference between i386:x64-32 vs i386 vs i386:x86_64](https://stackoverflow.com/questions/36347063/difference-between-i386x64-32-vs-i386-vs-i386x86-64)
-   [Are there performance advantages of 32 bit apps over 64 bit ones, on x86-64?](https://stackoverflow.com/questions/69852851/are-there-performance-advantages-of-32-bit-apps-over-64-bit-ones-on-x86-64)
-   [Security considerations of x86 vs x64](https://security.stackexchange.com/questions/255210/security-considerations-of-x86-vs-x64)
