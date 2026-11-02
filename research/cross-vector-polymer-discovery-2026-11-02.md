# Cross-Vector Exploration of Molecular Possibility Space: An Open-Ended Framework for Polymer and Material Discovery

**Author and originator of the proposed research direction:** Slavko Stojnić  
**Publication date:** 2 November 2026  
**Status:** Research proposal and testable methodological hypothesis; not an experimental report.

## Abstract

Contemporary computational materials discovery commonly generates candidates to improve specified properties. We propose a complementary, open-ended discovery system in which monomers, polymers, and potentially other molecular assemblies are generated and studied for properties and behaviours that need not be anticipated. The system explores dissimilar parents, constructs candidate combinations, and deliberately examines reflected and opposing directions in a representation of structural, functional, or temporal properties. It records not only successful candidates but failure modes, viability boundaries, unexpected symmetries, anomalous behaviours, environmental dependencies, and complete property trajectories over time. An evolving database supports both prediction and explicit induction and testing of explanatory rules. The research hypothesis is that controlled exploration of dissimilar and reflected candidate directions, coupled to boundary-seeking and life-cycle modelling, will discover more diverse and scientifically informative materials than conventional goal-directed selection under comparable computational budgets.

**Keywords:** polymer discovery; open-ended exploration; molecular design; diversity; symmetry; active learning; self-driving laboratories; materials informatics; digital twins; ageing; scientific discovery.

## 1. Scope and motivation

Monomers and polymers extend across organic, inorganic, and hybrid chemistry. DNA is one example of a polymer with information-bearing functionality, not the conceptual boundary of the proposed system. A sufficiently developed computational platform could represent ordinary and previously unexamined molecular building blocks, their assembly, their environments, and their time-dependent behaviour. The system's long-term target is to discover not only *which* structures are feasible but *what matter can do*, *under what circumstances*, *why*, and *how it changes*.

Here “digital twin” denotes the intended progressively calibrated simulation-and-measurement system; a purely generated and simulated material is initially a virtual candidate, not a validated twin of a physical sample.

## 2. Proposed exploration method

### 2.1 Random generation and representation

Generate structurally distinct candidate monomers, polymer repeat units, sequences, topologies, crosslinks, and mixed assemblies using a controlled mixture of random construction, structural mutations, recombinations and learned generators. Retain provenance and a reproducible random seed for every candidate. A representation may encode structural features, simulated properties, observed properties, and dynamical responses separately. Any learned embedding used for geometric searches must be evaluated for whether its distances and angles correspond to meaningful chemical or physical distinctions.

### 2.2 Dissimilar-parent combination

Select pairs of candidates whose descriptor vectors are deliberately divergent. The originating heuristic suggests an angular separation of approximately 90° or greater as one adjustable selection threshold, rather than a universal law or a necessary chemical condition. Generate hybrids or descendants from such pairs, including candidates predicted in an intermediate direction. The geometric midpoint identifies an exploration target, not a guarantee that a corresponding molecule exists or has interpolated properties.

### 2.3 Four-direction cross exploration

For a two-dimensional projection of a candidate exploration direction **g** = (x,y), probe:

- original: (x,y)
- mirror across the y-axis: (-x,y)
- opposite: (-x,-y)
- mirror across the x-axis: (x,-y)

The proposal generalizes these operations to multiple selected projections and feature subspaces. Such reflected points are *search targets*, translated through generation and constrained reconstruction into molecular candidates where possible. A reflection in descriptor space does not imply physical inversion of a molecule or automatic existence of a viable counterpart.

Every generated direction is associated with its entire cross and the outcome of each probe. The central scientific interest lies as much in asymmetry among mirrored outcomes as in any discovered symmetry.

### 2.4 Viability, “death,” and boundary exploration

The search tests direct opposites first. If a proposed direction corresponds to a nonviable or physically unrealizable outcome, it also explores nearby viable reflections and partial inversions. “Death” is an informal name for defined loss-of-viability conditions, not a single universal classification: examples include electronic or chemical instability, chain disintegration under tested conditions, failure of the intended assembly, or inability to preserve a chosen dynamic function. Unconstructable and untested cases remain distinct from established physical impossibilities. Failures are stored as boundary evidence, with confidence and model provenance.

A nearest-viable mirror is a *candidate* obtained by constrained search, not a mathematically guaranteed projection onto a known feasible manifold.

### 2.5 Life cycles and temporal properties

A candidate is evaluated not only at an initial state but, where models permit, over a trajectory **P**(t,E,H), where t denotes elapsed time, E the environment, and H exposure and processing history. Investigate ageing, degradation, repair, adaptation, state transitions, history dependence, and potential self-maintenance. Organic, inorganic, and hybrid material systems are eligible. Unusual histories—for example, strengthening followed by softening, or responses that depend on prior stimuli—are treated as possible discoveries, not prespecified success criteria.

### 2.6 Rules, explanations, and apparent impossibilities

In parallel with candidate generation, maintain an explicit evolving account of:
1. Observed and simulated regularities between composition, architecture, processing, conditions, and properties.
2. Dependencies and competing mechanistic explanations.
3. Exceptions, anomalies, uncertain regions, and apparent incompatibilities.
4. Proven feasibility boundaries versus merely missing observations or inadequate models.

The system proposes discriminating experiments or higher-fidelity simulations to decide between competing explanatory hypotheses. It actively explores locations where predicted trade-offs collapse, multiple materials achieve unlike results from superficially related structures, or model disagreement is high.

## 3. Architecture and records

A minimum implementation connects: (i) a candidate generator; (ii) chemical/structural validity checking; (iii) low-cost descriptors and surrogate predictions; (iv) selective quantum-chemical, molecular-dynamics or mesoscopic modelling as appropriate; (v) a persistent outcome and lineage database; (vi) a scheduler for randomness, divergence, reflection, novelty and uncertainty; and (vii) a rule-discovery and hypothesis-testing subsystem. Ultimately, experimental measurements should recalibrate both predicted properties and the learned viability boundaries.

Each record contains structural representation, generation operator and seed, ancestry, parent-space angles, projection definition, all cross directions, construction outcomes, environmental and temporal conditions, predicted/observed attributes, uncertainties, model/software versions, failures and their causes, inferred rules, and supporting evidence. Claims of novelty should distinguish database novelty, literature novelty, structural novelty, and experimentally validated novelty.

## 4. Testable evaluation

Compare the proposed search against random generation, standard property-directed active learning, novelty search, and quality-diversity methods using equal computation budgets and identical evaluation models. Evaluate:
- valid and nonduplicate structures found;
- diversity of structures, behaviours and property trajectories;
- coverage of feasible property space and viable boundary regions;
- robust violations of *expected empirical trade-offs* (not violations of physical law);
- explanatory rules discovered and their success on held-out or experimentally tested cases;
- unexpected cross-direction asymmetries;
- per-discovery computational and experimental cost.

Ablate the dissimilar-parent angle threshold, the four-direction cross, boundary exploration, temporal evaluation, and explanatory feedback individually. Register predictions ahead of validation. This makes the combined methodology falsifiable and separates its potential contribution from existing techniques.

## 5. Relationship to prior work and novelty boundary

Generative polymer models, reinforcement-learning-guided inverse design, closed-loop active learning, autonomous polymer laboratories, high-throughput virtual screening, and chemical-diversity control already exist. Therefore **none of these individual capabilities is claimed here as an invention**. This proposal's candidate contribution is their *particular integration*: intentionally dissimilar parent combinations; systematically generated cross/reflection families; explicit viable-boundary counterparts; open-ended time-dependent behaviour discovery; and continual explanatory-rule formation with deliberate exploration of apparent impossibilities.

A targeted literature review supports treating that integration as a **research hypothesis worth testing**, not as an established first-in-the-world method. Exhaustive novelty, patentability, or freedom-to-operate has not been established. Computational results, chemical feasibility, and physical synthesis remain to be demonstrated.

## 6. Limitations and research agenda

Feature-space angles depend on normalization and representation; most candidate vectors are not directly invertible into chemically valid structures; model uncertainty may dominate in unfamiliar molecular regions; material ageing can span incompatible time and length scales; and computationally plausible materials may be inaccessible to synthesis. These are measurable research problems to investigate, not reasons to restrict the exploration to established material families.

The first decisive demonstration is whether cross-vector and boundary-seeking exploration produces reproducible gains in *behavioral diversity and new explanatory findings*, rather than merely more unusual descriptor values.

## References

1. Cheng, M. et al. (2026). “Artificial intelligence-driven approaches for materials design and discovery.” *Nature Materials* 25, 174–190. https://doi.org/10.1038/s41563-025-02403-7
2. Li, W., Li, Y., Lei, Q., Wang, Z. & Wang, X. (2026). “PolyRL: reinforcement learning-guided polymer generation for multi-objective polymer discovery.” *Digital Discovery* 5, 266–276. https://doi.org/10.1039/D5DD00272A
3. Sahu, H. et al. (2026). “POLYT5: an encoder-decoder foundation chemical language model for generative polymer design.” *npj Artificial Intelligence* 2, Article 30. https://doi.org/10.1038/s44387-026-00087-1
4. Vogel, G. & Weber, J. M. (2025). “Inverse design of copolymers including stoichiometry and chain architecture.” *Chemical Science* 16, 1161–1178. https://doi.org/10.1039/D4SC05900J
5. Azzouzi, M., Worakul, T. & Corminboeuf, C. (2026). “NaviDiv: a web app for monitoring chemical diversity in generative molecular design.” *Digital Discovery* 5, 1579–1589. https://doi.org/10.1039/D5DD00487J
6. Tobias, A. V. (2025). “Autonomous ‘self-driving’ laboratories: a review of technology and policy implications.” *Royal Society Open Science* 12, 250646. https://doi.org/10.1098/rsos.250646
7. Alosious, S. et al. (2026). “PolyDiscover: an integrated trust-aware platform for multi-objective polymer discovery and simulation validation.” *arXiv* preprint, posted 28 October 2026. https://arxiv.org/abs/2610.38843
8. Zhang et al. (2026). “Active Learning-Accelerated Discovery of Antifungal Polymers With Self-Assembly Capacity for Tackling Invasive Fungal Diseases.” *Angewandte Chemie International Edition*. https://doi.org/10.1002/anie.3008697

## IPClaim — authorship and original-contribution declaration

**Author / claimant:** Slavko Stojnić.  
**Claimed contribution:** The original formulation and proposed integration recorded in this document, particularly its directed use of divergent candidate parents, four-direction reflected molecular exploration, viable-boundary alternatives, open-ended material life cycles, and the derivation and testing of rules and exceptions from an expanding materials database.

**Universal, evidence-based claim:** I claim, as my intellectual property, whatever can be claimed and is not already owned, claimed, or publicly disclosed by another. I do not need to specify in advance which parts of my work qualify as IP, nor under which category they fall. My claim applies to my original contribution as evidenced by this publication.

Existing scientific principles, independent earlier work, publicly disclosed methods, and prior third-party rights are excluded from the claim. This document records disclosure and a claim; it is not an issued patent, proof of patentability, or an independently timestamped IPClaim cryptographic token.

**IPClaim project and verification mechanism:** https://github.com/aRcHmaGe333/IPClaim . A GitHub commit provides a public repository record. The full IPClaim RFC 3161 independent timestamp proof is a separate step and is not asserted here unless a verifiable timestamp token is actually attached.
