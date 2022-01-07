# The paper that started it all...

[Universal Composability is Secure Compilation](https://arxiv.org/pdf/1910.08634.pdf)
- Marco Patrignani, Riad S. Wahby, Robert Künnemann

### Universal Composability

### Secure Compilation

In compiler verification, we look to prove a compiler correct by proving that it has a certain property.
For example, the (currently) "standard" property is _Semantics Preservation_ which states that compiled
program's _behaviour_ must be one of the source program's behaviours (must be the same) i.e. the compiler should not introduce _new_ behaviours.
Behaviour is dependent on a language's semantics -- For example, a language might have non-determinism (multiple behaviours) or might not
permit infinite loops (e.g. non-turing complete languages). Intuitively, the semantics of the source and target languages must be
similar/close enough to be given a notion of "behaves the same".  

Semantics preservation typically only works for compilers that process _whole programs_ e.g. semantics perservation does not apply
to cases where you link with a pre-compiled library, or libraries written in another language. This is precisely because programmers
are interested in linking/combining code from vastly different source languages where it is difficult to give their semantics a notion of "behaves the same".  

Consider compiled Java (a memory safe langauge) code that is linked against a C (a memory unsafe language) library.
*Secure compilation* is the current area of research that studies
- the properties of interest (to verify) in a separate compilation setting  i.e. what does it mean for our compiler to
maintain "memory safety" of the compiled Java code?
- what kind of guarantees about source level security (or really, any) abstractions we can provide in target code in a separate compilation setting.
i.e. How can we prove our compiler "maintains the memory safety of the compile Java code"? (Whatever that means).


##### SC papers
[Formal Approaches to Secure Compilation](https://theory.stanford.edu/~mp/mp/Publications_files/main-full.pdf)
- Marco Patrignani, Amal Ahmed, Dave Clarke
