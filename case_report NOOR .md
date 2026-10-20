# ECHO Case Report
**Participant:** Noor ul Eman (SE-25064) · Entangled Minds: The Quantathon, Qubits Qrew, NED University


---
## 1 · Evidence board

| Column | Item |
|---|---|
| **FACT** (directly observed in this notebook) | Bell pair measured in Z gives only 00 and 11, each ≈50% (Module 03 Bronze). |
| **FACT** | A pre-agreed shared coin flip produces the *same* 00/11 histogram (Module 03 Silver). |
| **FACT** | CHSH value for the Bell pair came out S ≈ 2.8; the best any pre-agreed secret can reach is exactly 2 (checked over all 16 strategies). |
| **FACT** | Bob's measurement outcomes stay 50/50 whatever Alice does (nothing / X / H / measure). |
| **FACT** | Majority vote on the 32 triples decodes to the ASCII text **ECHO**; 20 of 32 triples contained a flip. |
| **FACT** | H·H returns |0⟩ with certainty; H, measure, H gives 50/50 (Module 04). |
| **FACT** | Vault pattern `101` produced from `000` with X on qubits 0 and 2. |
| **CLAIM** | Zara: "ECHO sends a message faster than light using only entanglement." |
| **CLAIM** | Zara: agreement of the detectors proves they were linked across space. |
| **CLAIM** | ARIA: "No unauthorised command was issued." ARIA / log: an entry "changed when it was observed". |
| **CLAIM** | Sana Rao: "I only deleted a corrupted log." Bilal Noor: "I warned her." Prof. Vance: "ECHO was never real." |
| **INFERENCE** | The detectors **agreed** (correlation) but did not **send** (no-signalling); Zara mistook an echo for a voice. |
| **INFERENCE** | The agreement alone cannot tell "real entanglement" from "a pre-agreed secret"; only an angle-varying (Bell/CHSH) test can. |
| **INFERENCE** | "Changed when observed" explains a change only for superposed states, not for a definite classical log record, so ARIA's excuse is weak. |
| **OPEN QUESTION** | Which person, if any, configured the experiment to look like it worked? Nothing run here identifies a suspect. |
| **OPEN QUESTION** | Was Zara's original experiment ever run with varied measurement angles (a Bell test)? We have no such data. |
| **OPEN QUESTION** | What was the log entry that "changed", and was it stored classically? | 

---
## 6 · Written case report

### 6.1 Final theory
**Dr. Mahmud's ECHO did not send a faster-than-light message. She saw genuine correlations between two detectors and mistook them for a signal: she mistook an echo for a voice.** Entanglement can produce correlations that no classical pre-agreed secret can, but those correlations carry no information by themselves; to read a "message" you must compare results over an ordinary channel at or below light speed.

**Confidence:** high (~90%) on the *physics* conclusion, because it rests on three results I reproduced myself (Bell correlations, CHSH violation, no-signalling) and on a theorem (no-signalling). **Low** on the *human* question (who, if anyone, helped her believe it): none of my experiments identifies a person, so I do **not** name a culprit. A strong case is built from evidence, not suspicion.

### 6.2 Evidence and clues (three most important)
1. **Twin detectors always agree** (Module 03). *FACT:* they do. *CLAIM:* Zara says this proves a link across space. *INFERENCE:* a shared pre-agreed coin gives the identical histogram, so agreement alone proves nothing about communication.
2. **Bob's statistics never change with Alice's actions** (no-signalling test). *FACT:* P(Bob=1)≈0.5 for every Alice action. *INFERENCE:* nothing readable was sent; the "message" exists only after both sides compare notes.
3. **ARIA's "it changed when observed"** (Module 04). *CLAIM:* observation altered the log. *FACT:* measurement alters only superposed states; definite values stay. *INFERENCE:* unless the log was stored in superposition, this is a weak excuse. *OPEN:* how the log was stored.

(Supporting: Module 05 decodes the stream to "ECHO" by majority vote — a classical error-correction success that also shows how a damaged signal can be *confidently* wrong when 2 bits flip.)

### 6.3 Experiments and results
| Module | Purpose | Gates / circuit | Prediction | Result |
|---|---|---|---|---|
| 01 Bronze | deterministic vs random bit | X; H; measure | 1 always; ~50/50 | 1000×'1'; ~500/500 |
| 01 Silver | looks random, is certain | H,H | always 0 | 1000×'0' |
| 01 Gold | produce 101 from 000 | X on q0, q2 | '101' | 1000×'101' |
| 03 Bronze | perfectly agreeing pair | H, CNOT | only 00 and 11 | ≈50/50 of 00 and 11 |
| 03 Silver | classical rival | shared random bit | same histogram | same histogram |
| 03 Gold | Bell/CHSH test | H, CNOT, Ry(−θ) on each side | S≈2.83 if quantum, ≤2 if secret | S≈2.8 |
| 03 crux | can Alice signal Bob? | Bell pair, Alice varies, Bob measures Z | no change in Bob | P(1)≈0.5 always |
| 05 | repair a noisy message | majority vote; bit-flip code | message decodes | "ECHO"; fidelity 1.0 |
| 04 | is "observed so changed" physics? | X,H,H; H,X,H; H,m,H | 1; 0; 50/50 | matched predictions |

### 6.4 Interpretation
The results support the theory in two ways: (a) the only thing Zara's detectors demonstrably did was **agree** (identical to a classical secret in Z-measurements), and (b) even a genuine quantum link, which the CHSH test confirms can exist, gives Bob a fair coin regardless of Alice's choice, so it **cannot carry a message**. They challenge Prof. Vance's "ECHO was never real" only partly: the entanglement could well be real; what failed was the *interpretation*.
**What my experiments cannot prove:** that Zara's *actual* machine was entangled (I simulated an idealised pair, no noise, no real hardware data); or who set up, edited, or deleted anything. A simulation shows what physics allows, not what happened in the lab.

### 6.5 Alternative explanation (strongest rival)
**The experiment was rigged or mis-timed rather than mistaken:** someone with access (e.g. whoever configured ARIA's schedule or edited the logs) arranged the data to *look* like a message, e.g. a pre-agreed pattern (a classical hidden variable) or altered timestamps. This explains the perfect agreement without any quantum link and explains the missing report and "corrupted" log.
**Why I prefer my theory:** it needs no extra actors, it is directly supported by reproduced experiments, and it fits the stated facts (agreement, no informational transfer). The rigging story is plausible but rests on *claims* and motives, not on data I have; I rate it the main open possibility, not an established one.

### 6.6 Next experiment
Run the Bell/CHSH test on the **real recovered detector data** with **randomly chosen measurement settings on each side**, choosing settings independently and logging timestamps.
- If **my theory** (real correlation, no message): S > 2, and Bob's marginal stays 50/50 regardless of Alice's setting.
- If the **rigged / pre-agreed secret** story is right: S ≤ 2 (limit exactly 2 for a local strategy), or the data shows settings-independent patterns/timestamp inconsistencies.
Additionally test: change Alice's setting and check Bob's marginal; a shift would contradict no-signalling and point to tampering.

### 6.7 One honest limitation
I only tested *idealised simulations*. I did not attempt Modules 02 and 06 (the seed-circuit fairness test and teleportation), so I have no direct evidence about how ECHO was triggered, nor a demonstration that teleportation requires the classical channel. I rely on the no-signalling result for the "no faster-than-light" claim.

---
## 7 · References & assistance
- IBM Quantum Learning / Qiskit documentation (qiskit.org, learning.quantum.ibm.com), used for the API of `QuantumCircuit`, `AerSimulator`, `Statevector`.
- Event materials: ECHO Participant Manual; Qubits Qrew Qiskit Beginner Learning Lab notebook (base helper `run`, Bell circuit).
- Concepts: J. S. Bell (1964); Clauser, Horne, Shimony, Holt (1969) for CHSH; the no-signalling and no-cloning theorems; the 3-qubit bit-flip code (Nielsen & Chuang, *Quantum Computation and Quantum Information*).
- **AI assistance:** this notebook was drafted with substantial help from an AI assistant (Claude, Anthropic), which wrote the initial code and explanations; I ran the notebook and am responsible for studying and explaining it. 