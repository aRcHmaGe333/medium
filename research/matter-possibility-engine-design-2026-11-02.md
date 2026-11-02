# Matter Possibility Engine — System Design 0.1
**Originator:** Slavko Stojnić  
**Date:** 2026-11-02  
**Status:** Architectural specification. Computational feasibility and physical discoveries are unverified.  
**Companion:** [Scientific foundation](cross-vector-polymer-discovery-2026-11-02.md)

## 1. Purpose

Create a continuously expanding system that **invents, constructs digitally, investigates and ultimately enables physical construction of unfamiliar matter and capabilities of matter**. Initially polymers and molecular assemblies; extend to novel monomers, inorganic and hybrid materials, other molecular architectures, and ultimately higher-order systems exhibiting unfamiliar emergent behaviour.

The engine is not a product optimizer or a collection of known compounds. Its primary products are (a) new constructible matter and mechanisms, (b) explanations and reusable principles that open entire families of possibilities, (c) construction pathways, and (d) reproducible evidence. Scientific publication and IPClaim accompany demonstrated advances.

**Design criterion:** Any exploration or modelling component must improve the system's ability to make, discover or explain something; the available compute determines fidelity and throughput, not the scope of the architecture.

## 2. Objects and representations

The system uses typed objects, because a coordinate in a property embedding is not a molecule.

1. **Building block:** atoms/isotopes, composition, charge, bonding graph and stereochemistry; monomers and proposed monomers with attachment/active sites and candidate reactions.
2. **Structure:** molecular graph, polymer repeat units and sequences, branches, crosslinks, mixed chemistry, network topology, conformations and ensembles; explicit degree of polymerization/distribution rather than only a repeating-unit SMILES.
3. **Assembly:** interfaces and spatial arrangements among molecules, aggregates, phases, membranes, supramolecular networks and potential self-assembled structures.
4. **Environment and history:** temperature, pressure, fields, solvent/medium, reactive species, mechanical loading, elapsed time, synthesis and exposure history, and boundaries.
5. **State/trajectory:** electronic, structural, mechanical, thermal, optical, transport, chemical and temporal states, with units and uncertainty. Trajectories P(t,E,H) allow ageing, transformation, repair, memory and life-like dynamics to be discovered.
6. **Candidate:** proposed structure + assembly + environment + generation lineage + predicted states. Candidate existence is not evidence of viability.
7. **Mechanism:** proposed causal relation among constituent structure, conditions, transformations and resulting behaviour; includes tests that could disprove it.
8. **Discovery:** reproducible evidence of a new construction or principle, linked to all candidate, simulation and measurement records.

Each object has a stable content hash and provenance. Store unknown, predicted, computed and experimentally measured values distinctly. Preserve model versions, raw outputs and random seeds.

## 3. Closed discovery and construction loop

**Invent → construct digital candidate → establish viable representations → model and perturb → observe properties and temporal behaviour → compare with rules → propose mechanisms → generate further candidates → archive and promote discoveries.**

**Invent:** Novel random building blocks and connectivity; mutations; sequence recombination; hybridization across unrelated chemistry families; learned proposals; directed exploration of poorly mapped parts of descriptor space. Sampling rates are adjustable and include uncompromised random exploration.

**Construct:** Convert an abstract proposal into an explicit molecular graph and possible assembly, checking valence, charge, bonding and basic physical plausibility using the selected chemistry model. Record unresolved proposals as speculative, rather than discarding them or labeling them impossible.

**Model:** Start with inexpensive validity/structural descriptors and surrogate models. Escalate select candidates to force fields, conformational searches, molecular dynamics, quantum chemistry, coarse-grained simulations, and reactive/time-evolution models as appropriate. Surrogates estimate uncertainty and can abstain outside their domain. A digital twin of a physical counterpart exists only after calibration against measurements.

**Observe:** Capture properties not preselected as optimization targets; include changes across conditions and time, unusual responses, failures and unanticipated correlated effects. A fixed library of measurable observables can be extended whenever new mechanisms require new measurements.

**Understand:** Extract regularities, anomalies, apparent impossibilities and candidate causal explanations. Suggest new simulations or experiments that distinguish competing explanations.

**Exploit:** When a mechanism is promising, generate an entire family around it, seek feasible precursors and reaction/assembly pathways, and record the route to physical construction. Scientific claims and public evidence follow the actual maturity of the discovery.

## 4. Directional exploration: DnD randomness, divergence and crosses

Represent candidates in several **separately defined** spaces: chemical structure, composition, properties, behaviour, trajectories and learned descriptors. Keep the space and normalization attached to every directional claim; distances and angles are not interchangeable across spaces.

**Dissimilar parents:** Choose A and B with angular difference theta at least an adjustable threshold (initial heuristic 90 degrees) in a selected centered, normalized representation. This is a diversity *search rule*, not a chemically universal metric; test different thresholds and also pairs that fail it. Degenerate zero vectors have undefined angle and use a different selection rule.

**Intermediate:** Probe vectors between A and B, with random or systematic combination weights. To make a material rather than a vector, use constrained decoders, explicit graph recombination, or structure edits; retain both the desired descriptor target and the actual reconstructed result. If no feasible reconstruction exists, preserve the failed target as information about the model.

**Cross:** On any chosen 2-D projection, for discovered direction g=(x,y), also investigate (-x,y), (-x,-y), (x,-y). The original, the two mirrors and the opposite constitute one linked discovery group. Repeat across changing subspaces and origins, not just a global x/y pair. Above-ground mirrors correspond to the same positive y and negative x in a projection whose positive y denotes the chosen viable/upward direction; this visual convention does **not** make positive y inherently biologically safe.

**Boundary-seeking:** Attempt opposite directions. When they lead to nonviable or unresolved candidates, investigate alternate constructions and viable *nearby* targets, partial reflections and neighbouring paths. Record why an outcome failed and how well supported that conclusion is. A nearest viable mirror is an optimization objective, not an assumed existing mathematical object.

**Dice allocation:** Maintain parallel exploration budgets for pure random, divergent combinations, crosses/reflections, boundaries, unusual life cycles, explanatory tests and exploitation of breakthroughs. Keep a substantial random stream to find what the trained models did not imagine.

## 5. Life-cycle and emergent-system investigation

Every candidate is a potential **process**, not simply a static material. Simulate or emulate time where appropriate: bond formation/breakage, environmental changes, wear, oxidation, light-driven changes, diffusion, restructuring, state transitions, chain growth and degradation. Discover how behaviours depend on prior states, and whether cycles are stable, self-maintaining or self-propagating.

A layered ontology avoids conflating *organic chemistry*, *living systems*, and *information-bearing matter*. Life-like behaviour—homeostasis, energy throughput, reproduction, heredity and adaptation—is explored as graded observable capability, not assumed to activate merely from a carbon backbone. A model can define hypothetical systems and test consequences without claiming that a synthetic organism has been created.

## 6. Knowledge engine: rules, exceptions, impossibility frontiers

Maintain two coupled evolving models:
- **Prediction:** Expected state/behaviour of a defined structure in defined conditions, with calibration and uncertainty.
- **Explanation:** Explicit conditional rules and alternative mechanisms; their evidence, counterexamples, scope and proposed tests.

Index phenomena by **structure → environment/history → observed behaviour**, not by compound name alone.

For every apparent impossibility classify: (i) fundamental constraint from the chosen physical theory, (ii) strongly evidenced chemical/material incompatibility, (iii) construction pathway not yet known, (iv) model conflict or extrapolation, (v) failed candidate under specific conditions, or (vi) entirely unexplored. These labels may change as evidence improves.

Find frontier regions: collapsed empirical trade-offs, nonlinear transitions, symmetry-breaking cross results, sharp viability boundaries, novel dynamics, and high disagreement between plausible models. The engine can construct tests *specifically to disprove* a proposed rule, then update it.

Treat a newly established **mechanism yielding a family of buildable candidates** as more consequential than an isolated record-setting candidate.

## 7. Compute-independent architecture

The system consists of independently replaceable services and common records:

| Component | Responsibility | Low-compute expression | Higher-compute extension |
|---|---|---|---|
| Candidate maker | Emit well-described structures and assemblies | Graph-based stochastic generation | Generative models and reaction-aware search |
| Representation mapper | Project, reflect, recombine, inverse-map targets | Interpretable descriptors; heuristic graph edits | Calibrated equivariant or learned embeddings/decoders |
| Feasibility assessor | Characterize structural plausibility | Valence, known constraints, cheap estimates | Quantum/reactive predictions and measured synthesis |
| Physics/model runner | Produce candidate state and trajectories | Descriptors and small simulations | DFT, MD, reactive MD, multiscale models |
| Explorer | Allocate dice and directional/boundary search | Seeded reproducible policies | Adaptive novelty, active learning, quality-diversity |
| Rule discoverer | Learn dependence, anomalies, mechanisms | Transparent fits and counterexample search | Bayesian/symbolic causal-hypothesis pipelines |
| Knowledge archive | Retain all outcomes and their evidence | SQLite plus content-addressed blobs | Distributed database/object store |
| Builder interface | Convert findings to construction plans | Proposed pathways + status tags | Robot/automation or human laboratory execution |
| Publication/IP record | Preserve original claims and proof | Git commits and documentation | Verified IPClaim RFC3161 timestamp + releases |

Compute scheduler chooses model fidelity according to novelty, confidence, scientific impact and resource budget; expensive methods run only when they can change a consequential decision. Model provenance and uncertainty are mandatory because unfamiliar chemistry is most likely to lie outside prior training distributions.

## 8. Data contracts

Each candidate record includes:
`id; parent_ids; creation_operator; seed; representation_type; structure; assembly; requested_direction; achieved_direction; projection_basis; origin; angle_threshold; cross_group_id; environmental_conditions; time_history; model_runs; predicted_properties; observed_properties; uncertainty; failure_category; viable_status; novelty_dimensions; inferred_rules; physical_construction_status; evidence_links; citations; timestamps`.

A **model run** records model name/version, parameters, resource/time cost, raw output location and the limits of its applicability. Every newly asserted law or mechanism links to confirming and contradicting cases. Keep time evolution as an ordered set of states, with enough checkpointing to reproduce the claimed transition.

## 9. Scientific programme and milestone gates

**Gate A — operational discovery loop:** Reproducible generation and preservation of divergent parent pairs, intermediate candidates and complete four-way cross families; each has explicit structure/feasibility status, recorded properties and causal lineage. Evaluate against unstructured random search under equal budgets.

**Gate B — informative discovery:** Discovery of statistically reproducible cross asymmetries, previously unmodelled dependencies or anomalous behaviours across independent seeds and models; distinguish model artefacts from robust phenomena.

**Gate C — family-enabling mechanisms:** A rule or construction method produces a coherent novel family of stable candidates, with computational results validated by a genuinely distinct method.

**Gate D — matter built:** Synthesis/assembly, independent physical characterization, reproducible observed behaviour, and calibration of the digital model against measurements. This is the decisive threshold for a claim about newly constructed matter.

**Gate E — expanded possibility space:** New building-block families, material life cycles and emergent functions recursively become starting points for further invention. This is an ongoing capacity, not a final endpoint.

No gate assumes a fixed number of compounds as the outcome. The purpose is enlargement of what can be constructed and understood, with discoverable mechanisms that open new branches of possibility.

## 10. What remains unknown at design time

The most fruitful geometries and diversity measures, inverse mapping fidelity, coverage of unknown chemistries, feasible synthesis routes, length/time scales of emergent behaviours, and eventual compute required are **questions the system itself must help resolve**. They do not narrow the intended purpose. Architecture makes these assumptions replaceable and keeps the accumulated discoveries usable as models improve.

## 11. Authorship and scientific traceability

The original cross-vector, open-ended matter discovery and life-cycle exploration proposal is attributed to **Slavko Stojnić**. Existing techniques and prior publications retain their own attribution; see the companion research document. IPClaim declarations, licenses, verifiable timestamps and Git history document the contribution as it develops. This design is a disclosed specification, not evidence of a working implementation, a chemically feasible invention, a patent, or a completed independently verifiable IPClaim timestamp proof.
