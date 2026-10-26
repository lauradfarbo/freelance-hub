# Freelance-Hub

> [!WARNING]
> **This is not legal advice.** This repo and the Claude skill in it give you a baseline: a structured way to understand what is common, what may be possible, and what to ask for in your particular situation. Laws on contractor status, payment terms, termination, copyright and tax differ by country and change over time, and an AI can get them wrong or miss details that matter for your contract.
>
> **Before you sign, negotiate on the strength of it, or act on anything it tells you, have a qualified lawyer in your country confirm it.** This matters most for high-value contracts, foreign governing law, IP assignments, non-competes, and clauses that make you liable for the client's tax or employment obligations.

A Claude skill that helps freelancers and independent contractors review client contracts, spot the risky clauses, and negotiate better terms in any country.

## About

Freelance contracts are usually written by the client's side. They often leave out the things that protect you: payment if the client cancels, a fair notice period, a cap on your liability, the right to show your work in your portfolio. This repo packages a contract-review method that was built and used in real negotiations, so you can get the same structured second opinion on your own contracts.

**Who it's for:** self-employed freelancers, consultants and contractors who sign statements of work, consulting agreements or retainers with clients, and want a practical review before signing.

**What it is:** a *skill*, which is a folder of instructions that Claude loads when you ask for contract help. It is not an app and nothing runs on your computer. You upload it to your own Claude account once, and from then on Claude follows this method whenever you share a contract.

**What makes it work across countries:** the commercial logic of a good freelance contract is similar everywhere, but the law behind it is not. So the skill first asks where you and your client are based, researches the local rules (contractor classification, late-payment interest, termination, copyright, tax), and only then reviews your contract against them. A worked Netherlands example is included, so you can see what a finished review looks like.

**What it is not:** legal advice. It is a well-informed first pass that helps you ask for the right changes. For high-value or unusual contracts, have a local lawyer read it before you sign.

## What to do with it

1. **Install the skill in Claude.** Zip the `skills/freelance-contract-review` folder (the folder itself must sit at the top level of the zip). In Claude, open Settings, then Capabilities (or Skills), and upload the zip. If your plan doesn't support skills, create a Claude Project and paste `SKILL.md` and the files in `references/` into its instructions.
2. **Start a chat and share your contract.** Paste the text or attach the PDF or Word file, and say where you and the client are based.
3. **Read the review.** Claude will check local rules first, then send back a scorecard, the critical issues, replacement wording and a ranked list of what to ask for.
4. **Negotiate.** Ask Claude to draft the pushback email or a summary of redlines. The skill defaults to short, friendly wording that makes your requests sound like your standard way of working.

### Example prompts

- "I'm a freelance designer in Canada. This SOW is from a client in the US. Please review it before I sign."
- "My client wants a 7-day notice period and no kill fee. What should I push for, and what can I trade?"
- "Here's the client's latest version and my agreed redlines. Did they change anything we didn't discuss?"
- "Draft a friendly email asking for a portfolio carve-out and a 30-day payment term."

## What you get back

- A short summary of the local rules that matter for your contract, with sources
- A scorecard rating every checklist item as strong, weak or missing, with a risk level
- The critical issues first, explained plainly
- Ready-to-paste replacement wording for weak or missing clauses
- A negotiation plan: what to settle before signing, what to trade, and what to defer to renewal
- A flag when a local lawyer should look at the contract

## What's in this repo

```
skills/freelance-contract-review/
├── SKILL.md                         the workflow and response format
└── references/
    ├── clause-checklist.md          what to look for in every clause
    ├── jurisdiction-research.md     how to research the local law
    ├── negotiation-lessons.md       how to ask, trade and check
    └── example-netherlands.md       a worked jurisdiction example
```

## Make it yours

- Add `references/example-<your-country>.md` once you have verified the local rules, and mention it in `SKILL.md` under Step 1.
- Add the clauses you win and the lessons you learn to `references/negotiation-lessons.md`.
- Adjust the ranges in `clause-checklist.md` (kill fee, notice periods, payment terms) to your industry.

## Keep it safe to share

Don't commit real contracts, client names, rates or contact details to this repo. Keep the lessons general so the repo can be shared freely.
