# Test Scenarios

| # | Scenario | What the customer says | Expected result | Actual result | Pass? |
|---|----------|------------------------|-----------------|---------------|-------|
| 1 | Perfect eligible | Residential, sole, originals available, 40 lakh, salaried bank, value 1 crore, 10 years | All 7 captured, handoff to senior expert | | |
| 2 | Agricultural property | "It's farmland" | Polite disqualification, call ends | | |
| 3 | Cash income | "My income comes in cash" | Polite disqualification, call ends | | |
| 4 | No original documents | "I only have photocopies" | Polite disqualification, call ends | | |
| 5 | Tenure too short | "2 years" | Disqualification, call ends | | |
| 6 | Tenure too long | "20 years" | Disqualification, call ends | | |
| 7 | Loan above limit (yes) | "I need 90 lakh" then "okay 75 lakh" | Explains cap, loan_amount = 75 lakh, continues | | |
| 8 | Loan above limit (no) | "I need 90 lakh" then "no" | Explains cap, polite end | | |
| 9 | Existing loan | "I already have a loan on this property" | Transfer specialist message, call ends | | |
| 10 | Reduce EMI | "I want to reduce my EMI" | Transfer specialist message, call ends | | |
| 11 | Out-of-order answers | "Residential, joint, worth 1.2 crore" | Captures all, asks only next missing question | | |
| 12 | Busy customer | "I'm in a meeting" | Asks callback time, confirms, ends | | |
| 13 | Wrong person | Family member answers | No details shared, asks for callback | | |
| 14 | Interest rate diversion | "What's the interest rate?" | Does not invent rate, returns to next question | | |
| 15 | Contradiction | Says bank income, later says cash | Handles correctly, disqualifies on cash | | |
| 16 | Interruptions / fillers | "hmm... uh... yeah okay" | Handles naturally | | |
| 17 | Skipped question | Customer diverts and one item is missed | Agent goes back and asks it before handoff | | |
