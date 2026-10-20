# ECHO — Quantathon Submission
**Syed Mohammad Huzaifa** · Entangled Minds: The Quantathon · Qubits Qrew, NED University

## The case
Dr. Zara Mahmud vanished from her lab, leaving her quantum machine looping one experiment, **ECHO**, which she believed sent a message faster than light using entanglement. The investigation unlocks six quantum modules and asks one question: **was ECHO a real breakthrough, or did she mistake an echo (correlation) for a voice (communication)?** Suspects: Prof. Imran Vance, Sana Rao, Bilal Noor and the lab AI, ARIA.

The full challenge is in the organisers' *ECHO — Participant Manual*.

## Verdict (short)
ECHO never sent a message: entangled detectors are correlated, but each side alone always sees 50/50, and teleportation fails without two classical bits. The "random" seed that triggered ECHO was biased (P(1) = 0.30), so the run was a chosen setting, not chance. Full reasoning: `Case_Report.md`.

## Files
| File | Contents |
|---|---|
| `ECHO_Investigation_Notebook.ipynb` | Solutions: Modules 01, 03, 05 (mandatory), 06 (stretch), 02 (extra) — prediction, code, results and "what it proves" for each |
| `Case_Report.md` | Case report: verdict, evidence board, experiments, interpretation, alternative theory, next experiment, limitations, references and AI use |

## How to run
Open the notebook in Google Colab (File → Open notebook → GitHub tab → paste this repo's URL) and choose **Runtime → Run all**. The first cell installs Qiskit and Qiskit Aer. Results are reproducible (`AerSimulator(seed_simulator=42)`).
