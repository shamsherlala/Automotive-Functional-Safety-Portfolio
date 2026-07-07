# 05 — Safety Case Summary
**Document ID:** AEB-SC-005
**Version:** 1.0
**Date:** 07.07.2026
**Author:** Shamsher Lala
**Status:** Draft

---

## 1. Scope and Purpose
This document presents the safety case for the AEB system, demonstrating that 
all identified hazards have been analysed, safety goals defined, and safety 
mechanisms established in accordance with ISO 26262.

---

## 2. System Overview
AEB comprises a dedicated ECU working together with LiDAR, cameras, ultrasonic 
sensors, and radar to detect objects or pedestrians and alert the driver via 
acoustic and visual signals to prevent potential collisions. If no driver response 
is received within the FTTI, the system automatically applies emergency braking.

AEB does not control vehicle acceleration, engine management, battery management, 
airbag deployment, or steering systems such as Lane Keeping Assist.

---

## 3. HARA Summary
Three hazardous events were identified. All resulted in S3 severity due to 
potential fatality risk. ASIL ratings ranged from A to B based on exposure 
and controllability parameters.

| ID | Hazardous Event | S | E | C | ASIL |
|---|---|---|---|---|---|
| HE1 | AEB fails in muddy conditions | S3 | E2 | C3 | B |
| HE2 | AEB false positive on highway | S3 | E2 | C3 | B |
| HE3 | AEB fails in urban driving | S3 | E3 | C1 | A |

---

## 4. Safety Goals

| ID | Safety Goal | Linked Events | ASIL |
|---|---|---|---|
| SG1 | The AEB system shall not apply emergency braking unless sensor input is valid and a collision threat is confirmed | HE1, HE2 | B |
| SG2 | The AEB system shall warn the driver when a pedestrian is detected and apply emergency braking if the driver does not respond within FTTI | HE3 | A |

---

## 5. Functional Safety Concept

| ID | Linked Events | Functional Safety Mechanism |
|---|---|---|
| FSM1 | HE1, HE2 | Upon detection of invalid or obstructed sensor input, the AEB system shall enter a safe state, deactivate emergency braking, and alert the driver via acoustic and visual signals |
| FSM2 | HE3 | Upon detection of a collision threat, the AEB system shall alert the driver via acoustic and visual signals. If no driver response is received within FTTI, emergency braking shall be applied automatically |

---

## 6. Sign Off

| Role | Name | Signature | Date |
|---|---|---|---|
| Author | Shamsher Lala | | 07.07.2026 |
| Functional Safety Manager | TBD | | |
| Project Manager | TBD | | |
| Independent Safety Assessor | TBD | | |
| Supplier Representative | TBD | | |
| OEM Representative | TBD | | |