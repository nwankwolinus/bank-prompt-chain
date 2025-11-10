---

# ✅ README.md (Customized + Final Submission Version)

```
# Bank Customer Support Prompt Chain

**Author:** Linus Nwankwo  
**Course:** AI For Developer  
**Assignment:** Prompt Chain Development  

---

## Overview

This project implements a 5-stage prompt reasoning system designed to interpret and process customer banking queries. The chain transforms raw text into structured insights and generates a professional response using Together AI.

Each stage builds logically on the previous one, forming a complete reasoning flow from understanding the customer’s intent to generating an actionable and polite reply.

The project includes:
- A Google Document with full prompt descriptions and explanations
- A JavaScript script implementing the chain (`prompt-chain.js`)
- Step-by-step logic flow and sequential output

---

## Prompt Chain Stages

### 1. Intent Interpretation  
Extracts the customer's primary intent with a clear, one-sentence summary.

### 2. Category Mapping  
Suggests 1–3 possible categories (ranked) with short reasons.

### 3. Category Selection  
Chooses the most relevant category based on evidence.

### 4. Detail Extraction  
Pulls important structured details (amounts, dates, error messages, etc.).

### 5. Response Generation  
Generates a concise, professional, and friendly customer response.

---

## Supported Categories

- Account Opening  
- Billing Issue  
- Account Access  
- Transaction Inquiry  
- Card Services  
- Account Statement  
- Loan Inquiry  
- General Information  

---

## File Structure

```

.
├── prompt-chain.js        # Main script implementing the 5-stage chain
├── README.md              # Documentation (this file)
├── .env.example           # Environment variable example
└── (optional) test_cases/ # Additional tests

```

---

## Setup Instructions

### 1. Install dependencies

```

npm install axios dotenv

```

### 2. Set your Together AI key

Create a `.env` file:

```

TOGETHER_API_KEY=your_api_key_here

```

### 3. Run the script

```

node prompt-chain.js

````

---

## Function Specification

The main function is:

```js
async function runPromptChain(query)
````

**Input:**

* `query` — a customer’s free-text message

**Output:**
An array of 5 strings representing each stage’s result:

```
[
  intent,
  categories,
  selectedCategory,
  details,
  finalResponse
]
```

---

## Example Usage

```js
const output = await runPromptChain("I was charged $50 yesterday and I need help understanding it.");
console.log(output);
```

Expected output format:

```
[
  "The customer is reporting an unexpected charge.",
  "1. Billing Issue - ...",
  "Billing Issue: ...",
  "- Amount: $50\n- Time period: yesterday",
  "Thank you for reaching out! ..."
]
```

---

## Google Document Requirement

A companion Google Document has been created containing:

✅ All 5 prompts
✅ 3–6 sentence explanation per stage
✅ Neatly structured with code formatting
✅ Shared with “Anyone with link can comment”

---

## Notes

* `.env` should not be committed to GitHub
* Together AI model names can be replaced as needed
* Script is modular and can be expanded into a chatbot system later

---

## License

MIT License

```
