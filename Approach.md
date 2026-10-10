# Approach

## 1. Understanding the requirements
Read the assignment and converted it into: conversation stages (greeting, offer, checklist, handoff), 7 eligibility rules, and 4 business-logic switches (disqualification, transfer, amount limit, handoff gate).

## 2. Eligibility rules
| Item | Eligible | Not eligible |
|------|----------|--------------|
| Property type | Residential, Commercial, Industrial | Agricultural |
| Ownership | Sole, Joint | none |
| Documents | Originals available | Not available |
| Loan amount | Up to 75 lakh | Above 75 lakh (offer max 75 lakh) |
| Occupation + income | Salaried / Self-employed with Bank income | Cash income |
| Market value | Capture only | no threshold |
| Tenure | 3 to 15 years | Outside range |

## 3. Prompt structure
Identity, input variables, voice style rules, call flow, internal state, business rules, customer-question handling, never-do list, per-turn self-check, example dialogues.

## 4. Handling natural conversation
Short spoken replies, one question per turn, tolerance for fillers and long sentences, interruption handling, spoken number formatting, language and gender consistency.

## 5. Testing
Ran multiple calls: happy path, each disqualification, loan limit, transfer, busy customer, out-of-order information, diversions (interest rate question), and adversarial cases (contradictions, changing answers).

## 6. Iterations / fixes
Document what you changed after testing, for example:
- Issue: <what went wrong>  ->  Fix: <what you changed in the prompt>

## 7. Learnings
<2 to 3 lines>
