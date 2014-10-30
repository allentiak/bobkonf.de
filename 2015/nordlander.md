---
layout: talk
active: bob2015
title: Clutching a grip on AUTOSAR using Haskell
speaker: Johan Nordlander
time: 16:15-17:00
portrait: nordlander.jpg
type: Vortrag
---

The AUTOSAR standard is an open software component architecture for
the automotive industry. Its main goal is to enable interoperability
of software modules among different vendors and on heterogeneous
platforms, via an extensive set of standardized interfaces and a
common software development methodology. As a software architecture,
AUTOSAR provides run-time support for concurrent execution,
communication, seamless distribution, and selected real-time
programming facilities.

However, the sheer size of the AUTOSAR specification (~ 12,500 pages
of pdf text and diagrams in version 4.1) obviously makes interpreting
the detailed meaning of many AUTOSAR concepts a challenging task. In
practice, the AUTOSAR standard is thus naturally approximated as the
specific behavior of one's chosen platform and development tools. This
phenomenon is not unique to AUTOSAR, and would perhaps not motivate
further attention, if it weren't for the following aspects of AUTOSAR
software development:

1. The scope of the AUTOSAR standard puts platform- and tool
   neutrality at the core of its features. Yet the AUTOSAR
   specification aims to cover complex technical areas that
   traditionally have only been associated with vendor-specific
   operating systems, real-time kernels, distribution frameworks, etc.

2. The size of typical automotive software systems makes distributed
   development and testing an absolute necessity. Yet, due to the
   inherent platform and tool dependencies, faithful testing of an
   arbitrary AUTOSAR subsystem can only be performed with the full
   software installation in place.

From this perspective, the platform- and tool-neutral system semantics
specified by the AUTOSAR standard is, or should be, the focus of
attention. Unfortunately, no authoritative formulation more accessible
than a 12,500 page textual specification appears to exist. Not only
does this make AUTOSAR development unnecessarily hard and error-prone,
it also hampers the emergence of platform-independent tools like
simulators, that could enable truly distributed development of
interoperable AUTOSAR subsystems.

The RAW FP project at Chalmers University of Technology seeks to
demonstrate how the technology of Domain Specific Languages (DSLs)
embedded in Haskell can be applied to serious industrial software
development problems. As one of its main validator tracks, RAW FP has
attempted to first formalize the core semantics of AUTOSAR, then
implement this semantics as a Haskell DSL that is executable on any
major platform under simulated real time. While the formalized
semantics captures every possible direction an AUTOSAR system can
evolve in at run-time, the embedded DSL defers its scheduling
decisions to a pluggable procedure that can select among all legal
execution paths. This feature has been put to good use in the
implementation of an AUTOSAR simulator with random scheduling, that
has the ability to reveal race conditions and other concurrency
problems much faster than the partially deterministic scheduler found
on typical AUTOSAR platforms. It has also been integrated with the
Chalmers QuickCheck tool, to systematically test randomized executions
against given properties and minimize any counter-example found.

In this talk I would like to give an overview of the AUTOSAR semantic
formalization we have carried out in the RAW FP project, and also show
how it has been concretized as a Haskell DSL. In the first part my
intent is to illustrate the level of precision at which one can (and
should!) study the behavior of complex concurrent real-time
systems. Some ambiguities and dubious features of the AUTOSAR
specification will also be emphasized, together with suggested paths
forward.

In the second part I plan to introduce the small Haskell-based AUTOSAR
DSL we have developed at Chalmers, and show how it can be readily used
to construct a non-trivial automotive system in the form of an ABS
implementation. A comparison with real AUTOSAR code and a discussion
on syntactic complexity will be inevitable here, as well as examples
of the kind of AUTOSAR validation checks that can be captured using
the Haskell type system alone. Simulation runs under different
scheduling policies will also be shown, and I'll demonstrate how the
addition of QuickCheck may help narrow down a race-condition that
real-world testing is likely not to have found.

The talk will conclude on the topic of platform independence versus
real-time authenticity, and the role functional programming may play
in bridging these seemingly opposite goals. The embedded DSL approach
will be in focus, of course, but also some open problems that stand in
the way of a more direct adoption of functional programming in the
resource-constrained industrial domain.



#### Johan Nordlander

Johan Nordlander holds a Ph.D. from Chalmers University of Technology
in 1999, and is currently dividing his time between a research
position at Chalmers and his work as a network management consultant
for Data Ductus AB. His research interests lie in the fields of formal
semantics, real-time constraints, programming language design, and
type systems. Nordlander has been deeply involved in the TIMMO and
TIMMO-2-USE projects, that provided the foundation for the Timing
Extension of the AUTOSAR standard. As a software professional, he is
mostly engaged in developing tools and techniques that support
software-defined networking.
