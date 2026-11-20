# Riverpe — Payment Supply Network Framework

**Status:** completed framework, v4. Supersedes v3 (20 November 2026) and v2 (August 2026).
**Prepared for:** Riverpe founding team, prospective banking partners and institutional investors.
**Author:** candidate for Head of Growth Operations / Partnerships / Market Expansion.
**Document date:** 20 November 2026. **All sources accessed 20 November 2026.**

---

## Executive Summary

Riverpe proposes to run a small number of payment corridors as a supply business: licensed counterparties, funded balances, settled obligations. Revenue comes from a take rate on cross-border payout. The binding constraint is float, not demand.

The provisional first corridor is **Côte d'Ivoire ← France** — euros collected in France, paid out to Ivorian wallets and bank accounts. It is not the largest opportunity assessed; Brazil scores higher on capability. It is the only corridor where a five-figure float funds a live operation, because the XOF is pegged to the euro at 655.957, SEPA settles same or next day, and the payout leg is domestic and instant.

Three things gate launch: a BCEAO-licensed payout partner, an approved intermediary bank for the cross-border leg (payment institutions may not originate payments abroad), and about $60,000 of committed float.

Unresolved: no partner has been approached, the 4.05% corridor benchmark and the 0.8% PI-SPI cap compress pricing, and no primary interview has been completed.

---

## How to read the evidence in this document

Every material claim carries one of these labels. They are not decoration; they tell a reader how much weight the number can bear.

| Label | Meaning | Treatment in decisions |
|---|---|---|
| **Verified** | Primary instrument or dataset read directly: regulator text, central-bank statistics, official register | Can be relied on; re-check the register before signing |
| **Secondary** | Reputable secondary reporting of a primary source not directly read | Directional; confirm before contractual commitment |
| **Estimate** | Author's calculation from labelled inputs, with the arithmetic shown | Reproducible; challenge the inputs, not the maths |
| **Assumption** | Planning figure with no current market quote | Replace with a quoted rate card before launch |
| **Pending validation** | Plausible, unconfirmed, specific to a partner or regulator conversation | Cannot be used in a customer promise or a deck claim |
| **Unknown** | Not established by this research | Listed in §13 with the test that would resolve it |

Two conventions matter for reading the rest:

- **Corridor notation is `payout ← funding`.** "Côte d'Ivoire ← France" means funded in France, paid out in Côte d'Ivoire. Float sits on the payout side, so the arrow points at the balance sheet that has to be funded.
- **Market score ≠ launch order.** The score in §3 measures whether a market can be operated. Launch order in §4 is decided by demonstrated access and by whether the available capital can fund the float. A market can score highly and still not be first.

---

## 1. Original Thesis and Business Model

### 1.1 The thesis, preserved from v1 and v2

Payment infrastructure is supply-constrained, not demand-constrained. Diaspora senders already want to move money; small importers already owe suppliers. What is scarce is a set of licensed, funded, reliable counterparties inside a specific corridor, plus the operational discipline to settle through them without failing.

The v2 formulation — "own the supply side, not the demand side" — is retained. So is the operating consequence: a corridor is a *stack of contracts and balances*, not a list of logos on a website. Three signed partners with funded accounts beat thirty integrations with no float.

What changes in v4 is how the thesis is measured. v2 counted corridors and partners. This version counts net contribution per unit of volume and days of float cover, because those are the numbers that decide whether the next corridor is affordable.

### 1.2 What Riverpe actually sells

| Layer | What Riverpe provides | Who pays | Revenue mechanism |
|---|---|---|---|
| **Corridor access** | A settlement path from a funding market to a payout market that a customer cannot build alone | Sender or sending business | Take rate on payout value |
| **FX execution** | Conversion at a published rate with the spread embedded | Sender, implicitly | Spread between reference and applied rate |
| **Payout reach** | Wallet, bank and cash-out coverage through licensed local partners | Sender, bundled | Included in the take rate |
| **Operational reliability** | Success rate, settlement timing, exception handling | Business customers, via premium pricing | Higher take rate, not a separate fee |

The fourth line is the strategy. Reliability is the only durable differentiator available to a company that does not own a licence, a bank or a wallet network, and it can only be sold at a premium if it is measured and published.

### 1.3 The business model in one page

```
Customer (France, EUR)
   |  EUR 206.00 for a EUR 200.00 payout
   v
Funding-side payment provider  -- collection, KYC at source
   |  EUR 205.30 net of collection fee
   v
Approved intermediary bank (RFE-mandated)  -- FX + cross-border settlement + reporting
   |  XOF credited to Riverpe's payout account
   v
Licensed payout provider (BCEAO authorisation)  -- bulk disbursement via PI-SPI
   |
   v
Beneficiary wallet or bank account (XOF)
```

Four counterparties, three of them regulated, one of them a bank by legal requirement rather than commercial preference. That structure is what the float in §5 has to fund and what the unit economics in §6 have to pay for.

### 1.4 What Riverpe is not

- **Not a wallet.** It does not hold customer funds as an e-money issuer in year one; that requires an establishment licence and XOF 300,000,000 of paid-up capital (§2.3).
- **Not an FX broker.** It buys conversion from an approved intermediary and resells at a margin.
- **Not a marketplace.** Integrations are not the product; funded settlement capacity is.
- **Not a remittance brand at launch.** The first customers are businesses and diaspora senders reached through partners, not a consumer app competing on advertising.

---

## 2. Market Selection and Regulatory Eligibility

Regulatory eligibility is decided **before** any commercial scoring. A market that fails this section is not scored, not ranked and not compared on volume. This replaces v2's approach, where "regulatory clarity" was 15% of a weighted score and could be outvoted by market size.

### 2.1 The five questions that must be answered in writing

For each market, by someone qualified to answer — a licensed partner's compliance officer, or counsel — not by inference from a website:

1. Which entity type may settle the **payout** leg, and can a licensed partner carry it, or is a Riverpe-owned authorisation required?
2. Does the partner's authorisation cover this specific use case — cross-border remittance, B2B supplier payout, crypto-originated funds — or only domestic collection?
3. **Who may legally originate the cross-border leg?** This is the question v3 got wrong and it is now first-order (§2.2).
4. What KYC is required, at which threshold, and who performs it — Riverpe, the funding-side provider, the payout partner, or all three?
5. What reporting, sanctions and PEP-screening obligations attach, and which are delegated by contract?

### 2.2 Côte d'Ivoire: the correction that changes the corridor design

Three instruments govern this market, and reading them changes the partner structure.

**(a) Payment institutions are a new, real regime — not a partner-only grey area.** BCEAO Instruction n°001-01-2024 of 23 January 2024 governs payment services in WAEMU and created the *établissement de paiement* (EP). Minimum capital is tiered by licensed activity: XOF 10,000,000 for account aggregation only, XOF 20,000,000 for payment initiation only, XOF 30,000,000 for both, and XOF 100,000,000 where the authorisation covers the wider service set including fund transfers [S1]. The union register listed 31 authorised EPs as at 28 February 2026, of which **9 are in Côte d'Ivoire**, all first authorised between May and September 2025 [S2]. A twelve-month-old regime with nine licensees is a market where a licensed payout partner can be found and verified — and where a direct licence is a real option later, at roughly XOF 100m (about $165,000 at 655.957) rather than the multi-million sums an e-money licence implies.

**(b) E-money issuance is a different, heavier licence.** An *établissement de monnaie électronique* requires XOF 300,000,000 fully subscribed and paid in cash before authorisation [S3]. This is why Riverpe should not plan to issue wallets in year one. It should pay out into wallets that someone else issues.

**(c) The decisive constraint: EPs and EMIs may not originate payments abroad.** Under Règlement n°06/2024/CM/UEMOA of 20 December 2024 and its implementing Instruction n°01/07/2025/RFE of 1 August 2025, transfers to and from outside UEMOA must be executed through an **approved intermediary** — a bank designated by the Finance Minister on BCEAO's advice, listed annually [S4, S5]. Article 26 is explicit: e-money institutions and payment institutions "ne sont pas habilités à émettre des paiements sur l'étranger" (are not authorised to make payments abroad); they may receive funds originating outside UEMOA, under the responsibility of an approved intermediary [S4].

**What this means operationally.** A France → Côte d'Ivoire corridor cannot be built from three PSPs alone. It needs:

| Leg | Entity required | Why |
|---|---|---|
| EUR collection in France | French payment institution, or Riverpe as its registered agent | PSD2 scope; SEPA reach |
| EUR→XOF conversion and cross-border settlement | **Approved intermediary bank in WAEMU** | RFE Regulation art. 26; EPs/EMIs may not originate external payments |
| XOF payout to wallets and accounts | BCEAO-authorised EP, or an EMI's distribution network | Domestic disbursement; PI-SPI connectivity |
| Reporting and documentation | Approved intermediary, with Riverpe supplying underlying documents | RFE declarations per transfer |

This makes the bank a **regulatory requirement in the settlement position**, not a commercial preference for cheap settlement. v3 described a "partner-only licence path" and put the bank in as the preferred primary partner on cost grounds. The conclusion survives; the reasoning was incomplete, and the float consequence is material (§5.3).

**(d) The domestic rail is now price-capped and interoperable.** BCEAO's PI-SPI platform launched on 30 September 2025; from 2 November 2026 interoperable e-money transfers in WAEMU must route through it, sending is free up to XOF 8,000 cumulative per user per participant per day, charges above that are capped at 0-0.8% before tax, and receiving is free [S6, S7]. Cross-border UEMOA transfers align to the same terms from 1 June 2027 [S6]. The platform reported 175 connected participants and reach to more than 38 million people at the time of the pricing revision [S7].

Two consequences, both material:

- **The payout leg is becoming a utility.** A 0.8% regulated ceiling on the domestic e-money transfer compresses what any intermediary can charge for "wallet payout" and moves the margin to the cross-border and FX legs.
- **A regional reference price is being set.** Intra-UEMOA transfers get cheaper from June 2027. France→Côte d'Ivoire is outside that scope, but customers will compare, and any price above the regional ceiling needs a visible reliability or FX justification.

**Eligibility verdict — Côte d'Ivoire: ELIGIBLE, with three conditions.** A BCEAO-authorised payout partner verified on the register; an approved intermediary bank contracted for the cross-border leg; RFE-compliant documentation per transfer. No Riverpe-owned licence is required to start; a direct EP authorisation at XOF 100m becomes viable once volume justifies it.

### 2.3 The other markets

**Brazil — ELIGIBLE, with FX-specific conditions.** Payment institution authorisation sits with BACEN. PIX runs on the SPI, a central-bank-operated real-time gross settlement system settling in central-bank money, 24 hours a day, seven days a week, irrevocably [S8]. Crucially, PIX is now the majority rail: 55.2% of all payment transactions in H1 2026, roughly 44 billion transactions out of 79.7 billion, with total value of R$71.9tn [S9]. The condition that decides design: cross-border FX must be executed through an institution authorised by BACEN to operate in the FX market; a payment institution authorisation does not by itself confer that right [S10, pending validation]. **Verdict: eligible; requires a bank or authorised FX counterparty, and a BACEN-licensed payout partner.**

**Botswana — ELIGIBLE, small.** A payment services licensing regime exists under the Bank of Botswana; a partner or direct route is available [S11, pending validation]. Convertible currency, functioning banking sector, very small addressable flow. **Verdict: eligible, not a launch candidate.**

**Malawi — ELIGIBLE, conditional on FX access.** Licensing exists under the Reserve Bank of Malawi, but the binding constraint is foreign-exchange availability rather than authorisation: kwacha liquidity and allocation can delay settlement independently of any partner's performance [S12, pending validation]. **Verdict: eligible with an FX-availability caveat that cannot be resolved from published sources.**

**Democratic Republic of the Congo — NOT ELIGIBLE for year one.** Population 112.8 million and GDP per capita $806.8 [S13] make it the most discussed market in v2, which ranked it third. But the licensing path is not establishable from published instruments, the CDF is not a currency in which to hold a float, and dual USD/CDF circulation adds a documentary layer without adding margin. **Verdict: gate failure. Not scored in §3.** This is the gate doing its job: a market can be large, interesting and ineligible at the same time.

### 2.4 Eligibility summary

| Market | Payout-leg authority | Cross-border leg | Riverpe licence needed to start | Verdict |
|---|---|---|---|---|
| Côte d'Ivoire | BCEAO EP (9 licensed) or EMI partner | Approved intermediary bank, mandatory | No | **Eligible, conditional** |
| Brazil | BACEN payment institution | BACEN-authorised FX institution | No | **Eligible, conditional** |
| Botswana | Bank of Botswana PSP licence | Commercial bank | No | Eligible, small |
| Malawi | Reserve Bank of Malawi PSP licence | Commercial bank; FX allocation risk | No | Eligible, FX-constrained |
| Congo (DRC) | Not establishable | Not establishable | Unknown | **Not eligible** |
---

## 3. Revised Market Scoring Methodology

### 3.1 Why eight criteria, and why these weights

v2 used seven weighted factors including "regulatory clarity" and produced unshowable scores (4.2, 3.8, 2.8). v4 keeps seven commercial and operational criteria, removes regulation entirely because it is now a gate (§2), and adds competitive intensity explicitly rather than as a footnote.

| # | Criterion | Weight | Why this weight |
|---|---|---|---|
| 1 | **PSP availability and accessibility** | 20% | The scarcest input. Without reachable licensed payers, nothing else converts into a corridor. Highest weight because it is the constraint that cannot be bought with capital |
| 2 | **Banking relationship stability** | 15% | Every leg touches a bank, and in WAEMU the cross-border leg *requires* one. A bank that will not onboard is a hard stop, so this is weighted like infrastructure |
| 3 | **Settlement infrastructure and reliability** | 15% | Determines failure rate, working capital and what can honestly be promised to a customer |
| 4 | **Liquidity availability** | 15% | Float is the binding constraint on a small balance sheet; it is also the cost that scales worst at low volume |
| 5 | **FX convertibility and volatility** | 10% | Lower weight than liquidity because exposure can be limited by days-of-float even where it cannot be hedged — but a pegged currency removes an entire risk category, so it cannot be ignored |
| 6 | **Commercial opportunity (priced, not sized)** | 15% | Scores the *price gap* a corridor can capture and whether flow is already paying for a worse service. Deliberately not a market-size input |
| 7 | **Operational complexity** | 5% | A cost, not a strategy. Low weight because complexity is manageable with process, but it sets time-to-launch |
| 8 | **Competitive intensity** | 5% | Real but poorly measurable. Low weight because it cannot be quantified defensibly at this stage, and a low weight is more honest than a confident score |

**Total 100%.** Weights were set by asking which input, if it failed, would stop the corridor outright. Availability, banking, settlement and liquidity each fail the corridor on their own; that is why the first four carry 65% between them. Commercial opportunity carries weight because a reliable corridor with no price gap is a charity. Complexity and competition are costs of doing business, not gates.

**Deliberate exclusions.** Raw payment volume and population are not inputs — that is what produced v2's size-led ranking. "Regulatory clarity" is not an input, because §2 decides it. Partner *count* is not an input; partner *access* is.

### 3.2 Scoring rules

- Each criterion scores **0-5**. 5 is best. For operational complexity, 5 means *simplest*.
- Anchors: **0** = disqualifying or absent; **1** = exists but unusable at this capital level; **3** = workable with effort; **5** = best available practice in the set.
- Weighted contribution = (score ÷ 5) × weight, so a perfect market scores 100.
- Every score carries an evidence tag and a stated gap. A score without an adjacent source or test is a judgement and is labelled as one.
- Scores are re-scored after the access sprint in §4. A score is not a finding until a partner has quoted.

### 3.3 Côte d'Ivoire — 73.0 / 100

| Criterion | Wt | Score | Contribution | Evidence and reasoning | Status |
|---|---|---|---|---|---|
| PSP availability | 20 | 4 | 16.0 | Nine BCEAO-authorised EPs, plus three mobile-money issuers and their distribution networks [S2]; PI-SPI gives a common domestic rail [S6] | Verified register; **partner access not tested** |
| Banking stability | 15 | 4 | 12.0 | Approved intermediaries are designated and published annually [S5]; regional banking sector is supervised and correspondent links to the euro area exist via the French Treasury operating account [S14]. Deduction: onboarding scrutiny of a non-resident fintech is slow and discretionary | Verified framework; **specific bank appetite unknown** |
| Settlement infrastructure | 15 | 4 | 12.0 | Domestic instant settlement via PI-SPI at par; RTGS available for bank legs; payout to wallets is instant. Deduction: holiday calendar and cut-offs still bind the bank leg [S6] | Verified |
| Liquidity availability | 15 | 3 | 9.0 | XOF is obtainable through an approved intermediary, but there is no deep non-bank market in XOF and no way to borrow it locally at short notice. Liquidity must be bought forward, not sourced on demand | Assumption pending validation |
| FX convertibility and volatility | 10 | 5 | 10.0 | XOF pegged to EUR at 655.957, fixed, no band; convertibility through the French Treasury account [S14] | Verified |
| Commercial opportunity | 15 | 3 | 9.0 | Corridor average cost 4.05% for EUR 140/345 tickets in Q3 2025, against a digital-only SSA benchmark of 3.54% [S15, S16]: a real gap, but not a wide one. Flow is modest: $1.77bn received nationally in 2024 [S17] | Verified data; **price gap narrow** |
| Operational complexity | 5 | 3 | 3.0 | Four counterparties, RFE documentation per transfer, French-language ops, calendar mismatch between EUR and XOF legs | Estimate |
| Competitive intensity | 5 | 2 | 2.0 | Incumbents, banks, three wallet networks and nine licensed EPs already serve this corridor; domestic transfers are free below XOF 8,000 and capped at 0.8% above [S6] | Verified pricing; **share data unavailable** |
| **Total** | **100** | | **73.0** | | |

**Major risks.** Crowded, price-capped domestic rail; mandatory bank in the settlement position adds onboarding time; RFE documentation creates a per-transfer operational load that a lean team may underestimate.

**Outstanding gaps.** No approved intermediary has been approached; no payout partner has quoted; the share of the corridor's 4.05% average that is fee versus FX margin is known from the benchmark but not the split a specific partner would offer.

### 3.4 Brazil — 80.0 / 100

| Criterion | Wt | Score | Contribution | Evidence and reasoning | Status |
|---|---|---|---|---|---|
| PSP availability | 20 | 4 | 16.0 | Deep market of licensed payment institutions and acquirers; PIX participation is broad. Deduction: many are large, well-capitalised and uninterested in a startup's volume | Secondary; **access not tested** |
| Banking stability | 15 | 4 | 12.0 | Deep, well-regulated banking system with functioning FX market. Deduction: onboarding a non-resident with no Brazilian licence is slow | Secondary |
| Settlement infrastructure | 15 | 5 | 15.0 | SPI settles in central-bank money, 24/7, irrevocably, with no overdrafts permitted [S8]; PIX is 55.2% of transactions [S9] | Verified |
| Liquidity availability | 15 | 5 | 15.0 | Onshore and offshore BRL liquidity; FX can be sourced and hedged | Verified market structure |
| FX convertibility and volatility | 10 | 3 | 6.0 | Floating BRL, hedgeable but not free; hedge cost and margin consume part of the take rate | Estimate |
| Commercial opportunity | 15 | 4 | 12.0 | Very large flow and a competitive but deep price pool; PIX has already compressed domestic pricing, which caps what a payout-only product can charge | Verified volume; **corridor pricing not researched** |
| Operational complexity | 5 | 2 | 2.0 | Portuguese-language compliance, BACEN authorisation for FX, PIX participation rules, tax withholding complexity | Estimate |
| Competitive intensity | 5 | 2 | 2.0 | Intense: incumbent remittance brands, fintechs and banks | Judgement |
| **Total** | **100** | | **80.0** | | |

**Major risks.** Capital intensity of the float (§5.3); FX execution requires an authorised counterparty; regulatory surface is broader than WAEMU's.

**Outstanding gaps.** No Brazilian corridor pricing study; no FX counterparty identified; the commercial opportunity score is the least evidenced in the set.

### 3.5 Botswana — 57.0 / 100

| Criterion | Wt | Score | Contribution | Evidence and reasoning | Status |
|---|---|---|---|---|---|
| PSP availability | 20 | 3 | 12.0 | Licensed PSPs exist in a small market; few candidates, so the "three PSPs" test is structurally hard | Pending validation |
| Banking stability | 15 | 4 | 12.0 | Well-supervised, sound banking sector; convertible currency | Secondary |
| Settlement infrastructure | 15 | 3 | 9.0 | Functioning RTGS and instant retail rails; smaller ecosystem, fewer integration options | Pending validation |
| Liquidity availability | 15 | 2 | 6.0 | Shallow local liquidity; float is easy to hold but hard to source at short notice | Estimate |
| FX convertibility and volatility | 10 | 4 | 8.0 | Crawling peg arrangement, orderly; hedge market thin | Secondary |
| Commercial opportunity | 15 | 1 | 3.0 | Very small addressable flow; no evident price gap worth building for | Judgement |
| Operational complexity | 5 | 4 | 4.0 | Single currency, single regulator, small partner set | Estimate |
| Competitive intensity | 5 | 3 | 3.0 | Few competitors, because few customers | Judgement |
| **Total** | **100** | | **57.0** | | |

**Major risks.** Too small to amortise fixed cost. **Gaps.** No partner identified; no flow estimate attempted, because published corridor data is thin.

### 3.6 Malawi — 30.0 / 100

| Criterion | Wt | Score | Contribution | Evidence and reasoning | Status |
|---|---|---|---|---|---|
| PSP availability | 20 | 1 | 4.0 | Very few licensed providers capable of the payout leg; the three-PSP test likely fails structurally | Pending validation |
| Banking stability | 15 | 2 | 6.0 | Functioning but constrained; correspondent relationships limited | Pending validation |
| Settlement infrastructure | 15 | 2 | 6.0 | Domestic rails exist; reliability and integration quality uncertain | Unknown |
| Liquidity availability | 15 | 1 | 3.0 | FX allocation is the constraint, not balance size; a funded float can still fail to settle | Pending validation |
| FX convertibility and volatility | 10 | 1 | 2.0 | Kwacha volatility and FX scarcity; unhedgeable at this scale | Secondary |
| Commercial opportunity | 15 | 1 | 3.0 | Real need, but a price the market can bear is unlikely to cover the risk | Judgement |
| Operational complexity | 5 | 3 | 3.0 | Simple counterparty map, difficult liquidity management | Estimate |
| Competitive intensity | 5 | 3 | 3.0 | Thin competition, thin market | Judgement |
| **Total** | **100** | | **30.0** | | |

**Major risks.** A funded position that cannot be converted is worse than no position. **Verdict.** Not fundable at current capital.

### 3.7 What the scores establish, and what they do not

| Market | Score /100 | Eligible | Rank by score |
|---|---|---|---|
| Brazil | 80.0 | Yes | 1 |
| Côte d'Ivoire | 73.0 | Yes | 2 |
| Botswana | 57.0 | Yes | 3 |
| Malawi | 30.0 | Yes | 4 |
| Congo (DRC) | Not scored | **No** | — |

Brazil leads on capability. It has better settlement infrastructure, deeper liquidity and a bigger priced market. **That is not the same as being launchable**, which is the subject of §4 — and anyone reading only the score would choose the wrong corridor. The score answers "can this be operated well?"; launch order answers "can this be started, by this team, with this balance sheet, this quarter?"

Two honest limitations of the scoring itself:

- The spread between Brazil (80) and Côte d'Ivoire (73) is inside the method's own error bars. Several inputs are judgements, and a two-point change on PSP availability would reverse the order.
- Commercial opportunity is the weakest-evidenced criterion in every market. It is scored on published pricing, not on observed customer willingness to switch.

---

## 4. Corridor Prioritisation

### 4.1 The access gate

Market score does not decide launch order. Six execution tests do, and each is pass or fail — not a score.

| # | Test | Pass condition | Côte d'Ivoire | Brazil |
|---|---|---|---|---|
| 1 | Three payout-side providers **identified** | Named entities, verified on the regulator's register | Pass (9 licensed EPs published) [S2] | Pass (large licensed population) |
| 2 | Commercial decision-maker **reachable** | A named individual with pricing authority takes a call within 5 business days | **Not demonstrated** | **Not demonstrated** |
| 3 | Banking partner available | An approved intermediary willing to open accounts and quote an FX margin | **Not demonstrated** | **Not demonstrated** |
| 4 | Settlement arrangement obtainable | Contracted cycle, cut-off and returns policy in writing | **Not demonstrated** | **Not demonstrated** |
| 5 | Liquidity source identified | A named source of XOF/BRL at short notice, priced | **Not demonstrated** | **Not demonstrated** |
| 6 | Regulatory path confirmed | Written confirmation of who originates the cross-border leg | Pass (RFE requires approved intermediary) [S4] | Pending validation |

**Status at the date of this document: four of six tests are undemonstrated in both markets. No partner has been contacted, no rate card has been quoted and no bank has been approached.** Everything below is therefore a *ranked hypothesis with a test date*, not a finding. Saying so is the only defensible position; a framework that implies meetings it did not hold is worth less than one that states its position plainly.

### 4.2 The access sprint (7 calendar days)

| Day | Action | Output |
|---|---|---|
| 1 | Build a 12-name list per market from the BCEAO EP register, the approved-intermediary list and competitor payout pages | 12 names, 2 contacts each |
| 2-3 | Outreach: warm introduction first, cold second; ask for 20 minutes with pricing authority | Booked calls or logged refusals |
| 4-5 | Calls: authorisation held, payout methods, quoted fee, settlement cycle, float minimum, RFE documentation | A quoted rate card per provider, or the reason none was given |
| 6 | Verify each authorisation against the regulator's published register | Gate evidence, not self-report |
| 7 | Written go/no-go per market, signed by the author | Decision memo |

**Gate rules.** A provider that will not quote has not passed, however senior the contact. Two entities in the same group count as one. A provider absent from the register fails regardless of what it says about itself. A bank that will discuss FX but will not confirm it will act as approved intermediary for this flow has not passed test 3.

### 4.3 Why Côte d'Ivoire ← France is the provisional first corridor

Four reasons, in order of how much they actually decide:

1. **The float is fundable.** About $60,000 of committed float (§5.3) against a five-figure balance sheet. Brazil needs roughly $150,000 plus hedge margin because its settlement gap and FX position are both larger. On a small balance sheet this is not a preference; it is the difference between launching and not.
2. **The currency cannot move against the position.** XOF is fixed at 655.957 to the EUR with no band [S14]. For a first corridor run by a team without a treasury function, removing an entire risk category is worth more than a larger addressable market.
3. **The payout leg is domestic, instant and price-capped.** PI-SPI settles wallet-to-wallet at par in seconds, with a 0.8% ceiling above the free threshold [S6]. Predictable unit cost on the leg where most transactions fail elsewhere.
4. **The cross-border leg has a defined legal shape.** RFE requires an approved intermediary bank; that is a constraint, but it is a *known* constraint with a published list of eligible banks [S5], not an unwritten discretion.

**What this is not.** It is not a claim that Côte d'Ivoire is the bigger opportunity — Brazil scores higher. It is not a claim that access exists — it has not been tested. It is not a claim that pricing is comfortable — the corridor benchmark is 4.05% and the domestic rail is capped at 0.8%, so the take rate has a visible ceiling [S15, S6].

### 4.4 The fallback, and the rule that decides

**If Côte d'Ivoire fails the access gate and Brazil passes:** Brazil ← US becomes the first corridor. The cost is stated rather than hidden — minimum float rises to roughly $150,000 plus hedge margin, and the fixed-cost base rises with Portuguese-language compliance and a BACEN-authorised FX counterparty. **If the balance sheet cannot fund that float, Brazil is not a fallback; it is a later phase.**

**If both fail:** the answer is not a third market. It is that Riverpe has a distribution or credibility problem, not a supply problem, and the next 90 days belong to customer commitments and partner relationships before any corridor is committed.

**The rule, stated once.** The first corridor is whichever eligible market clears all six access tests *and* whose minimum float is below committed capital. Preference, score and market size do not enter that sentence.
---

## 5. Treasury and Liquidity Strategy

Treasury is not a support function in this business; it is the product's constraint. v2 treated a liquidity failure as a reason to retry on a backup provider. It is not: a backup with no funded balance fails at the same moment as the primary, and retrying against an empty float converts one failed transaction into a failed corridor.

### 5.1 A. Pre-funding requirements

| Requirement | Value | Basis |
|---|---|---|
| Settlement currency (payout side) | XOF | Beneficiaries are credited in XOF |
| Funding currency | EUR | Senders pay in EUR; peg removes translation risk |
| Average daily payout at pilot | $4,000 | 600 transactions/month at $200 median ÷ 30 |
| Peak daily payout | $7,200 | 1.8× average at month-end and salary weeks (assumption) |
| Structural settlement gap | 1 business day, extending to 3 over a weekend | Collection T+0/T+1; bank conversion and credit T+1; payout instant |
| Replenishment | Weekly, plus event-driven | Refill by SEPA transfer when cover falls below 5 days |
| Minimum operating balance, payout account | $30,000 | Worst-case weekend gap of $21,600 plus 40% headroom |
| Minimum balance, aggregation partner | $12,000 | Three days of average payout held at the aggregator |
| Contingency reserve | $15,000 | One stuck batch resolved manually without missing payroll |
| **Committed float to launch** | **$57,000 (plan $60,000)** | Sum of the three lines above |

**Why this is higher than the $50,000 in v3.** Two corrections, both from primary sources rather than caution: the RFE regime requires an approved intermediary bank in the settlement position, which adds a bank operating balance that did not exist in the earlier three-PSP design [S4]; and the settlement gap through a weekend is three days, not two, because the bank leg follows the business-day calendar while wallet payout does not. Funding a 2-day gap when the true gap is 3 days is how a corridor runs dry on a Monday.

### 5.2 B. Cost of capital and holding local currency

Three distinct costs, routinely conflated:

| Cost | Calculation | Result at pilot | Comment |
|---|---|---|---|
| **Devaluation** | XOF fixed at 655.957, no band [S14] | Zero by construction | The reason this corridor is affordable; not a permanent property of the business |
| **Funding cost of idle balance** | $60,000 × 5% ÷ 12 | $250/month | At $120,000 monthly volume = **0.21% of volume**, or about 7% of gross revenue |
| **Conversion cost** | 0.25% spread on each refill | ~$126/month at $50,000 refilled monthly | Already inside unit economics; do not double-count |
| **Bank and custody fees** | Account, transfer and reporting charges | $100-200/month (assumption) | Priced per relationship, not per transaction |

The important number is the second row. At pilot volume, **float carrying cost is 0.21% of volume** — larger than the entire network and reconciliation line. At $1.14m monthly volume the same float costs 0.02%. Float cost is a small-volume problem that scale solves, which is exactly why a pilot cannot be judged on margin.

**Opportunity cost is real and usually ignored.** $60,000 held in a non-interest-bearing XOF operating account earns nothing. At a 5% cost of capital the corridor must generate at least $3,000 a year before it has paid for the privilege of existing, on top of its operating costs.

### 5.3 C. Settlement management

| Leg | Instrument | Timing | Cash effect |
|---|---|---|---|
| Collection, France | SEPA Instant Credit Transfer | Seconds, 24/7, where the payer's provider supports it [S18] | Receivable cleared same day |
| Collection, France | SEPA Credit Transfer | By end of the next business day [S19] | Receivable cleared T+1 |
| Conversion and cross-border settlement | Approved intermediary bank | Value date T+1, subject to cut-off [S20, pending validation] | XOF credited to payout account |
| Payout to wallet | PI-SPI / partner API | Instant, 24/7 [S6] | Cash out immediately |
| Payout to bank account | Domestic transfer | Same day if before cut-off, else next business day | Cash out T+0/T+1 |

**The asymmetry that creates the float.** Payout is instant and runs at weekends; the bank leg is a business-day process with a cut-off. A Friday evening payout is funded by Riverpe and reimbursed on Monday or Tuesday. That is the three-day gap in §5.1, and it is structural, not a partner defect.

**Operating rules.**

- **Cut-off discipline.** No payout batch is released after the bank's cut-off unless the payout account already holds cover for it. Releasing on the assumption of next-day reimbursement is how a corridor discovers its true float requirement at the worst moment.
- **Three-way reconciliation daily.** Provider settlement file vs Riverpe ledger vs bank statement. Unexplained breaks are incidents, not backlog.
- **Settlement failure procedure.** On a missed settlement: freeze new payout above the cover threshold, notify the partner's operations contact with the batch reference, reconcile to the transaction, and only then release. Never re-send a batch that may already have settled; the second send is a double payment and a compliance event.

### 5.4 D. Foreign exchange exposure

| Exposure | Size | Management |
|---|---|---|
| **Intraday** — rate moves between collection and conversion | Up to one day of volume | Immaterial under the peg; would be material in Brazil |
| **Overnight and weekend** — XOF held while EUR receivables settle | 1-3 days of volume | Accepted; peg removes the price risk, leaving only liquidity risk |
| **Spread** — bank margin versus reference | 0.20-0.35% (assumption, to be quoted) | Priced into the take rate; measured per transaction, not averaged monthly |
| **Convertibility** — ability to obtain XOF at all | Event risk | Mitigated by holding a working balance rather than converting on demand |
| **Peg risk** — a change in parity | Tail risk | Not hedgeable at this scale. Managed by limiting float to days of volume, not by instrument |

The last row is the honest one. A peg is not a guarantee; it is a low-probability, high-impact exposure that a small operator cannot hedge. The correct response is to keep the position small enough that a parity event is survivable, and to say so to investors rather than describing the corridor as "FX-free".

### 5.5 E. Liquidity failure management

Six failure types, deliberately separated, because they look identical to a customer and require different owners.

| Failure | What it actually is | Owner | Response | What not to do |
|---|---|---|---|---|
| **Provider technical failure** | API or platform down; balances intact | Operations | Route to the second live provider | Re-send blindly through a queue |
| **Settlement failure** | Batch sent, funds not credited on time | Treasury + Partnerships | Trace with the partner; hold new payout above cover | Re-send a batch that may have settled |
| **Liquidity shortage at partner** | Provider's own float at a wallet network is exhausted | Treasury | Top up within 4 hours; throttle intake at the threshold | Assume the backup resolves it — the backup has its own balance |
| **Treasury funding failure** | Riverpe's own account cannot cover the day's payout | Treasury (CFO-level) | Throttle intake, honour in-flight, extend the replenishment | Queue transactions and hope for a Monday credit |
| **Banking partner failure** | Approved intermediary suspends the flow or the relationship | CEO + Treasury | Activate the second bank; expect 2-4 weeks, not 2 days | Promise customers continuity you cannot deliver |
| **FX execution failure** | Rate unavailable or conversion rejected | Treasury | Pause payout, execute at next window, absorb the spread | Quote a rate you cannot obtain |

**Treasury escalation ladder.**

| Trigger | Action | Authority |
|---|---|---|
| Cover < 5 days | Replenish; review next week's payout plan | Treasury analyst |
| Cover < 3 days | Replenish immediately; notify CFO; hold new customer onboarding | CFO |
| Cover < 2 days | Throttle intake; prioritise in-flight and payroll-dated transactions | CFO |
| Cover < 1 day | Stop new intake; publish a status notice to customers | CEO |
| Cover = 0 | Incident response: honour what is funded, communicate what is not, no silent failures | CEO |

**Cover is measured in days, not currency.** Cover = deployable float ÷ trailing 7-day peak daily payout. Using the average instead of the peak is the most common way a corridor that "looked funded" fails at month-end.

### 5.6 Illustrative treasury model — 10 business days at pilot volume

Opening payout-account balance $50,000. Payouts $4,000/day, $7,200 on days 6-7 (month-end). Collections reimburse two days later.

| Day | Payout | Collection received | Closing balance | Cover (days at peak) |
|---|---|---|---|---|
| 1 | 4,000 | 0 | 46,000 | 6.4 |
| 2 | 4,000 | 0 | 42,000 | 5.8 |
| 3 | 4,000 | 4,000 | 42,000 | 5.8 |
| 4 | 4,000 | 4,000 | 42,000 | 5.8 |
| 5 | 4,000 | 4,000 | 42,000 | 5.8 |
| 6 | 7,200 | 4,000 | 38,800 | 5.4 |
| 7 | 7,200 | 4,000 | 35,600 | 4.9 |
| 8 | 4,000 | 7,200 | 38,800 | 5.4 |
| 9 | 4,000 | 7,200 | 42,000 | 5.8 |
| 10 | 4,000 | 4,000 | 42,000 | 5.8 |

**Trough: $35,600 on day 7.** Maximum cumulative deficit is $14,400 (2 × $7,200), which is why the account needs $30,000 rather than $15,000: the deficit plus a weekend extension plus headroom. Everything in this table is an **estimate** built on assumed volume and an assumed 1.8× peak factor. The shape is robust; the numbers are not yet observed.

---

## 6. Unit Economics and Financial Model

All figures are **modelled planning numbers built from labelled assumptions**, not quoted rates. They exist to be replaced line by line with a rate card from §4.

### 6.1 Definitions, stated so the arithmetic can be checked

| Term | Definition |
|---|---|
| **GTV** | Gross transaction value — the payout amount, not Riverpe's income |
| **Gross revenue** | Take rate × GTV |
| **Direct costs** | Collection fee, payout fee, FX spread, float carry, network/reconciliation |
| **Gross profit** | Gross revenue − direct costs |
| **Gross margin** | Gross profit ÷ gross revenue |
| **Net revenue** | Gross profit, after all variable costs attributable to the transaction |
| **Contribution margin** | Contribution ÷ gross revenue |
| **Cost per transaction** | Direct costs ÷ settled transactions |
| **Break-even volume** | Monthly fixed cost ÷ net contribution rate |

**The error this table prevents.** Reporting $120,000 of monthly GTV as "revenue" overstates income by a factor of 33 at a 3% take rate. Every figure below is revenue or contribution, never volume.

### 6.2 Base case — per transaction, $200 ticket

| Line | Rate | Per $200 | Note |
|---|---|---|---|
| **Customer price (take rate)** | 3.00% | **$6.00** | Below the 4.05% corridor average and the 3.54% digital benchmark [S15, S16] |
| Collection fee (funding-side provider) | −0.30% | −$0.60 | SEPA or card collection; assumption |
| Payout fee (local provider) | −0.85% | −$1.70 | Blended across primary and backup |
| FX spread (approved intermediary) | −0.25% | −$0.50 | Mid of the 0.20-0.35% assumption |
| Float carrying cost | −0.21% | −$0.42 | $60,000 at 5% over $120,000 monthly volume |
| Network, reconciliation, chargeback | −0.15% | −$0.30 | Card disputes, manual recon, monitoring |
| **Direct cost total** | **1.76%** | **$3.52** | |
| **Net contribution** | **1.24%** | **$2.48** | Per $1,000 moved: **$12.40** |

Gross is 3.00%; net is 1.24%. **59% of the take rate is consumed by direct cost.** That ratio, not the headline price, is the business.

### 6.3 Three scenarios

| Line | Conservative | Base | Optimistic |
|---|---|---|---|
| Take rate | 2.50% | 3.00% | 4.00% |
| Collection fee | 0.40% | 0.30% | 0.25% |
| Payout fee | 1.10% | 0.85% | 0.65% |
| FX spread | 0.35% | 0.25% | 0.20% |
| Float carry | 0.30% | 0.21% | 0.10% |
| Network and recon | 0.20% | 0.15% | 0.12% |
| **Total direct cost** | **2.35%** | **1.76%** | **1.32%** |
| **Net contribution rate** | **0.15%** | **1.24%** | **2.68%** |
| Net per $200 ticket | $0.30 | $2.48 | $5.36 |
| Net per $1,000 moved | $1.50 | $12.40 | $26.80 |
| Cost per transaction | $4.70 | $3.52 | $2.64 |
| Contribution margin | 6.0% | 41.3% | 67.0% |

**Scenario assumptions, disclosed.**

- *Conservative:* competitive pressure forces the price to 2.50%, payout is quoted at the top of the range, FX margin is worse than expected, and float carry is high because volume stays small. Volume grows from 300 to 600 transactions/month over 12 months.
- *Base:* price holds at 3.00%, blended fees land mid-range, and float cost falls as volume grows. Volume grows from 600 to 2,000 transactions/month.
- *Optimistic:* a reliability premium is earned and sustained at 4.00%, payout is renegotiated to 0.65% on volume, and float is recycles faster. Volume reaches 4,000 transactions/month.

Fixed cost is held at **$18,000/month** in all three: two loaded salaries, compliance tooling and monitoring, legal and audit amortisation, insurance, and the infrastructure minimum.

### 6.4 Monthly P&L at pilot scale (600 transactions, $120,000 GTV)

| Line | Conservative | Base | Optimistic |
|---|---|---|---|
| GTV | $120,000 | $120,000 | $120,000 |
| Gross revenue | $3,000 | $3,600 | $4,800 |
| Direct costs | $2,820 | $2,112 | $1,584 |
| Gross profit | $180 | $1,488 | $3,216 |
| Fixed costs | $18,000 | $18,000 | $18,000 |
| **EBITDA** | **−$17,820** | **−$16,512** | **−$14,784** |

The pilot is designed to lose money. What it buys is corridor proof, a failure taxonomy and a rate card that has been tested against real settlement — not margin.

### 6.5 Break-even volume

Break-even GTV = fixed cost ÷ net contribution rate. At $200 average ticket, transactions = GTV ÷ 200.

| Take rate | Net rate (base cost structure) | Break-even GTV/month | Transactions/month |
|---|---|---|---|
| 2.0% | 0.24% | $7,500,000 | 37,500 |
| 2.5% | 0.74% | $2,432,432 | 12,162 |
| **3.0%** | **1.24%** | **$1,451,613** | **7,258** |
| 3.5% | 1.74% | $1,034,483 | 5,172 |
| 4.0% | 2.24% | $803,571 | 4,018 |
| 5.0% | 3.24% | $555,556 | 2,778 |
| 6.0% | 4.24% | $424,528 | 2,123 |

**Worked example of the base row:** $18,000 ÷ 0.0124 = $1,451,612.90; ÷ $200 = 7,258 transactions.

### 6.6 What the model says

**At a 3% price this corridor needs about $1.45m of monthly volume to break even — twelve times the pilot.** That is attainable in year two and impossible in month four. The corridor is a valid proof of operation and an invalid near-term business, and it should be funded and judged on exactly that basis.

**The price is boxed in from both sides.** The France→Côte d'Ivoire corridor averaged 4.05% total cost in Q3 2025, with a cheapest observed transparent quote at 2.46% [S15]. Domestic transfers in Côte d'Ivoire are free below XOF 8,000 and capped at 0.8% above it [S6]. So a 3% price is: below the corridor average, above the domestic rail, and above the 3.54% digital-only benchmark for the region [S16]. There is room to price at 4%, but only if reliability is demonstrable; there is no room to price at 6% without a product the incumbents do not offer.

**The conservative case does not work at any plausible pilot volume.** At 0.15% net contribution, break-even is $12m a month. That is not a scenario to plan around; it is a warning that a price concession plus a fee miss is existential, and the reason the KPI in §11 triggers at $9 per $1,000 rather than at break-even.

**Decision rule.**

- Launch only if **take rate ≥ 3.5%** or a written volume path to **$1.5m/month within four quarters** exists.
- If neither holds, run the corridor as a fixed-budget data exercise with a stop date, and say so before committing the float.
- Report **net contribution per $1,000 moved**, never take rate alone. The first number survives a finance review; the second invites an argument about gross margin that the cost base settles immediately.
---

## 7. Worked Corridor: Côte d'Ivoire ← France

**Corridor.** Funds collected in France in EUR, paid out in Côte d'Ivoire in XOF to mobile wallets and bank accounts. Median ticket €200. Target customers: diaspora senders and small businesses paying suppliers.

**No provider is named anywhere in this section.** Counterparties are described by operational category, which is what a reader needs in order to map their own market. Fees and timings marked *A* are illustrative assumptions; those marked *V* are verified from the sources in §14.

### 7.1 The counterparties, by position

| Position | Category | Authorisation held | What it does | Commercial shape (assumed) |
|---|---|---|---|---|
| **F1** | Funding-side payment institution | French payment institution, or Riverpe as its registered agent | Collects EUR by SEPA transfer and card, performs payer KYC | 0.30% of collected value |
| **B1** | Approved intermediary bank | Designated intermediary under the RFE regulation [S4, S5] | Executes FX, moves funds cross-border, credits XOF account, files declarations | 0.25% FX margin plus per-transfer fee |
| **P1** | Local payout provider — aggregator | BCEAO *établissement de paiement* [S1, S2] | Bulk disbursement to all wallet networks and bank accounts via PI-SPI | 0.85% of payout value |
| **P2** | Local payout provider — bank-led | Licensed bank or its payments subsidiary | Settlement-grade payout, bank-account credits, cheaper at volume | 0.60-0.90%, slower onboarding |
| **X1** | Liquidity source | Bank treasury or FX desk at B1 | Supplies XOF forward of need; sets the conversion quote | Priced into the spread |

**Why four positions and not three.** The RFE regime forbids payment institutions and e-money institutions from originating payments abroad [S4]. The bank is therefore not a commercial choice between two providers; it is a mandatory node. v3's three-provider design was legally incomplete, and this is the correction that changes the float, the onboarding plan and the contract set — not the thesis.

**Minimum viable redundancy.** F1 + B1 + P1 + P2, with P1 and P2 live simultaneously. A corridor with one payout provider is not a corridor; it is a single point of failure with a marketing site.

### 7.2 The transaction lifecycle, step by step

A single €200 transfer, sender in France, beneficiary in Abidjan holding a wallet.

| # | Step | Actor | What happens | Timing | Verified? |
|---|---|---|---|---|---|
| 1 | Initiation | Customer | Sender enters amount, beneficiary identifier, purpose. Riverpe quotes the XOF the beneficiary will receive, all-in | Instant | Product design |
| 2 | Collection | F1 | EUR 206.00 debited (€200 payout + 3.00% take). SEPA Instant if the provider supports it, otherwise SEPA CT | Seconds to T+1 [S18, S19] | V |
| 3 | Receipt confirmation | F1 → Riverpe | Webhook with provider reference, amount, payer name, timestamp; signature verified | Seconds after collection | V |
| 4 | Reconciliation (first pass) | Riverpe | Transaction matched to quote and to ledger entry; duplicate check by idempotency key; sanctions screening result attached | < 60 seconds | Architecture |
| 5 | Treasury position update | Riverpe | Payout obligation booked against the XOF account; available cover recalculated; batch eligibility checked | Immediate | Architecture |
| 6 | FX conversion | B1 | EUR→XOF at reference 655.957 less 0.25% margin. Conversion booked with value date and rate reference | Intraday to T+1 | Peg V [S14]; margin A |
| 7 | Settlement instruction | B1 | XOF credited to Riverpe's payout account; declaration filed with underlying documents | T+1, subject to cut-off | V framework [S4]; timing A |
| 8 | Payout | P1 | Batch includes the transaction; funds pushed to the beneficiary wallet over PI-SPI; provider returns a per-item status | Seconds, 24/7 [S6] | V |
| 9 | Reconciliation (second pass) | Riverpe | Provider settlement file vs ledger vs bank statement; beneficiary credit confirmed; break logged if status is ambiguous | Daily | Architecture |
| 10 | Revenue and cost posting | Finance | Gross revenue, each cost line and net contribution posted per transaction; FX spread measured against reference | Daily, reported monthly | Architecture |

### 7.3 The same transaction in numbers

| Item | EUR | XOF | Note |
|---|---|---|---|
| Payout value | 200.00 | 131,191 | At 655.957 (V) |
| Take rate 3.00% | 6.00 | 3,935 | Revenue, not margin |
| **Customer pays** | **206.00** | | |
| Collection fee 0.30% | −0.60 | −393 | F1 |
| FX margin 0.25% | −0.50 | −328 | B1; XOF received falls to 130,863 |
| Payout fee 0.85% | −1.70 | −1,115 | P1; beneficiary receives 129,748 |
| Network, recon, chargeback 0.15% | −0.30 | −197 | Provisioned |
| Float carry 0.21% | −0.42 | −275 | Monthly allocation |
| **Total direct cost** | **−3.52** | **−2,308** | 1.76% of payout value |
| **Net contribution** | **2.48** | **1,627** | 1.24% of payout value |

**Check the arithmetic.** 131,191 × 0.0300 = 3,935.7 XOF revenue. 131,191 × 0.0176 = 2,309.0 XOF direct cost (rounding accounts for the 2,308 shown). 3,935.7 − 2,309.0 = 1,626.7 XOF = €2.48 at 655.957. The beneficiary receives 129,748 XOF for €206.00 paid — an effective cost to the sender of 4.09% including the FX margin, which is at the corridor average [S15].

**What the customer sees versus what Riverpe keeps.** The sender pays €6.00 above the payout value and receives XOF 129,748 rather than the XOF 131,191 that €200 converts to at the reference rate. That gap — 1.10% — is FX margin and payout fee showing up as a worse rate. Disclosing it as a rate rather than a fee is legal, common, and the fastest way to lose a customer who checks; the recommendation is to quote the all-in percentage.

### 7.4 Flows, separated

| Flow | Path | Content | Failure if broken |
|---|---|---|---|
| **Transaction** | Customer → F1 → Riverpe → B1 → P1 → beneficiary | Payment instruction and status | Double payment or lost payment; mitigated by idempotency keys and status-state machine |
| **Funds** | Customer bank → F1 → B1 → Riverpe XOF account → P1 → beneficiary wallet | EUR then XOF | Liquidity failure (§5.5) |
| **Data** | Riverpe ↔ F1, B1, P1 | References, amounts, status, KYC attributes, screening results | Reconciliation break; unresolved breaks become audit findings |
| **Documents** | Riverpe → B1 | Purpose of payment, underlying invoice or remittance details, payer and beneficiary identification | RFE non-compliance; the bank can reject or suspend the flow [S4] |

### 7.5 Failure scenarios, priced

| Scenario | Frequency (assumed) | Customer impact | Response | Cost |
|---|---|---|---|---|
| Provider timeout at payout | 1 in 500 | Delayed minutes | Retry with idempotency key; status reconciled before any re-send | Nil |
| Wallet credit fails (wrong identifier) | 1 in 300 | Funds returned, sender notified | Return to sender or hold for correction; never auto-retry | Refund fee plus support time |
| P1 balance exhausted | Monthly at peak | Payouts queue | Top up; shift batch share to P2 | Float acceleration, ~0.05% of volume |
| B1 misses cut-off | Weekly if undisciplined | One-day delay | Hold batch; release next window | One day of float |
| FX rate unavailable | Rare | Quote withdrawn | Pause new quotes; honour funded ones | Reputational |
| RFE documentation rejected | Unknown, potentially 1 in 100 | Payment held for days | Case-by-case with bank; documentation checklist tightened | Support cost plus float extension |
| Sanctions match | Rare | Payment blocked | Compliance review; no automatic retry | Regulatory reporting |

The RFE row is the one that is new in v4 and the one most likely to be underestimated. A documentation rejection is not a technical failure; it is a payment that sits in a bank while a customer waits, and it consumes float for as long as it sits.

### 7.6 What "working" looks like at day 90

600 transactions/month, $120,000 payout volume, first-attempt success ≥92%, settlement inside the contracted cycle on 95% of batches, zero compliance incidents, two payout providers live, one approved intermediary contracted. That proves the corridor operates. §6 shows why it does not yet prove a business.

---

## 8. Operational and Settlement Architecture

### 8.1 The principle that makes the rest affordable

**Adding a provider must be a configuration change, not a rewrite.** Every provider sits behind one internal interface: quote, collect, payout, status, reconcile. If the second provider in a corridor requires a code change, the second corridor costs the same as the first and the redundancy in §7.1 is theoretical.

### 8.2 Components

| Component | Function | Build-or-buy | Why it matters |
|---|---|---|---|
| **Provider abstraction layer** | Normalises collection and payout across F1, B1, P1, P2 | Build (thin) | Converts partner redundancy from a promise into a switch |
| **Ledger** | Double-entry, per-corridor, per-currency accounts for float, receivables, payable-to-customer, revenue and each cost line | Build | Without it, "net contribution per $1,000" cannot be computed and §11 is decoration |
| **State machine** | Explicit states: quoted, collecting, collected, converted, settling, paid, failed, reversed | Build | Prevents the double-payment class of incident |
| **Idempotency** | Every instruction carries a key; re-sends are no-ops | Build | The single highest-value 40 lines in the system |
| **Reconciliation engine** | Three-way match, daily, with a break queue and ageing | Build | Detects partner errors before customers do |
| **Sanctions and PEP screening** | Screening at onboarding and per transaction, with audit trail | Buy | Cannot be improvised; evidence is required |
| **Observability** | Success rate, latency, float cover, break ageing, per-provider error codes | Buy | The five KPIs in §11 need a source |
| **Document generation** | RFE purpose codes and supporting documents per transfer | Build | Bank rejects are otherwise unmanageable at volume |

### 8.3 Settlement architecture

```
EUR collection          Approved intermediary            XOF payout
-----------------       ------------------------         -----------------
F1 (PSD2, SEPA)  -->    B1: FX + RFE declaration  -->    Riverpe XOF account
                        value date T+1                   |
                                                         +--> P1 (EP, PI-SPI) --> wallets
                                                         +--> P2 (bank)        --> accounts
```

**Rules that keep it solvent.**

- Payout releases only against settled or covered balances. A receivable is not cover.
- The XOF account is the single source of truth for cover; no provider's dashboard is.
- Cut-off calendar is maintained as data, not folklore, including Ivorian and French public holidays.
- Every provider has a named operations contact and a stated escalation path, tested once before launch.

### 8.4 The cut-off calendar problem

Four calendars interact: French banking days (SEPA), the intermediary's correspondent cut-offs, WAEMU business days (RTGS and bank settlement), and the wallet networks, which do not close. On a Friday before a French public holiday, a payout can be funded by Riverpe for up to four days. That scenario should be modelled explicitly in the float, not discovered in the first month; it is the reason §5.1 sets the payout account at $30,000 rather than the $14,400 that two average days would imply.

### 8.5 Data and records

| Record | Retention | Why |
|---|---|---|
| Transaction and quote | 5 years minimum | Regulatory and dispute |
| KYC and screening result | 5 years minimum | AML evidence |
| RFE documentation | 5 years minimum | Bank and regulator request |
| Reconciliation breaks | 5 years | Audit trail of resolution |
| Provider rate cards and contracts | Life of relationship plus 5 years | Repricing and dispute |

Retention periods are a **planning assumption** based on common AML practice, not a verified WAEMU requirement; the partner's compliance officer should confirm them in writing before launch.
---

## 9. Risk Management

### 9.1 Register

Likelihood and impact are rated Low / Medium / High. "Residual" is the exposure after the stated mitigation, not after hope.

| # | Risk | L | I | Mitigation | Owner | Residual |
|---|---|---|---|---|---|---|
| 1 | **Access failure** — three providers cannot be reached or will not quote | High | High | Run the 7-day sprint before any spend; fallback corridor named in advance (§4.4) | Founder | Medium |
| 2 | **RFE documentation rejection** — payment held at the bank for missing or wrong documents | Medium | High | Document checklist per purpose code; pre-clear two specimen transfers with the bank; support script for held payments | Compliance + Ops | Medium |
| 3 | **Payout provider fails or de-risks the flow** | Medium | High | Two live providers per corridor; contract termination notice; monthly review of provider exposure | Partnerships | Medium |
| 4 | **Liquidity shortfall at month-end** | Medium | High | Float sized to 1.8× peak; cover measured in days; throttle rule at 1 day (§5.5) | Treasury | Low |
| 5 | **Approved intermediary bank exits the relationship** | Low | High | Second bank identified and pre-qualified; 90-day notice clause; no single-bank dependency beyond year one | CEO | Medium |
| 6 | **PI-SPI pricing or rules change again** | Medium | Medium | Price on the cross-border value, not the domestic leg; contractual right to reprice; monitor BCEAO circulars | Strategy | Medium |
| 7 | **FX margin compression** | Medium | Medium | Quote per transaction; measure realised margin against reference daily; reprice weekly | Treasury | Medium |
| 8 | **AML or sanctions failure** | Low | High | Screening at onboarding and per transaction; independent audit before scale; no high-risk flows without written partner consent | Compliance | Low |
| 9 | **Peg parity change** | Very low | High | Unhedgeable at this scale; limit float to days of volume; disclose to investors as tail risk | CFO | Accepted |
| 10 | **Fraud — account takeover, mule accounts, first-party** | Medium | Medium | Velocity limits by customer; device and behaviour checks; hold rules on new beneficiaries | Risk | Medium |
| 11 | **Concentration in one customer or partner** | Medium | Medium | No customer above 25% of volume without a contract; no provider above 70% | Commercial | Medium |
| 12 | **Key-person dependency** | High | Medium | Treasury runbook written before launch; two people trained on reconciliation and escalation | CEO | Medium |
| 13 | **Regulatory transition** — the EP regime is 12 months old and still bedding in | Medium | Medium | Partner must confirm authorisation scope in writing; re-verify on the register quarterly | Compliance | Low |

### 9.2 The three risks that actually decide the outcome

1. **Access (row 1).** Everything in this document is contingent on it, and it is the one thing that cannot be bought, modelled or delegated. It is also cheap to test: seven days and a phone.
2. **Documentation (row 2).** The RFE regime is the least familiar part of this corridor and the most likely to generate a held payment. A held payment is a treasury event, a support event and a reputational event at the same time.
3. **Pricing ceiling (rows 6 and 7).** The domestic rail is capped at 0.8% and the corridor average is 4.05%. If both compress, the model in §6 moves to the conservative scenario, where break-even is $12m a month and the corridor is no longer a business.

### 9.3 What is not in this register, deliberately

Operational risks that are fully controllable — staff turnover, supplier invoices, office leases — are excluded. A risk register that lists everything ranks nothing.

---

## 10. Evidence and Industry Validation

### 10.1 Statement of evidence status

**No direct industry interviews have been completed at the time of this assessment. The framework remains subject to primary market validation.**

As of 20 November 2026 this document contains **no customer interviews, no provider calls, no quoted rate cards, no bank confirmations and no regulatory pre-clearance**. Every factual claim is secondary or primary *documentary* — a regulator instrument, a central-bank statistical release, an official register or a World Bank dataset — tagged in §14. The market scores in §3 are the author's judgement applied to those documents. They are not diligence.

Stating this plainly is the point. A framework that implies conversations it did not have is worth less than one that says what it knows, and a reader who discovers the gap later discounts everything else in the document.

### 10.2 Interview register

Empty by design. It must be filled before this document is used to commit to a corridor or to raise capital.

| Date | Role | Organisation type | Market | Subject | What they said | Effect on the plan | Verification |
|---|---|---|---|---|---|---|---|
| — | — | — | — | — | — | — | — |

### 10.3 Interviews required before launch

| # | Role | Why this role | The question that must be answered | Needed by |
|---|---|---|---|---|
| 1 | Head of partnerships, local payout provider | Owns the rate card and the float minimum | What is your month-end cash-out success rate by wallet network? | Week 1 |
| 2 | Payments product lead, bank-led payout provider | Owns cut-off and return handling | Will you settle bank-account payouts same day, and what is your return policy? | Week 1 |
| 3 | Trade finance or correspondent banking, approved intermediary | Controls the mandatory cross-border leg | Will you act as approved intermediary for this flow, and what documents do you require per transfer? | Week 2 |
| 4 | Compliance officer, either local provider | Can veto the corridor after launch | What KYC do you require, and who performs screening? | Week 2 |
| 5 | FX desk, approved intermediary | Prices the conversion and the float | What margin on EUR→XOF at $120k monthly, and what minimum balance? | Week 2 |
| 6 | Operations lead, a live remittance operator in the corridor | Has already paid for the mistakes | What broke in your first 90 days and what did it cost? | Week 3 |
| 7 | Founder or CFO, 3-5 target business customers | Confirms willingness to pay, not interest | What do you pay per transfer today, all in, including the rate? | Week 3 |
| 8 | Diaspora association representative or community agent network | Explains how senders actually choose a provider | What makes a sender switch, and what makes them switch back? | Week 4 |

**Minimum evidence bar before the corridor is committed:** six completed conversations covering rows 1, 3 and 7, with a quoted rate card from at least two providers, a written indication from one approved intermediary that it will act, and one customer stating their current all-in cost. Until then, §6's figures are a model and §3's scores are a hypothesis.

---

## 11. Five Decision-Critical KPIs

v2 carried twelve metrics across four tables. Twelve numbers on a dashboard is a way of avoiding a decision. These five remain because each one can change what the company does next week.

### 11.1 The five

| # | Metric | Definition | Calculation | Frequency | Target | Escalation threshold | Decision it informs |
|---|---|---|---|---|---|---|---|
| 1 | **Net contribution per $1,000 moved** | What Riverpe keeps after all direct costs, per $1,000 of payout value | (Gross revenue − direct costs) ÷ GTV × 1,000 | Monthly, weekly rolling | ≥ $12.00 | < $9.00 | Whether to hold price, renegotiate fees, or stop expanding the corridor |
| 2 | **Payout success rate** | Share of transactions credited to the beneficiary on first attempt within the contracted cycle | Settled first attempt ÷ transactions submitted | Daily | ≥ 92% pilot, ≥ 96% steady state | < 88% | Whether to keep onboarding customers or shift volume to the second provider |
| 3 | **Days of float cover** | How many peak-volume days the deployable float can fund | Deployable float ÷ trailing 7-day peak daily payout | Daily | ≥ 5 days | < 3 days | Whether to top up, throttle intake, or stop new business |
| 4 | **Cost to serve per transaction** | All-in direct cost of a settled transaction | Total direct costs ÷ settled transactions | Weekly | ≤ $3.60 | > $4.20 | Whether the provider mix or the pricing is wrong |
| 5 | **Ageing reconciliation breaks** | Value and count of unreconciled items older than 48 hours | Open breaks > 48h ÷ transactions in period | Daily, reported weekly | < 0.5% of value | > 1.0% of value | Whether to freeze payout and fix the pipe before volume grows |

### 11.2 Why these five, and not the others

- **Commercial performance:** #1 measures what the business keeps, not what it bills. It is the only number that cannot be improved by moving volume around.
- **Transaction economics:** #4 catches a provider mix that is quietly eroding margin before #1 shows it at month end.
- **Settlement reliability:** #2 is the promise being sold. Everything else is a supporting metric.
- **Liquidity efficiency:** #3 is the constraint that ends corridors (§5.5).
- **Operational risk:** #5 is the leading indicator of a broken pipe; it moves before customers complain.

### 11.3 Retired from v2

| Retired metric | Why it went |
|---|---|
| Number of corridors | Rewards announcing markets, not operating them |
| Number of PSP partners signed | Rewards signatures over settlement |
| Monthly revenue | Moves with volume and hides margin; replaced by #1 |
| Gross take rate | Invites an argument the cost base settles; kept as an input, not a KPI |
| API uptime | Provider's obligation, not Riverpe's differentiator; covered by #2 |
| Customer NPS | Meaningless below 500 customers, and lagging |
| Onboarding time | Operational hygiene, not a decision trigger at this stage |

One metric was **added** rather than retired: ageing reconciliation breaks. v2 had no leading indicator of operational failure, which is why its failure table read as a list of surprises.
---

## 12. Implementation Roadmap

Capital figures are **estimates**; dates assume the access sprint starts on 23 November 2026.

| Phase | Window | Work | Exit gate | Capital committed |
|---|---|---|---|---|
| **0. Access** | Days 1-7 | Six-test sprint (§4.2) across Côte d'Ivoire and Brazil; register checks; refusals logged | Written go/no-go per market | $0 |
| **1. Structure** | Days 8-30 | Contracts with F1, B1, P1; P2 in diligence; bank accounts opened; float facility agreed; RFE documentation checklist agreed with B1 | One bank confirmed as approved intermediary; two payout providers contracted; $60,000 float available | $60,000 float + $10,000 legal |
| **2. Build** | Days 31-60 | Provider abstraction layer; ledger; state machine; reconciliation; screening integration; cut-off calendar | Sandbox-to-production in under a week per provider; reconciliation balances for 5 consecutive days | $25,000 build (or founder time) |
| **3. Pilot** | Days 61-90 | 3-5 customers, controlled volume, manual review of every exception; failure taxonomy started | Success ≥92%; float cover ≥5 days; zero compliance incidents | $18,000/month opex |
| **4. Prove** | Days 91-180 | Volume to $400,000/month; third provider signed; pricing tested at 3.5-4.0%; second bank qualified | Net contribution ≥$12 per $1,000; success ≥95% | $54,000 opex + float top-up |
| **5. Decide** | Days 181-365 | Either scale to $1.5m/month and open corridor two, or stop and return the float | Break-even path in writing, or an orderly wind-down | Case-dependent |

**Sequencing rules.** One corridor at a time until net contribution per $1,000 is above target for two consecutive months. The abstraction layer is not optional, and it is not a phase-two item: built later, it is a rewrite. No customer is promised a payout date before the provider's authorisation has been checked against the register and the bank has confirmed the flow in writing.

---

## 13. Outstanding Assumptions and Research Gaps

Every row is something a reader should not assume. Nothing in this section is hidden elsewhere in the document.

| # | Gap | Why it matters | How it gets resolved | By |
|---|---|---|---|---|
| 1 | **No provider has been approached** | All access claims are conditional | Run §4.2 | 30 Nov 2026 |
| 2 | **No rate card quoted** | Every fee in §6 is an assumption | Replace line by line after the sprint | 30 Nov 2026 |
| 3 | **No approved intermediary has confirmed the flow** | Without it the corridor cannot legally operate | Written indication from one bank | 15 Dec 2026 |
| 4 | **RFE documentation burden unquantified** | Drives support cost and float held in transit | Two specimen transfers cleared end to end | 15 Dec 2026 |
| 5 | **Corridor volume split unknown** | Commercial opportunity scored on price, not observed flow | Request corridor-level data from providers; BCEAO balance of payments detail | Q1 2027 |
| 6 | **Peak factor 1.8× is assumed** | Sets the float and the cover threshold | Replace with observed daily seasonality after 60 days of volume | Day 150 |
| 7 | **Fixed cost $18,000/month is a plan** | Drives every break-even number | Build the actual cost base before the pilot | Day 30 |
| 8 | **Direct licence timing and cost not verified** | Determines whether year two is partner-carried or own-licence | Written timeline from BCEAO or counsel | Q1 2027 |
| 9 | **Brazil corridor pricing not researched** | Fallback economics are unquantified | Corridor study using RPW and BACEN data | Q1 2027 |
| 10 | **Botswana and Malawi regulatory positions not read** | Scores rest on secondary description | Read the primary instruments if either becomes relevant | If promoted |
| 11 | **PI-SPI participation obligations for foreign-owned providers** | Could add a connection requirement and cost | Confirm with BCEAO or a licensed participant | 15 Dec 2026 |
| 12 | **Retention periods assumed at 5 years** | Compliance cost and storage design | Confirm with partner compliance | 15 Dec 2026 |
| 13 | **No customer willingness-to-pay evidence** | Pricing is benchmarked, not tested | Interviews 7 and 8 in §10.3 | 18 Dec 2026 |
| 14 | **Peg risk treated as unhedgeable** | A parity event would be absorbed, not hedged | Accept and disclose; no instrument exists at this scale | Standing |

---

## 14. Sources and References

All URLs accessed **20 November 2026**. Where a source is a secondary report of a primary instrument, it is labelled and the primary instrument is named so it can be checked.

| Tag | Organisation | Document | Published | URL | What it is used for | Limitations |
|---|---|---|---|---|---|---|
| **S1** | BCEAO | Instruction n°001-01-2024 relative aux services de paiement dans l'UMOA | 23 Jan 2024 | [bceao.int](https://www.bceao.int/sites/default/files/2024-02/Instruction%20N%C2%B0001-01-2024%20relative%20aux%20services%20de%20paiement%20dans%20l%27UMOA%20%20ok.pdf) | Payment institution regime; tiered minimum capital (XOF 10m / 20m / 30m / 100m) | French only; capital tiers depend on the licensed service set, which the register does not publish per entity |
| **S2** | BCEAO / Direction Générale du Trésor (CI) | Register of authorised payment establishments in UMOA, position at 28 Feb 2026 | Mar 2026 | [bceao.int](https://www.bceao.int/sites/default/files/2026-03/LISTE%20DES%20ETABLISSEMENTS%20DE%20PAIEMENT%20AGR%C3%89%C3%89S%20DANS%20L%E2%80%99UMOA%20au%2031%20janvier%202026.pdf) | 31 authorised EPs union-wide, 9 in Côte d'Ivoire, first authorisations May-Sep 2025 | File name references the January 2026 list while the content is dated 28 Feb 2026; per-entity licence scope is not shown |
| **S2b** | Direction Générale du Trésor (CI) | "La BCEAO agrée 31 nouveaux établissements dont 09 en Côte d'Ivoire" | 19 Mar 2026 | [tresor.gouv.ci](https://tresor.gouv.ci/tres/espace-uemoa-monnaie-electronique-la-bceao-agree-31-nouveaux-etablissements-dont-09-en-cote-divoire) | Corroborates the EP count and the legal basis | Government news item, not the register itself |
| **S3** | BCEAO | Instruction n°008-05-2015 (e-money issuers) and BCEAO FAQ on who may issue e-money | 21 May 2015; FAQ 9 Sep 2026 | [bceao.int](https://www.bceao.int/fr/documents/qui-peut-emettre-de-la-monnaie-electronique-dans-luemoa-ou-lun-de-ses-etats-membres) | EME minimum capital XOF 300m, fully paid before authorisation | The named EME register has not been published since 2017; entity-level confirmation requires the partner |
| **S4** | UEMOA Council of Ministers / BCEAO | Règlement n°06/2024/CM/UEMOA relatif aux relations financières extérieures | 20 Dec 2024 (published 29 Jul 2025) | [bceao.int](https://www.bceao.int/fr/reglementations/reglement-ndeg062024cmuemoa-relatif-aux-relations-financieres-exterieures-des-etats) | Approved-intermediary requirement; art. 26 bars EPs and EMIs from originating payments abroad | Does not set per-transfer documentation for a given purpose code; that is bank practice |
| **S5** | BCEAO / Commission Bancaire de l'UMOA | Instruction n°01/07/2025/RFE on execution of settlements with non-residents | 1 Aug 2025 | [cb-umoa.org](https://cb-umoa.org/sites/default/files/2025-08/Instruction%20n%C2%B0%2001%2007%202025%20RFE%20relative%20%C3%A0%20l%27ex%C3%A9cution%20des%20r%C3%A8glements%20%C3%A0%20destination%20ou%20en%20provenance%20de%20l%27%C3%A9tranger%20ou%20avec%20des%20non-r%C3%A9sidents.pdf) | Transfer request procedure through approved intermediaries; annual list of intermediaries | Operational turnaround for a transfer request is not published |
| **S6** | BCEAO, reported by Ecofin Agency | PI-SPI tariff revision effective 2 Nov 2026: free ≤ XOF 8,000/day, cap 0-0.8% above, receiving free, UEMOA cross-border parity 1 Jun 2027 | 5 Oct 2026 | [ecofinagency.com](https://www.ecofinagency.com/news/0510-59448-from-free-transfers-to-cfaf-8-000-bceao-reworks-its-instant-payment-promise) | Domestic payout price ceiling; regional reference price | **Secondary.** The BCEAO communiqué itself was not read; figures corroborated by several outlets |
| **S7** | BCEAO, reported by Linfodrome | PI-SPI: 175 participants, 38m+ users; free tier covers 75% of e-money transactions | 4 Oct 2026 | [linfodrome.com](https://www.linfodrome.com/economie/126097-mobile-money-les-petits-transferts-d-argent-gratuits-des-le-2-novembre) | Platform scale and reach | **Secondary.** Participant count is a point-in-time figure |
| **S8** | Banco Central do Brasil | Principles for Financial Market Infrastructures — SPI disclosure | 11 Feb 2026 | [bcb.gov.br](https://www.bcb.gov.br/content/estabilidadefinanceira/sistemapagamentosinstantaneos_docs/principios_infraestruturas_mercado_financeiro.pdf) | SPI settles in central-bank money, RTGS, 24/7, irrevocable, no overdrafts | Describes infrastructure, not commercial pricing |
| **S9** | Banco Central do Brasil | Retail payment statistics, H1 2026 (nota 21300) | Oct 2026 | [bcb.gov.br](https://www.bcb.gov.br/api/servico/sitebcb/notasImprensa/21300) | 79.7bn transactions; PIX 55.2% of count and ~44bn transactions | Excludes cash payments other than withdrawals; PIX value share differs from count share |
| **S10** | Banco Central do Brasil | Exchange-market regulation portal (consolidated FX framework) | Current | [bcb.gov.br](https://www.bcb.gov.br/estabilidadefinanceira/mercadocambial) | Basis for the statement that cross-border FX requires an authorised institution | **Not read in detail for this version - pending validation** |
| **S11** | Bank of Botswana | Payment services licensing framework | Current | — | Botswana eligibility | **Not read for this version - pending validation** |
| **S12** | Reserve Bank of Malawi | Payment services licensing framework | Current | — | Malawi eligibility | **Not read for this version - pending validation** |
| **S13** | World Bank | World Development Indicators — DRC population and GDP per capita | Data year 2025 | [data.worldbank.org](https://data.worldbank.org/country/congo-dem-rep) | 112.8m population; $806.8 GDP per capita | Estimates subject to revision; GDP per capita sensitive to exchange-rate conversion |
| **S14** | BCEAO | UMOA monetary cooperation; EUR/XOF parity 655.957, no band; convertibility via the French Treasury operating account | Institutional constant | [bceao.int](https://www.bceao.int) | The corridor's FX and convertibility profile | Parity is a treaty arrangement, not a market outcome; a parity change is a tail risk, not a modelled scenario |
| **S15** | World Bank | Remittance Prices Worldwide — corridor France → Côte d'Ivoire | Q3 2025 (collected 24 Jul-2 Sep 2025) | [remittanceprices.worldbank.org](https://remittanceprices.worldbank.org/corridor/France/C%C3%B4te%20d%E2%80%99Ivoire) | Corridor average total cost 4.05%; fee EUR 5.19; FX margin 0.34%; total cost EUR 5.66; cheapest transparent quote 2.46% | **Samples EUR 140 and EUR 345, not EUR 200**; excludes non-transparent services; bank and MTO mix varies by quarter |
| **S16** | World Bank | Remittance Prices Worldwide, main report and annex Q3 2025 | Apr 2026 | [remittanceprices.worldbank.org](https://remittanceprices.worldbank.org/sites/default/files/2026-04/RPW_main_report_and_annex_Q325.pdf) | SSA average cost to send $200: 8.46%; digital-only MTO benchmark 3.54% | Regional averages mask wide corridor variation; the digital benchmark is a sub-index, not a guarantee of achievable pricing |
| **S17** | World Bank / IMF balance of payments | Personal remittances received, Côte d'Ivoire (WDI series BX.TRF.PWKR.CD.DT) | Series updated 11 Nov 2026; data year 2024 | [World Bank API](https://api.worldbank.org/v2/country/CIV/indicator/BX.TRF.PWKR.CD.DT?date=2023:2024&format=json) | $1.77bn received in 2024; $1.31bn in 2023 | National total, not corridor-specific; revised annually; understates informal flows |
| **S18** | European Union | Regulation (EU) 2024/886 on instant credit transfers in euro; Commission announcement of 9 Oct 2025 | 13 Mar 2024; 9 Oct 2025 | [eur-lex.europa.eu](https://eur-lex.europa.eu/eli/reg/2024/886/oj/eng) | Instant euro payments mandatory for euro-area banks; charge parity with standard transfers; free payee verification | Applies to euro-area banks from the stated dates; payment institutions have later deadlines (2027) |
| **S19** | European Payments Council | SEPA Credit Transfer Scheme Rulebook 2025, version 1.1 | 5 Oct 2025 | [europeanpaymentscouncil.eu](https://www.europeanpaymentscouncil.eu/sites/default/files/kb/file/2025-09/EPC125-05%202025%20SCT%20Rulebook%20version%201.1.pdf) | Maximum execution time of one banking business day after receipt | Cut-off times are out of scope of the rulebook and set by each provider |
| **S20** | — | Bank value dating and cut-off practice for EUR→XOF settlement | — | — | Timing assumption in §5.3 and §7.2 | **Assumption.** Must be replaced with a quoted cut-off and value-date schedule from the approved intermediary |

### 14.1 Withdrawn or corrected claims

| Claim | Origin | Disposition |
|---|---|---|
| Ivory Coast 4.2, Brazil 3.8, DRC 2.8, Botswana 1.9, Malawi 1.8 | v2 | Withdrawn. No method, no inputs. Replaced by the eight-criterion scored model in §3 |
| "Regulatory clarity" at 15% of market score | v2 | Removed. Regulation is a gate (§2) |
| Orange 45%, MTN 30%, Wave 20%, "Free Money" 5% | v2 | Withdrawn. "Free" is not an operator in Côte d'Ivoire; the fourth is Moov. Wave's share was materially understated |
| PIX "60%+ of digital payments" | v2 | Withdrawn. Correct figure: 55.2% of all payment transactions in H1 2026 [S9] |
| "Card penetration ~5%" in Côte d'Ivoire | v2 | Withdrawn as unsourced |
| "$5B+ monthly P2P crypto in Africa/LatAm" | v2 | Withdrawn as unsourced and unverifiable as stated |
| "Gambling industry $2B+ annual in emerging markets" | v2 | Withdrawn as unsourced |
| "Emerging market rails command 1.5-4% take rates" | v2 | Replaced by measured corridor cost (4.05%) and SSA/digital benchmarks [S15, S16] |
| "~90% of DRC transactions are cash" | v2 | Withdrawn as a number; retained as a qualitative description only |
| "DRC ~100M population" | v2 | Corrected to 112.8m [S13] |
| 105-point "100-point" scorecard | v2 | Corrected to a 100-point card with Scalability inside Technical Capability |
| Liquidity failure → "retry on backup PSP" | v2 | Reclassified as a treasury event with owners (§5.5) |
| "IC → France (remittance)" | v2 | Direction reversed: funded in France, paid out in Côte d'Ivoire |
| Pilot success ">95%" vs KPI ">90%" | v2 | Contradiction resolved: ≥92% pilot, ≥96% steady state (§11) |
| "Partner-only licence path; no licence needed at the gate" | v3 | **Partly corrected.** A Riverpe licence is not needed to start, but EPs and EMIs may not originate payments abroad, so an approved intermediary bank is mandatory in the settlement position [S4]. This adds a counterparty and raises minimum float |
| Minimum float $50,000 | v3 | **Revised to ~$57,000 (plan $60,000).** The bank operating balance and the three-day weekend gap were both missing |
| Payout fee "0.9-1.3% plus flat charge" | v3 | Revised downward to 0.85% blended, reflecting the PI-SPI price ceiling [S6]; still an assumption |
| Unit economics: 1.58% net | v3 | **Revised to 1.24%.** v3 omitted the funding-side collection fee; adding it raises cost per transaction from $2.84 to $3.52 |
| Break-even $1.14m/month | v3 | **Revised to $1.45m/month** as a consequence of the collection-fee correction |

---

## Appendix A. Quality-control self-assessment

The ten questions a reader will ask, answered against this document rather than against its intentions.

| # | Question | Answer | Where it is weakest |
|---|---|---|---|
| 1 | Can an investor see how the business earns money? | Yes: take rate on payout value, with each cost line and break-even volume (§6) | The take rate is benchmarked, not tested with customers |
| 2 | Can a provider see what is being proposed? | Yes: four named positions, volume expectations, settlement and float requirements (§7.1) | No provider has been asked whether they want it |
| 3 | Can a treasury professional see the liquidity requirement? | Yes: component build-up, ten-day model, cover metric, escalation ladder (§5) | Peak factor is assumed, not observed |
| 4 | Can an operations executive see how payments move? | Yes: ten-step lifecycle with timings and owners, plus failure scenarios (§7.2, §7.5) | Cut-offs and value dates are assumptions pending bank confirmation |
| 5 | Can a compliance professional identify the obligations? | Yes: RFE documentation, approved intermediary, licensing, screening (§2, §7.4) | Per-purpose documentation is bank practice and unverified |
| 6 | Can another analyst reproduce the scores? | Yes: weights, anchors, per-criterion inputs and contributions for every market (§3) | Four criteria rest on judgement, and the Brazil-CI gap is inside the error bars |
| 7 | Can the corridor realistically be executed? | Conditionally: the legal structure and float are specified and affordable | Access is untested, which is the whole of §4.1 |
| 8 | Are the financial assumptions defensible? | Mostly: each is ranged, labelled and tied to a benchmark | No quoted rate card exists; the conservative case does not break even at plausible pilot volume |
| 9 | Is every material claim supported? | Documentary claims yes; commercial claims no, and they are labelled | No primary interviews (§10) |
| 10 | Are the gaps acknowledged? | Yes: fourteen explicit gaps with closure dates (§13) | Closure depends on third parties responding |

**The honest summary.** This is a well-evidenced *plan* and an unvalidated *business*. The regulatory, settlement and pricing structure now rests on primary instruments; the partner relationships, quoted fees and customer demand do not exist yet. The next seven days of outreach are worth more than the next seven drafts.

---

*Riverpe Framework v4 - 20 November 2026. Supersedes v3. All figures are sourced, ranged, or labelled as assumptions; the interview register in §10 is empty and says so.*
