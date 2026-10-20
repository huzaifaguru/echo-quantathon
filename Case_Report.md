# ECHO — Case Report
**Entangled Minds: The Quantathon · Qubits Qrew, NED University**
Modules completed: 01, 03, 05 (mandatory) · 06 (stretch) · 02 (extra stretch). Notebook: `ECHO_Investigation_Notebook.ipynb`.

## 1. Final theory / verdict
ECHO never sent a message. Dr. Mahmud's twin detectors were correlated (possibly genuinely entangled), but entanglement cannot carry information on its own: each detector alone always sees 50/50 noise, and any usable message needs an ordinary classical channel. **She mistook an echo for a voice.**

On the human side, the "random" seed that triggered ECHO was strongly biased (≈70/30), which means someone chose the setting rather than leaving the run to chance. Whoever configured the seed and ARIA's schedule — someone with access to the machine and its records — made sure the experiment ran. I cannot name that person from the physics alone.

**Confidence:** high (≈90%) that ECHO could not signal faster than light; moderate (≈60%) that the run was deliberately triggered; low on *who* did it.

## 2. Key evidence (top three)
1. **No-signalling test (Module 03):** Bob's probability of reading 1 stayed ≈0.50 whatever Alice did (nothing / H / X / measure). Agreement exists, communication does not.
2. **Teleportation without classical bits (Module 06):** with the two classical bits the receiver is 100% correct; without them Bob reads ≈0.50 for *every* message angle. Nothing useful crossed without the classical channel.
3. **Biased seed (Module 02):** the recovered seed circuit `ry(1.159)` gives P(1) = 0.301 over 10,000 shots (theory 0.300). A fair coin would need π/2 ≈ 1.571. z ≈ −40, so this is not bad luck.

## 3. Evidence board
| FACT (measured / decoded) | CLAIM (stated by someone) | INFERENCE (my interpretation) | OPEN QUESTION |
|---|---|---|---|
| Message decodes to **ECHO** (Module 05) | ARIA: "No unauthorised command was issued." | The detectors were correlated, never communicating | Who configured ARIA and the seed angle? |
| Bell pair gives only 00/11, also in the X basis | Sana: "I only deleted a corrupted log." | The seed angle was chosen on purpose, not random | What did the deleted log and changed timestamps contain? |
| Bob stays 50/50 whatever Alice does | Bilal: "I warned her. Nobody listened." | Bilal's missing report likely described this flaw | What was in Bilal's missing report? |
| Seed circuit: P(1) = 0.30, not 0.50 | Vance: "ECHO was never real." | Vance was right about the physics, which does not make him the culprit | Where is Dr. Mahmud? |
| Teleport without bits: Bob ≈ 0.50 for all messages | Zara: "I proved them wrong… Or did I?" | Zara half-suspected the flaw herself | |

## 4. Experiments and results
| Module | Test (gates) | Prediction | Result |
|---|---|---|---|
| 01 Bronze | X; H | always 1; 50/50 | `{'1': 2000}`; `{'0': 1012, '1': 988}` |
| 01 Silver | H, H | always 0 (interference) | `{'0': 2000}` |
| 01 Gold | X on q0 and q2 | `101` | `{'101': 2000}` |
| 03 Bronze | H(0), CX(0,1) | only 00/11 | `{'00': 983, '11': 1017}` |
| 03 Silver | hidden coin q2 copied by CX | also only 00/11 | identical pattern |
| 03 Gold | H on both before measuring | Bell keeps 00/11; coin goes random | Bell 00/11 only; coin ≈25% each outcome |
| 03 Crux | Alice acts, Bob measures alone | Bob 50/50 always | 0.504, 0.504, 0.504, 0.508 |
| 03 Bonus | CHSH with ry angles | S > 2 | S = 2.819 |
| 05 | majority vote on 32 triples | readable word | **ECHO**, 20 of 32 triples corrected |
| 06 | teleport with / without corrections | 100% / ≈50% | 100% / 51% |
| 02 | seed `ry(1.159)`, 10,000 shots | fair would be 0.50 | P(1) = 0.301, bias 0.20 |

Circuit diagrams and histograms are in the notebook.

## 5. Interpretation
"Always agreeing" (Module 03 Bronze) cannot by itself prove a quantum link, because a pre-shared secret does the same (Silver). Measuring in a second basis separates the two (Gold), and the CHSH value of 2.82 > 2 shows the correlation is genuinely quantum. But even genuine entanglement does not let Alice influence Bob's statistics, and teleportation only works when two classical bits arrive. Zara's ECHO was a real correlation that she mistook for communication.

**What my experiments cannot prove:** who set the biased seed or configured ARIA, and what happened to Dr. Mahmud. Also, the Module 05 decoding is only correct if the promise "at most one flip per triple" is true — two flips in a triple would silently change a bit, and the data cannot show this.

## 6. Alternative explanation
Zara was not misled by anyone: she sincerely misread correlation as signalling, and the seed bias was an honest calibration mistake (wrong rotation angle). I prefer the "deliberate trigger" theory because 1.159 rad is far from π/2 (a 20-percentage-point bias, z ≈ −40), and it appears together with a deleted log, a missing warning report and an AI that "issued no unauthorised command", which only means somebody authorised it. Still, I cannot rule out the honest-mistake explanation.

## 7. Next experiment
Run the seed circuit through the original machine's configuration history: if the angle was ever set to π/2 and later changed to 1.159, that indicates deliberate tampering (and the change log names the account); if it was 1.159 from the first run, a calibration mistake becomes more likely. On the physics side, running the Module 03 test on real IBM hardware should still give Bob ≈50/50, plus small device noise.

## 8. Limitations
- Simulator only (AerSimulator, seed 42); real hardware adds noise.
- The H/X/CNOT test alone rules out a simple shared coin, not every classical model; the CHSH bonus (using ry) is needed for that.
- The evidence identifies a deliberate setting, not a specific person.

## 9. References and AI assistance
- ECHO Participant Manual and Code of Conduct (Qubits Qrew, NED).
- Qiskit Starter and Python warm-up notebooks provided by the organisers.
- Qiskit documentation (https://docs.quantum.ibm.com), IBM Quantum Learning.
- **AI assistance:** I used Claude (Anthropic) to explain concepts, structure the notebook, draft the case report and check my circuit predictions by simulation. I reviewed all of the code and results and can explain them.
