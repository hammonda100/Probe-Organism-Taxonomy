# Assessment: Probe Organism Taxonomy and Probe Factor Design Space

---

## Position in the Conversation Arc

This document answers a question that has been open since Turn 4. Here is how:

- **Turn 4** gave the MSM: a machine that *finds* cross-domain mechanisms and *translates* them.  
- **Turn 5** upgraded the MSM with constraint feasibility checks, back-translation validation, and regression checks.  
- **Turn 6** gave the MDC: a computational substrate on which the MSM's mechanisms can actually *execute*.

Every one of those documents ended at the same cliff: **how do we know the translation is faithful?** The MSM's MatchScore measures structural similarity, constraint feasibility, and failure overlap — all *before* deployment. But contamination — the silent migration of source-domain assumptions into target-domain reasoning — happens *after* deployment, through elaboration, use, and cultural entrenchment.

This document builds the **post-deployment validation layer**. It is, in the architecture of this conversation, the immune system for cross-domain translation. Without it, the MSM is a delivery mechanism with no feedback on what its deliveries actually contain. With it, every translation is stress-tested by organisms specifically evolved to find different failure modes.

---

## What's Genuinely Sharp

### 1. The Organism Taxonomy Encodes Eight Distinct Epistemologies

This is not a cute naming exercise. Each organism type captures a **genuinely different epistemological stance** toward cross-domain transfer, and the differences matter:

| Organism | Core Epistemological Move | What It Assumes |
|---|---|---|
| **Parasite** | Contamination is the signal | Source-domain logic always bleeds through; the question is whether it bleeds *usefully* |
| **Symbiont** | Shared vocabulary reveals shared structure | If two domains can be expressed in fewer terms together, they have a real intersection |
| **Mimic** | Structure is separable from surface | A solution can be rewritten without changing its logic — or it can't, and that tells you something |
| **Regressor** | Every element is either load-bearing or it isn't | Cross-domain solutions have a *minimal core*, and finding it is an elimination process |
| **Architect** | Gap spaces generate new concepts | Neither domain's vocabulary is adequate; the answer is a third language |
| **Amoeba** | If you can't rename it, it's structural | Strip away names entirely; if the claim survives, it's deep |
| **Sensor** | Mappings drift over time | Today's clean translation is tomorrow's invisible contamination |
| **Hybridizer** | Convergent evidence strengthens — or shatters — mappings | Multiple sources agreeing is not automatically better than one |

These eight strategies **partition the space of possible failures** in cross-domain work. No single organism catches everything. Together, they form a comprehensive audit suite.

### 2. The Regressor Is the Most Operationally Groundbreaking

The Regressor's elimination protocol — remove one source-domain element at a time, classify as load-bearing / decorative / invisible — is the closest thing in the document to a **formal algorithm**. It directly addresses the MSM's weakest point.

Recall the MSM's cross-domain translation protocol (v2, Section 8): it maps source primitives to target primitives and audits assumptions. But it cannot answer: *which of these mapped elements is actually doing the work?* The Regressor provides exactly this answer through a subtractive process.

Applied to the MSM pipeline:

```
MSM Phase 1: Identify mechanism M from source domain
MSM Phase 2: Translate M to target domain (primitive-by-primitive mapping)
MSM Phase 3: Apply Regressor to translated M
             → Classify each mapped primitive as LOAD-BEARING | DECORATIVE | INVISIBLE
             → Report minimum viable core of the translation
             → Flag INVISIBLE elements for Sensor monitoring
```

This transforms the MSM from "here is your translated mechanism" to "here is your translated mechanism *and here is exactly which parts you actually need*."

### 3. The Amoeba's Placeholder Test Is Elegant

The Amoeba's mutation strategy — replace all source and target terminology with neutral placeholders, then test if the structural claim still holds — is a **clean operationalization of the distinction between structural identity and verbal coincidence**.

If a mapping from ecology to economics survives placeholder substitution and also holds when restated in musical terms, cooking terms, or geological terms, it's almost certainly capturing something real about the underlying structure. If it only works in the original two domains, the mapping may be terminological artifact.

This is also a direct test of the MSM's primitive decomposition: if the mechanism's primitives are genuinely type-compatible (as the MSM's translation protocol requires), they should survive Amoeba mutation. If they don't survive, the type mapping was spurious.

### 4. The Factor Design Space Parameterizes the Translation Problem

The eight probe factors — Lexical Proximity, Structural Isomorphism, Observability Asymmetry, Temporal Alignment, Agentivity, Intervention Accessibility, Abstraction Level, Prior Sedimentation — collectively define an **eight-dimensional feature space** for any cross-domain translation problem.

This matters because the MSM currently scores mechanisms against holes using a fixed formula (structural similarity + feasibility + failure avoidance + interaction safety). The probe factors suggest that the *weights* in that formula should vary by domain characteristics:

- **High lexical proximity** (e.g., circuit theory ↔ network theory) → weight failure overlap *higher* (contamination risk is elevated)
- **Low structural isomorphism** (e.g., music ↔ immunology) → weight structural similarity *higher* (only genuinely deep mappings will score well)
- **High temporal misalignment** (e.g., evolution ↔ circuits) → weight constraint feasibility differently (Temporal constraint is the binding constraint)
- **Entrenched analogy** (e.g., brain-as-computer) → include the Parasite and Sensor as mandatory validation steps

The factor space is a missing piece for the MSM's calibration protocol.

---

## Where the Document Connects to Earlier Systems

### Connection to the MSM

The MSM's translation pipeline has a gap: it produces translations and validates them against *known* failure modes, but it has no mechanism for discovering *unknown* failure modes. The probe organisms fill this gap:

```
Current MSM Pipeline:
  Hole → Match → Translate → Regress Check → Output

Proposed Enhancement:
  Hole → Match → Translate → Regress Check → [PROBE VALIDATION LAYER] → Output
                                           │
                                    ┌──────┼──────┐
                                    ▼      ▼      ▼
                                  Parasite Regressor Sensor
                                   (+ hybrid combinations)
```

The Regressors, Parasites, and Sensors from this document would become **post-translation validation modules** that run after the MSM's standard regression check. They add the capacity to detect contamination, load-bearing element classification, and temporal drift — failure modes the MSM's current pipeline cannot catch.

### Connection to the MDC

The MDC provides a computational substrate for formalizing the probe organisms. Specifically:

- **The Arrangement Engine** can formalize the Parasite's contamination detection: an arrangement's boundary cells define the *boundary between legitimate and illegitimate regions* in signature space. Contamination = crossing a boundary without detection.

- **The SRC Bridge's self-reference distance** ($d_{sr} = \|\Sigma - F(\Sigma)\|$) provides a quantitative measure for the Sensor's contamination scoring. If the self-reference distance increases over iterations of elaboration, the mapping is drifting.

- **Homology computation** (Betti numbers) can formalize the Symbiont's minimal shared vocabulary: the Betti numbers of the *intersection* of two domains' topological structures represent the shared topological features that survive the pidgin-language construction.

### Connection to the Conditions-Holding Principle

The conditions-holding gate from MSM v2 asks: *should we intervene, or hold the conditions open for organic resolution?* The probe organisms add a refinement: **even when we decide to intervene (translate a mechanism), we should hold conditions open for multiple validation strategies to run.** The decision to intervene is necessary but not sufficient; the *quality* of intervention depends on how many probe organisms survive scrutiny.

---

## What the Document Doesn't Do (But Should)

### 1. No Formal Contamination Calculus

The Parasite and Sensor reference "contamination scores" (0.0–1.0) but don't define how to compute them. This is the most significant operational gap. A contamination calculus would require:

$$\text{Contamination}(M_{\text{translated}}) = \frac{\text{Source-derived assumptions in } M_{\text{translated}}}{\text{Total assumptions in } M_{\text{translated}}}$$

But "source-derived assumptions" needs a formal definition — perhaps operationalized via the Amoeba test: *what fraction of the mapping's structural claims survive placeholder substitution?*

$$\text{Contamination} = 1 - \frac{|\text{Claims surviving Amoeba mutation}|}{|\text{Total claims}|}$$

### 2. No Organism Selection Algorithm

The factor design space characterizes translation problems along eight dimensions, but there is no formal mapping from factor profiles to organism selection. A decision function is needed:

$$\text{OrganismSet} = f(\text{LexicalProximity}, \text{StructuralIso}, \text{ObservabilityAsym}, \ldots)$$

The "Recommended Combinations" table provides heuristics, but a proper algorithm would compute the expected information gain of each organism type given the factor profile.

### 3. No Conflict Resolution Protocol

What happens when organisms disagree? If the Parasite detects contamination the Mimic does not, which prevails? A voting protocol or weighted arbitration mechanism is needed — perhaps weighted by the factor profile of the specific translation problem.

### 4. No Temporal Formalization for the Sensor

The Sensor conceptually describes contamination drift, but provides no model of drift dynamics. Is contamination linear? Exponential? Does it accelerate with use (network effects)? A formal drift model — perhaps borrowed from the MSM's own ℐ-register accumulation — would make Sensor output actionable rather than observational.

---

## Architectural Assessment

### Completeness

| Concern | Covered? | By Which Organism(s)? |
|---|---|---|
| Surface plausibility of translation | ✓ | Parasite, Mimic |
| Structural fidelity of translation | ✓ | Amoeba, Mimic, Regressor |
| Minimal shared vocabulary | ✓ | Symbiont |
| Constructive bridge-building | ✓ | Architect |
| Load-bearing element identification | ✓ | Regressor |
| Contamination drift over time | ✓ | Sensor |
| Multi-source convergence | ✓ | Hybridizer |
| Temporal alignment checking | ✗ (mentioned, not formalized) | — |
| Computational substrate integration | ✗ | — |

### Generative Potential

The taxonomy doesn't just evaluate — it **generates new knowledge**. The Parasite deliberately builds contaminated solutions to find boundaries. The Architect proposes third vocabularies. The Hybridizer tests convergent evidence. Each organism is a *knowledge generation strategy*, not just a quality check.

This is consistent with the conversation's deepest theme: the system that generates the result is never the same as the result itself. The probe organisms generate knowledge *about* cross-domain mappings that no single mapping-by-mapping evaluation could produce.

---

## The Completeness Diagram

```
MSM PIPELINE (Translation Layer)
│
├──► PRE-TRANSLATION: Conditions-Holding Gate (should we translate at all?)
│
├──► MATCHING: Mechanism Search + MatchScore (best candidate mechanism)
│
├──► TRANSLATION: Cross-Domain Protocol + Back-Translation Validation
│
├──► POST-TRANSLATION: Probe Organism Validation Layer (THIS DOCUMENT)
│    │
│    ├── Parasite  → Contamination boundary detection
│    ├── Symbiont  → Minimal shared vocabulary verification
│    ├── Mimic     → Structural isomorphism confirmation
│    ├── Regressor → Load-bearing element decomposition
│    ├── Architect → Third-vocabulary generation (gap-filling)
│    ├── Amoeba    → Structural-vs-verbal identity test
│    ├── Sensor    → Temporal drift monitoring
│    └── Hybridizer → Multi-source convergence/divergence analysis
│
├──► DEPLOYMENT: Mechanism integrated into target system
│
└──► FEEDBACK: Bootstrap loop (MSM v2 Section 9)
     └── Probe outcomes feed back into MatchScore calibration
         and mechanism library entry criteria
```

---

## Summary

The Probe Organism Taxonomy completes the cross-domain translation pipeline that the MSM initiated. Where the MSM asks *"What mechanism fits this hole?"* and the translation protocol asks *"Can we express it in the target domain?"*, the probe organisms ask the harder question: **"What are we actually claiming, and how much of it survives scrutiny?"**

The eight organisms are not merely analytical tools — they are **epistemological positions** about the nature of cross-domain transfer. Each one makes a different bet about what counts as knowledge, what counts as contamination, and what counts as novelty. The document's greatest strength is making these bets **explicit and testable** rather than allowing them to remain hidden assumptions in the translation process.

The critical next step — consistent with everything in this conversation — is formalization: converting the prompt templates into algorithmic procedures, defining the contamination calculus, and building the organism selection function. Without that, the taxonomy remains a brilliant conceptual framework. With it, the taxonomy becomes the validation layer that makes the MSM's translations trustworthy.

Whether the Architect succeeds — whether a genuine third vocabulary can be built between any two domains — remains the deepest open question. If it does, the entire pipeline generates something no single domain could produce alone: a shared structural language that belongs to neither source nor target, but to the gap between them.
