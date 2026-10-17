# Reviewer Guide — HICE Human Validation

**For independent reviewers · 2026-07-17**

The role is to 127 conflict event narratives to judge whether each describes a genuine
**Healthcare Interference Conflict Event (HICE)**. Work independently; do not consult
the detector's output or the other reviewer.

---

## What is a HICE?

A HICE is a conflict-related act that deliberately targets or affects healthcare.

For a record to be eligible, **all three** must be true:

| # | Condition                           | Question to ask                                                                                                          |
| - | ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| 1 | **Healthcare entity present** | Does the narrative mention a hospital, clinic, doctor, nurse, patient, ambulance, medical supplies, or health programme? |
| 2 | **Conflict-related act**      | Was there a violent, coercive, or obstructive act by a military, armed group, or conflict party?                         |
| 3 | **Narrative link**            | Does the narrative connect the act to the healthcare entity — not just place them near each other?                      |

If any condition fails → **NOT ELIGIBLE**.

---

## The 5 HICE Categories

If eligible, assign **exactly one** category using this priority order (first match wins):

| Priority | Category                          | What it means                                                                                                  | Example                                                |
| -------- | --------------------------------- | -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| 1        | **personnel_targeting**     | Health staff harmed as persons — killed, injured, arrested, abducted, threatened because of their health role | "Military arrested a CDM doctor"                       |
| 2        | **systemic_attack**         | Facility attacked while staff are present — damage with personnel exposure                                    | "Airstrike hit a hospital; patients and staff killed"  |
| 3        | **infrastructure_damage**   | Facility, supplies, or vehicles damaged without explicit staff harm                                            | "Clinic destroyed by shelling; no casualties reported" |
| 4        | **access_disruption**       | Access to care obstructed — forced closure, blockade, denial of movement                                      | "Military ordered the clinic closed, services denied"  |
| 5        | **humanitarian_disruption** | All other interference — coerced suspension of programmes, harm to patients, pressure on health system        | "MSF suspended programme after threats to staff"       |

---

## Common situations — eligible or not?

| Situation                                                  | Verdict                | Why                                         |
| ---------------------------------------------------------- | ---------------------- | ------------------------------------------- |
| Airstrike hits a clinic                                    | **ELIGIBLE**     | Target: healthcare facility                 |
| Artillery fired *from* a hospital at a village           | **NOT ELIGIBLE** | Hospital is a location marker, not a target |
| "Two doctors among 12 civilians killed" in a market attack | **NOT ELIGIBLE** | Health role mentioned only in casualty list |
| Clinic closed due to staff shortage                        | **NOT ELIGIBLE** | No conflict act — resource constraint      |
| Nurse arrested for treating resistance members             | **ELIGIBLE**     | Coercive act targeting health worker        |
| Ambulance stopped at checkpoint, patients delayed          | **ELIGIBLE**     | Obstructive: denial of movement             |
| Routine MSF programme report, no hostile act               | **NOT ELIGIBLE** | No conflict-related act                     |
| Medic pushed off building during raid                      | **ELIGIBLE**     | Violence against health responder           |

---

## How to fill the sheet

For each record in your CSV:

1. **Read the narrative** carefully
2. **Decide:** Is this a genuine HICE?
   - `Y` — Yes, eligible
   - `N` — No, not eligible
   - `AMBIG` — Genuinely uncertain (goes to adjudication)
3. **If Y:** assign the one category that fits (priority order above)
4. **In RATIONALE:** one short line explaining your choice, especially for AMBIG cases

---

## Key principle

> **Co-occurrence is not interference.**
> A hospital and a battle in the same narrative does not make a HICE.
> The narrative must show the act was directed at the healthcare entity (or the entity
> was harmed while performing its healthcare role).

---

*Full protocol with Mermaid flowchart and 15 edge-case rulings: `research/eligibility_definition.md`*

---

## AI-assisted preliminary review

If the full review feels too time-consuming, an AI assistant (e.g., ChatGPT, Claude) can
provide preliminary Y/N/AMBIG assessments for all 127 records based on the rules above.
The professor then **verifies** each AI assessment rather than starting from scratch.

**Important:** AI assessments are **preliminary only** — every record must be
human-verified before the results are used. The AI may miss context, nuance, or
edge cases that a human reviewer would catch.
