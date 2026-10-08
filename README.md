# Home Credit LAP AI Voice Agent

## Overview

This project implements an AI-powered voice agent for Home Credit using Retell AI. The agent contacts existing customers regarding a pre-approved Loan Against Property (LAP) offer of up to ₹75 lakh and performs a preliminary eligibility qualification.

The agent verifies the customer, collects the required eligibility information, handles disqualification conditions, detects existing-loan or EMI-reduction requests, and routes eligible customers to a senior loan expert for further assistance.

## Technology Used

- Retell AI
- GPT-5.6 Terra
- Voice AI
- Single Prompt Agent
- English (US)
- Voice: Maren

## Agent Configuration

| Field | Details |
|---|---|
| Agent Name | Keerthana |
| Company | Home Credit |
| Platform | Retell AI |
| Agent Type | Single Prompt |
| Model | GPT-5.6 Terra |
| Voice | Maren |
| Language | English (US) |
| Test Customer | Rahul Sharma |

## Key Features

- Customer identity verification
- Busy customer callback handling
- LAP offer presentation
- Seven-step eligibility qualification
- Out-of-order information handling
- Customer answer correction handling
- Immediate disqualification
- Existing loan and EMI-reduction detection
- Loan amount handling above ₹75 lakh
- Final handoff to a senior loan expert
- Natural conversational voice interaction
- No invented interest rates or eligibility requirements

## Eligibility Checklist

The agent collects and validates the following seven items:

1. **Property Type**
   - Residential, Commercial, and Industrial are eligible.
   - Agricultural property is not eligible.

2. **Ownership**
   - Sole ownership is eligible.
   - Joint ownership is eligible.

3. **Original Property Documents**
   - Original property documents must be available.

4. **Loan Amount**
   - Maximum offer amount: ₹75 lakh.
   - If the customer requests more than ₹75 lakh, the agent offers the maximum eligible amount of ₹75 lakh.

5. **Occupation and Income Mode**
   - Salaried and self-employed customers are eligible.
   - Income must be received through a bank.
   - Cash income is not eligible.

6. **Current Market Value**
   - The customer's estimated property market value is captured.
   - No minimum property-value threshold is assumed.

7. **Repayment Tenure**
   - Eligible tenure: 3 to 15 years inclusive.

## Transfer Logic

If the customer mentions:

- An existing loan on the property
- An existing property loan
- Balance transfer
- EMI reduction
- Transfer of an existing property loan

the fresh-loan qualification flow is stopped and the customer is directed to a loan-transfer specialist.

## Disqualification Logic

The agent immediately stops the qualification flow when any of the following conditions are confirmed:

- Agricultural property
- Original property documents unavailable
- Cash income
- Repayment tenure below 3 years
- Repayment tenure above 15 years
- Customer refuses the ₹75 lakh alternative after requesting more than ₹75 lakh

## Conversation Intelligence

The agent is designed to handle natural customer conversations rather than following a rigid questionnaire.

It can:

- Extract multiple details from a single response
- Handle information provided out of order
- Remember previously provided information
- Avoid asking questions that have already been answered
- Use the latest answer when a customer corrects an earlier response
- Handle interruptions and customer questions
- Ask only for the earliest unanswered checklist item

## Testing

The agent was tested against the following scenarios:

| Test Case | Scenario | Result |
|---|---|---|
| 1 | Happy Path / Eligible Customer | Passed |
| 2 | Agricultural Property | Passed |
| 3 | Cash Income | Passed |
| 4 | Original Documents Unavailable | Passed |
| 5 | Tenure Below Minimum | Passed |
| 6 | Tenure Above Maximum | Passed |
| 7 | Loan Amount Above ₹75 Lakh | Passed |
| 8 | Existing Loan / EMI Reduction | Passed |
| 9 | Out-of-Order Information | Passed |
| 10 | Customer Correction | Passed |

## Final Handoff

The agent only completes the final handoff after:

- Customer identity is verified
- All seven checklist items are answered
- All eligibility criteria are satisfied
- No transfer is required
- No disqualification condition exists

The customer is then informed that a senior loan expert will contact them for the next steps and exact interest-rate details.

## Project Documentation

The complete design, prompt, eligibility rules, test cases, results, and evidence are included in the project report.
## Retell AI Agent

You can interact with the deployed AI voice agent using the public Retell AI Voice Orb link:

[Talk to the Home Credit LAP AI Voice Agent](https://agent.retellai.com/orb/agent_2ade6e6e2c8ffe303dae843adc?token=5841918d2d5737f6e24150f4cc2c81f4)

> Note: The public link is provided for demonstration and evaluation purposes.

## Disclaimer

This agent performs preliminary qualification only. It does not make final loan approval decisions, promise loan approval, promise a specific interest rate, or promise loan disbursement.

## Author

**Keerthana Kanumuri**

B.Tech Computer Science and Engineering  

GitHub: https://github.com/keerthanakanumuri
