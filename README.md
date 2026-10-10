# SalesAgent-AI
# Home Credit LAP Qualification: AI Voice Agent

Assignment submission for **SalesAgents AI: AI Intern (Prompt Engineer)**.

## Use case
An outbound AI voice agent for Home Credit that contacts existing customers about a pre-approved **Loan Against Property (up to 75 lakh)**, collects 7 eligibility data points, disqualifies ineligible customers, routes existing-loan cases to a transfer specialist, and hands qualified leads to a senior loan expert.

## Platform used
- Voice platform: **<Retell AI / Bolna>**  <- edit this
- Voice: **<voice name>**
- Language: **<English / Hindi>**
- Agent name / gender: **<name> / <gender>**

## Repository contents
| File | Description |
|------|-------------|
| `system_prompt.md` | Complete system prompt text |
| `approach.md` | How I designed and tested the solution |
| `test_scenarios.md` | All test scenarios with expected vs actual results |
| `call_logs/` | Transcripts for each test call |

## Call recordings (public links)
| # | Scenario | Audio link | Transcript |
|---|----------|-----------|-----------|
| 1 | Perfect eligible customer | <link> | `call_logs/call_01_eligible.txt` |
| 2 | Agricultural property | <link> | `call_logs/call_02_agricultural.txt` |
| 3 | Cash income | <link> | `call_logs/call_03_cash_income.txt` |
| 4 | Loan above 75 lakh | <link> | `call_logs/call_04_above_75L.txt` |
| 5 | Existing loan / EMI reduction | <link> | `call_logs/call_05_transfer.txt` |
| 6 | Busy customer | <link> | `call_logs/call_06_busy.txt` |
| 7 | Out-of-order answers | <link> | `call_logs/call_07_out_of_order.txt` |
| 8 | Tenure too short / too long | <link> | `call_logs/call_08_tenure.txt` |

## Key design decisions
- Internal **qualification state** tracked every turn so answered questions are never repeated.
- Sequential questioning, but out-of-order answers are captured and skipped later.
- **Handoff gate**: final handoff only after all 7 data points are answered and criteria met.
- Immediate polite disqualification and call end on any failed criterion.
- No invented interest rates or market-value thresholds.

## How to reproduce
1. Create an agent on the voice platform.
2. Paste `system_prompt.md` into the agent instructions.
3. Set the variables (company_name, customer_name, agent_name, agent_gender, language_to_speak, etc.).
4. Make test calls using the scenarios in `test_scenarios.md`.
