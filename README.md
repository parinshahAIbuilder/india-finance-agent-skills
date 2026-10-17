# Finance & Accounts Agentic Skills: India Pack

Eight SKILL.md skills for Indian finance and accounts teams, built on the patterns that get installs on [agensi.io](https://www.agensi.io). Research date: 17 Oct 2026.

## Quick install

```bash
git clone https://github.com/parinshahAIbuilder/india-finance-agent-skills.git
```

Copy any skill folder into `~/.claude/skills/` (Claude Code / Cowork) or a project's `.claude/skills/`. For claude.ai, zip one skill folder and upload it under Settings → Capabilities → Skills. The skills also work with any agent that reads the SKILL.md standard.

All eight are also listed on Agensi: [GSTR-2B ITC Reconciler](https://agensi.io/skills/gstr-2b-itc-reconciler) · [TDS Compliance Auditor](https://agensi.io/skills/tds-compliance-auditor-india) · [MSME 43B(h) Payables Gate](https://agensi.io/skills/msme-43b-h-payables-gate) · [Bank Reconciliation (BRS)](https://agensi.io/skills/bank-reconciliation-brs) · [Trial Balance Close Gate](https://agensi.io/skills/trial-balance-close-gate) · [Budget vs Actual Commentary](https://agensi.io/skills/budget-vs-actual-commentary) · [Receivables Ageing & ECL](https://agensi.io/skills/receivables-ageing-ecl-ind-as-109) · [Journal Entry Red-Flag Scanner](https://agensi.io/skills/journal-entry-red-flag-scanner)

---

## 1. What the Agensi data shows

**Marketplace shape** (627 tags): the biggest categories are ai-agents (154), project-management (109), automation (99) and research (85). *Finance* has 52 skills, *accounting* 5, *reconciliation* 2 and *bookkeeping* 2.

**What gets installed in finance**

| Skill | Installs | Price |
|---|---|---|
| invoice extractor | 28 | Free |
| Software contract reviewer | 25 | Free |
| Financial Analysis Decision Engine | 18 | Free |
| Cash Flow Snapshot | 11 | Free |
| momsdeklaration-skatteverket (Swedish VAT return) | 9 | Free |
| Expense Categoriser Global | 8 | Free |
| Deferred Revenue Tie-Out Check | 4 | Free |

**What does not get installed**: about 30 paid reconciliation, invoice and bookkeeping skills ($5–$79), almost all with **0 installs**.

**India gap**: a search for GST / TDS / Tally / Ind AS / GSTR returns **one** skill (ITR filing, paid, 0 installs). No GST, TDS, MSME, Schedule III or Ind AS skill exists.

## 2. The pattern behind the trending skills

1. **"Best for" = verb + specific input → specific output.** For example: "Reconciles X and Y into matched records, exceptions and evidence." Generic "finance assistant" listings fail.
2. **Gate / verdict format.** The top skills end in a decision such as PASS / REVISE / HOLD or a release verdict, not just a report.
3. **Evidence-bound.** Every number traces to a source row or page, and there is a "cannot verify" list at the end. Trust is what sells.
4. **Severity-ranked findings** with an owner and an action.
5. **Free, single SKILL.md, minimal permissions** (read files, with optional Python for Excel). Free is the default for installs; paid skills sell only after a free version builds trust.
6. **Country-specific compliance wins** (the Swedish VAT skill has 9 installs) because generic models get the local rules wrong.
7. **Rich trigger-phrase descriptions**, so the agent loads the skill even when the user doesn't name a rule.
8. **A final self-check pass** (recompute, tie out, no double-bucketing) written into the skill.

Every skill in this pack follows all eight.

## 3. The skills

| # | Skill | Verdict | Core output |
|---|---|---|---|
| 1 | [gstr2b-itc-reconciler](gstr2b-itc-reconciler/SKILL.md) | CLAIM / CLAIM-WITH-HOLD / DO-NOT-FILE | Purchase register vs GSTR-2B/IMS, ITC at risk, Rule 37/37A, 16(4), 17(5), vendor emails |
| 2 | [tds-compliance-auditor](tds-compliance-auditor/SKILL.md) | CLEAN / FIX-BEFORE-RETURN / EXPOSURE | Section/threshold/rate test, 201(1A) interest, 40(a)(ia), 26Q tie-out; handles the 1961 → 2025 Act switch |
| 3 | [msme-43bh-payables-gate](msme-43bh-payables-gate/SKILL.md) | SAFE / PAY-BEFORE-31-MARCH / DISALLOWANCE | 45-day test, 43B(h) add-back, s.16 interest, s.22 note, Schedule III payables ageing, MSME Form 1 |
| 4 | [bank-reconciliation-brs](bank-reconciliation-brs/SKILL.md) | RECONCILED / WITH-ITEMS / DOES-NOT-CLOSE | Indian-format BRS, stale cheques, NACH/UPI items, suggested JEs |
| 5 | [trial-balance-close-gate](trial-balance-close-gate/SKILL.md) | PASS / REVISE / HOLD | 12 close checks, Schedule III mapping, draft BS/P&L, close checklist |
| 6 | [budget-vs-actual-commentary](budget-vs-actual-commentary/SKILL.md) | ON-TRACK / WATCH / ACTION-NEEDED | Branch-wise BvA, price/volume, re-forecast, management commentary |
| 7 | [receivables-ageing-ecl](receivables-ageing-ecl/SKILL.md) | ADEQUATE / TOP-UP / OVER-PROVIDED | Schedule III ageing, Ind AS 109 provision matrix, allowance movement, collections |
| 8 | [journal-entry-red-flag-scanner](journal-entry-red-flag-scanner/SKILL.md) | LOW / ELEVATED / HIGH | SA 240 JE testing, risk scores, Benford, defensible sample |

## 4. Agensi listing copy (paste-ready)

| Skill | Best for (≤ 20 words) | Tags | Suggested price |
|---|---|---|---|
| gstr2b-itc-reconciler | Reconciles purchase registers against GSTR-2B and IMS, returning safe ITC, at-risk credit and vendor follow-up emails. | finance, accounting, gst, india, reconciliation, tax | Free (lead magnet) |
| tds-compliance-auditor | Audits ledgers for TDS section, threshold and rate errors, returning interest, 40(a)(ia) exposure and corrections. | finance, tax, tds, india, compliance, audit | Free |
| msme-43bh-payables-gate | Tests payables against MSMED 45-day limits, returning 43B(h) disallowance, interest, Schedule III ageing and disclosures. | finance, accounting, msme, india, compliance, tax | Free |
| bank-reconciliation-brs | Reconciles bank books with statements into an Indian-format BRS, exceptions, stale cheques and suggested entries. | finance, accounting, reconciliation, bookkeeping, india | Free |
| trial-balance-close-gate | Checks a trial balance for close errors, maps it to Schedule III and returns a PASS/REVISE/HOLD verdict. | finance, accounting, month-end-close, audit, india | Free → $9 Pro version |
| budget-vs-actual-commentary | Turns budget and actuals into a branch-wise variance pack with re-forecast and evidence-backed management commentary. | finance, fp-and-a, reporting, business-operations | Free |
| receivables-ageing-ecl | Builds Schedule III receivables ageing and an Ind AS 109 ECL provision matrix with journal entry and disclosures. | finance, accounting, ind-as, audit, india | Free → $9 Pro version |
| journal-entry-red-flag-scanner | Scores every ledger entry against SA 240 red flags and returns a ranked, defensible audit sample. | finance, audit, fraud-risk, compliance, risk-management | Free |

**Each listing should include** (this mirrors the high-rated listings): a "What it does" list of 4–5 items, a 3-step "How it works", a usage example prompt, "Works with any SKILL.md agent; needs read files and Python for Excel", known limitations ("not tax advice; verify rates"), and a permissions note ("reads only attached files; no network").

**Launch strategy**: publish all eight free under one creator profile to build installs and ratings first. Then add a paid "India Close Pack" bundle with sample data, Excel templates and a multi-entity version.

## 5. How to use these skills

- **Claude Code / Cowork**: copy a skill folder into `~/.claude/skills/` (or a project's `.claude/skills/`).
- **claude.ai**: zip one skill folder and upload it under Settings → Capabilities → Skills.
- **Agensi**: submit through the creator dashboard, or ask me to submit with the Agensi connector.

*All skills are review aids, not legal or tax advice. Verify rates, thresholds and notifications for the period before relying on the output.*
