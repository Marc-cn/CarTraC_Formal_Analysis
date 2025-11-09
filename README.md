# CarTraC: Formal Verification of a Post-Crash Accountability Protocol

This repository contains the **ProVerif 2.05** model developed for the paper:

**CarTraC: A Post-Crash Accountability Framework to Mitigate Hit-and-Run Incidents**  

## Overview

CarTraC (Crash Traceability and Accountability) is a lightweight vehicular protocol designed to enable **secure post-crash evidence exchange** among vehicles and a Trusted Authority (TA) without relying on continuous network connectivity.

This repository provides the **formal verification model** of CarTraC implemented in **ProVerif**, which evaluates the protocol against a **Dolev–Yao attacker**.  
The model verifies three main security properties:

1. **Secrecy** — Confidentiality of crash data.  
2. **Reachability** — Guaranteed message delivery to the TA.  
3. **Non-repudiation of Origin** — Proof that a vehicle cannot deny signing its crash evidence.

## Files

| File | Description |
|------|--------------|
| `CarTraC.pv` | Main ProVerif model including events, cryptographic primitives, and queries. |
| `CarTraC_with_nonce.pv` | Main ProVerif model including events, cryptographic primitives, queries, and the nonce request to the TA. |
| `README.md` | This documentation file. |
| `results.log` *(optional)* | Example ProVerif output showing verified properties. |

---

## Requirements

- **ProVerif 2.05 or later**  
  Available at: [https://proverif.inria.fr](https://proverif.inria.fr)

---

## Running the Verification

Clone or download the repository and run:

```bash
proverif CarTraC.pv

or

proverif CarTraC_with_nonce.pv
