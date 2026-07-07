# 04 — Functional Safety Concept
**Document ID:** AEB-FSC-004
**Version:** 1.0
**Date:** 07.07.2026
**Author:** Shamsher Lala
**Status:** Draft

---

## Safety Mechanisms

| ID | Linked Events | Functional Safety Mechanism |
|---|---|---|
| FSM1 | HE1, HE2 | Upon detection of invalid or obstructed sensor input, the AEB system shall enter a safe state, deactivate emergency braking, and alert the driver via acoustic and visual signals |
| FSM2 | HE3 | Upon detection of a collision threat, the AEB system shall alert the driver via acoustic and visual signals. If no driver response is received within FTTI, emergency braking shall be applied automatically |