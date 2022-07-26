
In the past decades we have witnessed major advances in the power of automated
reasoning engines like Satisfiability Modulo Theories (SMT) and Horn clause
solvers. As a consequence, there has been a renaissance of software
verification based on this technology. Currently, there are a number of mature
verifiers available coming both from academia and industry. However, despite
these advances, the bar for newcomer researchers to contribute to this field is
still very high. One of the main obstacles is the very large cost of
development of a new software verifier from scratch. Hence, several groups have
been independently working on implementing open software verification
infrastructures, which would allow for easier prototyping of research ideas in
this space, e.g., new algorithms for verifying relational or timing properties,
thereby democratizing software verification.

This workshop aims to bring together the developers of open software
verification infrastructures and their potential clients, meaning researchers
and practitioners interested in developing prototypes of software verification
algorithms. We will structure the workshop to facilitate the exchange of ideas
and discussions between the developers and clients. Hence, the workshop will
include invited talks on core verification infrastructures as well as
presentations of projects that already leverage these infrastructures. We also
hope to attract potential new clients as well, who would present the
requirements of their projects through a series of lightning talks. Through
open discussions we will solicit feedback from the community on the
requirements and functionality that open research infrastructures should
include to make them more widely usable.

As further discussion topics, we will solicit talks and feedback on
benchmarking issues, reproducibility, input languages, and potential license
issues, all of which are important to have a viable software verification
research ecosystem that can be leveraged by both industry and academia.


## Location

Ullmann 300, The Technion, Haifa, Israel


## Program

| Time  | Description |
| ------------- | ------------- |
| 8:30-9:00 | Coffee and Refreshments |
| 9:00-9:45  | Elizabeth Polgreen (University of Edinburgh) and Yatin Manerkar (University of Michigan): *UCLID5: Multi-Modal Formal Modeling, Verification, and Synthesis* |
| 9:45-10:30  | Kuldeep Meel (National University of Singapore): *Democratizing SAT Solving* |
| 10:30-11:00 | Coffee Break |
| 11:00-11:45 | Zafer Esen (Uppsala University): *Eldarica and TriCera: Towards an Open Verification Framework* |
| 11:45-12:30 | Gennaro Parlato (University of Molise): *C2C-Trans as a Design Methodology for Software Verification Tools* |
| 12:30-14:00 | Lunch Break |
| 14:00-14:45 | Yakir Vizel (Technion): *Solving Constrained Horn Clauses Lazily and Incrementally* |
| 14:45-15:30 | Hila Peleg (Technion): *Interaction Models vs. Formal Models: Synthesis Co-Design* |
| 15:30-16:00 | Coffee Break |
| 16:00-16:45 | Jaroslav Bendik (Certora): *Formal Verification of Ethereum Smart Contracts: SMT-Based Approaches and Challenges* |
| 16:45-17:30 | Matthias Schlaipfer (Amazon Web Services): *TBD* |
| 18:00-19:30 | Workshop Dinner (Technion, Taub Terrace Floor 2) |


## Invited Speakers

### Elizabeth Polgreen (University of Edinburgh) and Yatin Manerkar (University of Michigan):
*UCLID5: Multi-Modal Formal Modeling, Verification, and Synthesis*

**Abstract:**
UCLID5 is a tool for the multi-modal formal modeling, verification, and
synthesis of systems. It enables one to tackle verification problems for
heterogeneous systems such as combinations of hardware and software, or those
that have multiple, varied specifications, or systems that require hybrid modes
of modeling. A novel aspect of UCLID5 is an emphasis on the use of
syntax-guided and inductive synthesis to automate steps in modeling and
verification. In this talk we will present new developments in the UCLID5 tool
including new language features, integration with new techniques for
syntax-guided synthesis and satisfiability solving, support for hyperproperties
and combinations of axiomatic and operational modeling, demonstrations on new
problem classes, and a robust implementation.

**Short bios:**
Yatin A. Manerkar is an Assistant Professor in the Computer Science and
Engineering Division at the University of Michigan. His research lies on the
boundary between formal methods and computer architecture, and develops
automated formal methdologies and tools for the design and verification of
computing systems. He is a contributor to the UCLID5 verification framework.

Elizabeth Polgreen is an Assistant Professor in the School of Informatics
at the University of Edinburgh. Her research focuses on formal synthesis and
verification, and the integration of the two. She is one of the main developers
of the UCLID5 tool, so please get in touch with her if you have applications
for UCLID5 in mind.

### Kuldeep Meel (National University of Singapore): *Democratizing SAT Solving*

**Abstract:**
Boolean satisfiability is a fundamental problem in computer science with a wide
range of applications including planning, configuration management, design and
verification of software/hardware systems. The annual SAT competition continues
to witness impressive improvements in the performance of the winning SAT
solvers largely thanks to the development of new heuristics arising out of
intensive collaborative research in the SAT community. Modern SAT solvers
achieve scalability and robustness with complex heuristics that are challenging
to understand and explain. Consequently, the development of new algorithmic
insights has been largely restricted to experts in the SAT community.

I will describe our project that boldly aims to democratise the design of SAT
solvers. In particular, our project, called CrystalBall, seeks to develop a
framework to provide white-box access to the execution of SAT solver that can
aid both SAT solver developers and users to synthesize algorithmic heuristics
for modern SAT solvers?We view modern conflict-driven clause learning (CDCL)
solvers as a composition of classifiers and regressors for different tasks such
as branching, clause memory management, and restarting, and we aim to provide a
data-driven automated heuristic design mechanism that can allow experts in
domains outside SAT community to contribute to the development of SAT solvers.

**Short bio:**
Kuldeep Meel holds the NUS Presidential Young Professorship in the School of
Computing at the National University of Singapore. His research interests lie
at the intersection of Formal Methods and Artificial Intelligence. He is a
recipient of the 2019 NRF Fellowship for AI and was named AI's 10 to Watch by
IEEE Intelligent Systems in 2020. His research program's recent recognitions
include the 2022 ACM SIGMOD Research Highlight, IJCAI-22 Early Career
Spotlight, 2021 Amazon Research Award, "Best of PODS-21" invite from ACM TODS,
"Best Papers of CAV-20" invite from FMSD journal, IJCAI-19 Sister conferences
best paper award track invitation.


### Zafer Esen (Uppsala University): *Eldarica and TriCera: Towards an Open Verification Framework*

**Abstract:**
This talk will give a hands-on introduction to the software verification
infrastructure consisting of the Horn solver Eldarica and the C model checker
TriCera. After giving a high-level overview, the presenter will provide
examples on how the tools can be used / extended for prototyping research
ideas. Both tools are open-source and implemented in Scala.

Eldarica is a Horn solver that supports, among others, Horn clauses over the
theories of integers, algebraic data-types, bit-vectors, arrays and the novel
theory of heaps that simplifies encoding programs with heaps. Input clauses go
through several preprocessing stages such as slicing, reachability analysis and
inlining before being passed on to the main CEGAR engine that attempts to
construct an abstract reachability graph that witnesses their satisfiability.

TriCera is a model checker for C programs that encodes input programs and
specifications into a set of Horn clauses that can then be input to a Horn
solver such as Eldarica or Z3/Spacer. TriCera mainly uses Eldarica for this
purpose due to the tight integration of the tools and the theory of heaps.
TriCera accepts most programs written in C11, and provides several other
features useful for researchers: - the declaration and usage of uninterpreted
predicates that can be seen as a form of inline assembler for Horn clauses,
which simplify experimenting with various encodings, - automatic inference of
loop invariants and function contracts, - parsing ACSL function contracts, -
timing constraints in C programs (similar to UPPAAL timed automata), -
concurrency.

**Short bio:**
Zafer Esen is a PhD student at Uppsala University under the supervision of
Philipp Rümmer, Tjark Weber and Wang Yi. He is one of the main developers of
the Horn-based C model checker TriCera. Over the past four years he has also
contributed to the Eldarica Horn and the Princess SMT solvers, mainly to
support the theory of heaps.


### Gennaro Parlato (University of Molise): *C2C-Trans as a Design Methodology for Software Verification Tools*

**Abstract:**
I will report on a number of tools we have designed and implemented for the
analysis of multi-threaded C programs. Our solutions share the common pattern
of rewriting the original program into an equivalent non-deterministic
sequential C program that is then fed to an existing well-performing
model-checking tool for the analysis. Our translations have been optimized to
take maximum advantage of the back-end technology used for the analysis. Using
this paradigm we have designed a few bug-finding approaches that use back-ends
based on bounded model-checking, as well as approaches to prove the correctness
of programs. I will also report on recent approaches that we are developing to
develop distributed bug-finding algorithms that make use of the large
availability of processors provided by computer clusters or cloud computing
platforms.

**Short bio:**
Gennaro Parlato is an Associate Professor of Computer Science at the University
of Molise (UNIMOL) where he leads the Program Analysis in Clouds (PAC) research
group. Before joining UNIMOL, Gennaro enjoyed a long international research
career.  Between 2006 and 2011, he worked as a postdoctoral research associate,
first in the Department of Computer Science at UIUC (Urbana, USA, May
2006-March 2010), and then in the Modeling and Verification research group at
LIAFA (now IRIF) Laboratory (Paris, France, April 2010-April 2011). From 2011
to 2018, Gennaro was an academic at the University of Southampton's Department
of Electronics and Computer Science, first as a Lecturer and then as an
Associate Professor. While at the University of Southampton, Gennaro was also a
member of the GCHQ/EPSRC Academic Centre of Excellence for Cybersecurity
Research. Gennaro received his doctorate in Computer Science from the
University of Salerno, Italy, in April 2006. Gennaro is interested in software
verification and in building reliable and secure software systems using formal
correctness techniques.

### Yakir Vizel (Technion): *Solving Constrained Horn Clauses Lazily and Incrementally*

**Abstract:**
Constrained Horn Clauses (CHCs) is a fragment of First Order Logic (FOL), that
has gained a lot of attention in recent years. One of the main reasons for the
rising interest in CHCs is the ability to reduce many verification problems to
satisfiability of CHCs. For example, program verification can naturally be
described as the satisfiability of CHCs modulo a background theory such as
linear arithmetic and arrays. To this end, CHC-solvers can be used as the
back-end for different verification tools and allow to separate the generation
of verification conditions from the decision procedure that decides if the
verification conditions are correct or not.

In this talk, we present a novel framework, called LazyHorn, that is aimed at
solving the satisfiability problem of CHCs modulo a background theory. The
framework is driven by the idea that a set of CHCs can be solved in parts,
making it an easier problem for the CHC-solver. Furthermore, solving a set of
CHCs can benefit from an interpretation revealed by the solver for its subsets.
LazyHorn is lazy in that it gradually extends the set of checked CHCs, as
needed. It is also incremental in its use of a CHC solver, supplying it with an
interpretation, obtained for previously checked subsets. We have implemented an
efficient instance of the framework that is restricted to a fragment of CHCs
called linear CHCs.

**Short bio:**
Yakir Vizel is an Assistant Professor in the Computer Science Department at The
Technion. Previously he was a Postdoctoral Research Associate at Princeton
University in the Electrical Engineering Department. He has received a B.Sc. in
Mathematics and CS from the Technion and a Ph.D. in CS from the Technion. He
has worked on developing Formal Verification algorithms and tools for hardware
and software verification at Intel, Jasper Design Automation, Cadence, Mellanox
and NVIDIA.

### Hila Peleg (Technion): *Interaction Models vs. Formal Models: Synthesis Co-Design*

**Abstract:**
Program synthesis is the problem of generating a program to satisfy a
specification of user intent. Since these specifications are usually partial,
this means searching a space of candidate programs for one that exhibits the
desired behavior. A lion’s share of the work on program synthesis focuses on
new ways to perform the search, but allowing the user to communicate intent
remains a major challenge.

This talk focuses on the complex relationship between user intent,
specifications, and interaction model. In the domain of program synthesis, we
narrow our focus by targeting a more specific category of users. Focusing on
any subgroup of users allows making assumptions on both the input the user can
generate for the synthesizer and the output they can consume. In the case of
developers, concepts that are part of the programmer’s life such as code review
and read-eval-print loops (REPL) can be leveraged for interactions with a
synthesizer. The talk describes two synthesis-based tools that both leverage
and cater to programmers as their users.

These assumptions also drive ways in which the hard problems of formal methods
can be delegated to incomplete assistants: (bounded resource) solvers are a
community favorite, and ML models are also gaining traction as an approach for
deciding a hard subproblem. A third option, less sound than a solver and less
decisive than a model, is a human: delegating parts of the task back to the
user ensures that they are solved to the user's satisfaction. But how to make
the user work for the tool, rather than the other way around, is a critical
issue that must be addressed at the intersection of intent, specification, and
interaction model.

Synthesizer design shows us how these elements can be at odds with each other,
in particular the tension between the interface and state of the art synthesis
techniques. Synthesis is, at best, a computationally hard problem, and many
existing program synthesis tools and techniques were designed around the
synthesizer and its internals, their user interface dictated by the needs of
the synthesizer. We demonstrate the process of concurrently building both the
synthesizer and its intended user-facing tool as a way to search for a balance
of the needs of the interaction model (and, implicitly, the user) and the
algorithm.

**Short bio:**
Hila Peleg is an Assistant Professor at the Technion in Haifa, Israel. She
recieved her PhD at the Technion, Israel and was a postdoctoral researcher at
UC San Diego with Nadia Polikarpova. Her research explores the way PL
technology in general and program synthesis specifically can be transformed
into tools for developers.

### Jaroslav Bendik (Certora): *Formal Verification of Ethereum Smart Contracts: SMT-Based Approaches and Challenges*

**Abstract:**
Ethereum Smart Contracts become a widely adopted technology to
buildDecentralized Financial Applications (DeFis) and as such, they alreadyhold
200 billion USDs. Consequently, bugs in smart contracts can beexploited by
malicious users and can lead to losses at the scale ofmillions or even billions
of USDs. To prevent such situations fromhappening, there has been a growing
interest in developing scalableformal verification techniques for this domain.
In this talk, we willspecifically focus on the architecture of the Certora
VerificationTool, i.e. an industrial standard automated prover technology
toverify smart contracts. Besides a brief overview of the overall
toolarchitecture, we will focus mainly on the SMT-based subroutines,including
features such as domain-specific CEGAR methodology,distributed solver-portfolio
approach, or techniques to share andexploit information between individual SMT
solvers.

**Short bio:**
Jaroslav received his Ph.D. in the areas of formal verification and constraint
processing. He is the main developer of several state-of-the-art tools for
analysing infeasible Boolean and SMT constraint systems (e.g., UNIMUS or
ReMUS), and his work was published at more than a dozen major conferences in
the field. After following an academic career path as a postdoc at National
University of Singapore and Max Planck Institute for Software Systems, Jaroslav
switched to industry and nowadays is a core researcher and developer of the SMT
prover technology at Certora.

### Matthias Schlaipfer (Amazon Web Services): *TBD*

**Abstract:**
TBD

**Short bio:**
TBD

## Registration

Please register for the workshop through the FLoC registration [page](https://www.floc2022.org/registration).


## Organization

This workshop will be held on August 11, 2022, and colocated with the [34th International Conference on Computer-Aided Verification (CAV)][CAV]. The workshop is chaired by developers of [SMACK] and [SeaHorn]:

* Michael Emmi, Amazon Web Services
* Arie Gurfinkel, University of Waterloo
* Temesghen Kahsai, Amazon Devices
* Jorge Navas, Certora
* Zvonimir Rakamaric, Amazon Web Services

[SMACK]: http://smackers.github.io
[SeaHorn]: https://seahorn.github.io
[CAV]: http://i-cav.org/2022/

