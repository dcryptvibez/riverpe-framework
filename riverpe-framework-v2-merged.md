# Riverpe Payment Supply Network Framework v2

**Prepared for:** Riverpe Founding Team
**Role:** Head of Growth Operations / Partnerships / Market Expansion
**Date:** August 2026
**Version:** Merged & Enhanced

---

## Executive Summary

> **The goal is not to collect PSP integrations. The goal is to build reliable payment corridors where customers can move money successfully, compliantly, and profitably.**

Riverpe is building local payment rails across emerging markets — the hardest, highest-value problem in global payments. The supply side of this business is a **payment supply network**: a curated, managed web of PSPs, banks, mobile money operators, and fintech partners that enable money to move in and out of every corridor Riverpe serves.

The core thesis: **payment infrastructure is a supply-constrained business**. The companies that win are not the ones with the best technology — they are the ones with the deepest, most reliable, most cost-efficient partner networks in the markets that matter. A strong payment network is built through operational excellence, not the number of integrations.

This document is the playbook for building that network from Day 1.

---

## 1. Market & Corridor Prioritization Framework

### The Mental Model: Corridor-First Thinking

Most payment infrastructure companies think in "markets." Riverpe should think in **corridors** — the specific route money travels from Point A to Point B. A corridor is defined by:

- **Origin market** (where money starts)
- **Destination market** (where money ends)
- **Payment method** (how money moves)
- **Use case** (why money moves)

Examples:
- Brazil → US (crypto off-ramp, iGaming payout)
- Ivory Coast → France (remittance, ecommerce)
- DRC → South Africa (B2B trade, payroll)
- Brazil → Argentina (cross-border ecommerce)

**Why this matters:** Two corridors in the same market can have completely different economics, risk profiles, and PSP requirements. A single "Brazil" strategy is meaningless — you need a Brazil→US strategy, a Brazil→Argentina strategy, and a Brazil domestic strategy.

### Market Scoring Framework

Before entering any market, score it across seven weighted dimensions:

| Factor | Weight | Key Questions |
|--------|--------|---------------|
| **Demand** | 25% | Are customers actively needing local payment rails? Failed payments? High-friction corridors? |
| **Payment Volume** | 20% | Is there enough transaction activity to justify entry? What's the TAM? |
| **Cross-Border Need** | 15% | Is there significant money flow in/out of this market? |
| **Regulatory Clarity** | 15% | Can Riverpe operate safely? What's the licensing path? |
| **PSP Availability** | 10% | Are quality payment partners available? How many viable options? |
| **Competition** | 5% | Is the market underserved? Can Riverpe differentiate? |
| **Revenue Potential** | 10% | Take rate × volume. What's the unit economics upside? |

### Customer Demand Signals

Before scoring any market, validate that real demand exists. Talk to 15–20 potential customers:

**Who is already trying to move money and can't?**
- Crypto exchanges operating in Africa/LatAm
- iGaming platforms expanding into emerging markets
- Remittance corridors with high failure rates
- Ecommerce platforms with cross-border sellers
- Forex platforms needing local settlement
- Global merchants with emerging market payouts

**What's the existing volume?** Pull data from:
- World Bank remittance flows ($50B+ annual into Sub-Saharan Africa)
- Chainalysis crypto volume reports ($5B+ monthly P2P in Africa/LatAm)
- SWIFT traffic reports
- Central Bank filings
- Gambling industry reports ($2B+ annual in emerging markets)

**What's the willingness to pay?** Emerging market rails typically command 1.5%–4% take rates. Validate that customers will pay Riverpe's margin on top of local PSP costs.

### Initial Market Prioritization

| Priority | Market | Score | Rationale | Entry Strategy |
|----------|--------|-------|-----------|----------------|
| **Tier 1** | **Ivory Coast** | 4.2 | Strong West African commercial hub. Mature mobile money (Orange, MTN, Wave). CFA franc peg = currency stability. Gateway to Francophone Africa. | Enter first. Prove Africa model. Expand to Senegal, Cameroon, Burkina Faso. |
| **Tier 2** | **Brazil** | 3.8 | Largest market. PIX dominates (60%+ of digital payments). Massive crypto/digital asset market. Mature fintech ecosystem. | Enter second. High regulatory bar — requires strong local PSP partner with BACEN relationships. Win through specialized corridors and underserved verticals. |
| **Tier 3** | **Congo (DRC)** | 2.8 | ~100M population. Massive untapped potential. Low competition. Growing digital adoption. | Enter third, after proving Africa model. High difficulty — liquidity, banking access, regulatory ambiguity. Requires strong local partner. |
| **Tier 4** | **Botswana** | 1.9 | Stable regulatory environment. Small market (~2.6M). Financial hub for Southern Africa. | Enter on-demand only. Niche corridors (Botswana→South Africa, Botswana↔Zimbabwe). |
| **Tier 5** | **Malawi** | 1.8 | Emerging digital payments. ~20M population. Volatile Kwacha. | Enter on-demand only. Thin liquidity, limited PSP depth. |

> **Note on sequencing:** The ChatGPT framework prioritizes Ivory Coast first (enter Africa first, prove the model, then expand). My original framework prioritized Brazil first (highest volume, fastest revenue). Both are defensible. The recommendation depends on Riverpe's existing customer base and investor thesis. If the core customers are in Africa, start with IC. If they're in LatAm or global, start with Brazil.

### Corridor Demand Heat Map

Once a market is selected, map the specific corridors:

```
IVORY COAST CORRIDORS
├── IC → France (remittance, diaspora)          HIGH DEMAND
├── IC → US (crypto, B2B)                       MEDIUM DEMAND
├── IC → Senegal (WAEMU trade)                  HIGH DEMAND
├── IC → China (import/export)                  MEDIUM DEMAND
└── IC → Nigeria (regional commerce)            GROWING

BRAZIL CORRIDORS
├── Brazil → US (crypto, iGaming, B2B)          HIGH DEMAND
├── Brazil → Argentina (ecommerce)              MEDIUM DEMAND
├── Brazil → Portugal/EU (remittance, trade)    HIGH DEMAND
├── Brazil → China (import payments)            HIGH DEMAND
└── Brazil → Mexico (LatAm expansion)           GROWING

DRC CORRIDORS
├── DRC → South Africa (trade, payroll)         HIGH DEMAND
├── DRC → UAE (mining, trade)                   MEDIUM DEMAND
├── DRC → Belgium (historical ties, remit)      MEDIUM DEMAND
└── DRC → China (import/export)                 HIGH DEMAND
```

---

## 2. Regulatory & Risk Assessment

### The Principle

> Payment infrastructure is built on trust. Regulatory assessment is not a checkbox exercise — it is a go/no-go gate that determines whether Riverpe enters a market at all.

I have seen companies burn 6–12 months and six figures on integrations only to discover they cannot legally operate. This framework prevents that.

### Market-Level Regulatory Checklist

For each market, evaluate:

**Licensing**
- Payment institution requirements
- Money transfer regulations
- E-money regulations
- Foreign exchange restrictions
- Timeline and cost to obtain (or operate under partner)

**Banking Environment**
- Which banks support fintech companies?
- Settlement capabilities and timelines
- Cross-border transfer restrictions
- Minimum reserve requirements

**Compliance Requirements**
- KYC requirements (thresholds, documentation)
- AML monitoring obligations
- Transaction reporting requirements
- Sanctions screening obligations
- Customer verification standards

### Payment License Requirements

| Market | License Required | Authority | Complexity | Path |
|--------|-----------------|-----------|------------|------|
| Brazil | Payment Institution License or partnership | BACEN | **High** | Partner (0 time) or direct (6–12 mo) |
| Ivory Coast | PSP license or licensed partner | BCEAO | **Medium** | Partner (0 time) or direct (3–6 mo) |
| Congo (DRC) | Unclear — framework underdeveloped | BCC | **High** | Partner only (regulatory risk) |
| Botswana | PSP license | Bank of Botswana | **Medium** | Partner or direct (3–6 mo) |
| Malawi | PSP license | Reserve Bank of Malawi | **Medium** | Partner or direct (3–6 mo) |

**Recommendation:** For the first 90 days, operate through licensed local PSP partners. Riverpe acts as technology/aggregation layer. Direct licensing becomes a Year 2 priority for high-volume markets.

### High-Risk Industry Evaluation

For industries like crypto, iGaming, and forex, PSP selection requires deeper screening:

**Key Questions:**
1. Does the PSP explicitly accept these industries?
2. Do their banking partners allow these transactions?
3. What risk controls exist for high-risk flows?
4. Have they experienced account freezes or compliance actions?
5. What transaction limits apply to high-risk merchants?
6. What's their dispute/chargeback handling capability?

> **Critical principle:** Never hide the crypto use case from PSP partners. Hidden crypto flows that surface during a regulatory audit will destroy the partnership and potentially Riverpe's ability to operate in that market.

**Crypto-specific considerations by market:**
- **Brazil:** Regulated under Law 14.478/2022. PSPs must report crypto transactions. Some accept, many won't.
- **Ivory Coast:** CFA franc convertibility constraints make crypto on/off-ramps complex. Yellow Card already serves this corridor.
- **Congo (DRC):** Minimal crypto-specific regulation, but AML concerns heightened.

**Action:** Maintain a distinct partner tier for PSPs that explicitly accept crypto-originated or crypto-destined funds. These partners command premium pricing and are harder to find.

### How Regulation Affects Partner Selection

Regulatory requirements create hard filters:

- Without proper licensing → **automatically disqualified**
- History of regulatory sanctions → **high-risk**, low-volume pilot only
- Compliance infrastructure quality → determines **scaling ceiling**
- Risk appetite → determines **which use cases** they support
- Banking relationship stability → determines **operational continuity**

> A PSP with cheap pricing but unstable banking relationships creates operational risk. Price is secondary to reliability.

---

## 3. Mapping the Payment Ecosystem

### The Principle

Before evaluating any specific PSP, build a complete map of how money flows within each target market. This is the foundational intelligence that drives partner selection.

### The Ecosystem Map (Layer Model)

**Layer 1: Banks**
- Settlement banks (where Riverpe's funds settle)
- Commercial banks (PSP's banking partners)
- Fintech-friendly banks (willing to work with payment companies)
- Foreign exchange providers

**Layer 2: Mobile Money & Wallets**
- Mobile operators (M-Pesa, Airtel, MTN, Orange, Wave)
- Digital wallets
- Alternative payment methods

**Layer 3: PSPs & Aggregators**
- Payment gateways
- Local processors
- Acquirers
- API providers

### Market-Specific Ecosystem Maps

**Ivory Coast:**
- Mobile money is king: Orange Money (~45%), MTN MoMo (~30%), Wave (~20%), Free Money (~5%)
- Banks: SGBCI (Société Générale), BICICI (BNP Paribas), Ecobank, NSIA Banke, Coris Bank
- PSPs: Flutterwave, FedaPay, CinetPay, ReliaMoney
- Card penetration ~5% — mobile money dominates
- CFA franc zone: payments within WAEMU (Senegal, Mali, etc.) are simpler; payments outside require EUR conversion

**Brazil:**
- PIX: 60%+ of all digital payments — instantaneous, 24/7, zero consumer cost
- Boleto Bancário: ~20% of e-commerce (cash-based, 3-day settlement)
- Cards: Elo (local), Visa, Mastercard
- PSPs: PagSeguro, Mercado Pago, StoneCo, EBANX, dLocal, Cielo, Rede
- Open Banking rolling out under BACEN — new partnership opportunities
- NuBank, Inter, C6 Bank reshaping banking landscape

**Congo (DRC):**
- Cash: ~90% of all transactions
- Mobile money: Airtel Money (largest), Orange Money, M-Pesa (limited)
- Banks: Rawbank, Equity BCDC, TMB (Trust Merchant Bank), FBNBank
- Very limited PSP infrastructure — this is where Riverpe creates value
- USD widely used alongside Congolese franc — dual-currency economy

### Partner Discovery Process

Six channels for finding potential partners:

1. **Industry Databases:** The Paypers PSP Directory, CB Insights, Fintech Maps, MRC member lists, GlobalData Fintech
2. **Fintech Associations:** Africa FinTech Network, ABFintech (Brazil), PASA, African Liberty Banking Association
3. **Regulatory Directories:** Central Bank licensed entity registers (BCEAO, BACEN, Bank of Botswana)
4. **Competitor Analysis:** Map who Flutterwave, Paystack (Stripe), dLocal, Chipper Cash, MFS Africa/onafriq, Yellow Card use as local partners — if they process real volume through a PSP, that PSP is proven
5. **Local Market Research:** 2–3 local consultants per market. $500–2,000 for structured market mapping. Local knowledge of informal networks and partnership culture cannot be replicated remotely
6. **Conferences & Network:** Africa Fintech Summit, Money20/20, Seamless Africa, Web Summit LatAm, DEVCON (crypto-specific)

---

## 4. PSP Partner Selection Framework

### The Discovery Funnel

```
Market Intelligence (100+ potential partners)
    ↓
Initial Screening (20–30 pass basic filters)
    ↓
Outreach & Discovery Calls (15–20 conversations)
    ↓
Detailed Evaluation (8–12 complete full assessment)
    ↓
Technical & Commercial Negotiation (4–6 in discussions)
    ↓
Partner Selection (2–3 signed per market)
```

### PSP Scorecard (100 Points)

Every PSP is scored out of 100 across five categories:

**Business Strength (20 points)**

| Criterion | 1 pt | 3 pts | 5 pts |
|-----------|------|-------|-------|
| Market Coverage | Single city | Multiple cities, one country | Nationwide + regional |
| Existing Clients | Unknown/few | 50+ active | 500+ with recognizable brands |
| Transaction Volume | <$100K/mo | $1M–10M/mo | $10M+/mo |
| Reputation | Complaints/disputes | Neutral, no red flags | Strong references |

**Technical Capability (20 points)**

| Criterion | 1 pt | 3 pts | 5 pts |
|-----------|------|-------|-------|
| API Quality | No API, manual | REST API, basic docs | Versioned API with SDKs |
| Integration Speed | 3+ months | 2–4 weeks | <1 week sandbox→prod |
| Reliability | Frequent downtime | 95%+ uptime | 99.5%+ with robust SLA |
| Settlement Infra | Manual, wire only | Automated, T+3+ | Real-time or T+1 |

**Payment Performance (25 points)**

| Criterion | 1 pt | 3 pts | 5 pts |
|-----------|------|-------|-------|
| Payment Methods | 1 method | 2–3 methods | Full stack |
| Success Rate | <85% | 90–95% | 97%+ |
| Transaction Limits | <$100/tx | $100–$5,000 | $5,000+ |
| Liquidity | Low, inconsistent | Moderate | Deep, always available |
| Settlement Speed | T+7+ | T+3 | T+0 or T+1 |

**Risk & Compliance (20 points)**

| Criterion | 1 pt | 3 pts | 5 pts |
|-----------|------|-------|-------|
| Compliance Maturity | No formal program | Basic KYC/AML | Dedicated team, automated |
| AML Controls | Manual, ad hoc | Some automated | Full monitoring + SAR |
| Licensing | Unlicensed/disputed | Licensed, no issues | Licensed + audit history |
| Risk Appetite | Very restrictive | Selective | Broad with due diligence |

**Commercial Terms (15 points)**

| Criterion | 1 pt | 3 pts | 5 pts |
|-----------|------|-------|-------|
| Pricing | Above market | At market | Below market/volume discounts |
| Revenue Share | No flexibility | Standard | Flexible, performance-based |
| Min. Commitments | High minimums | Moderate | No/low minimums |
| Scalability | Cannot handle growth | Moderate | Built for high-volume |

### Corridor PSP Structure

For each corridor, structure the PSP relationship as:

```
┌─────────────────────────────────────────────┐
│           PRIMARY PSP                        │
│  Best performance, main transaction volume   │
│  70–80% of corridor traffic                  │
├─────────────────────────────────────────────┤
│           BACKUP PSP                         │
│  Failover capacity, risk reduction           │
│  15–25% of corridor traffic                  │
│  Scales up if primary degrades               │
├─────────────────────────────────────────────┤
│           FUTURE PSP                         │
│  Competitive pricing negotiation leverage     │
│  Integrated but low volume                   │
│  Ready to activate if needed                 │
└─────────────────────────────────────────────┘
```

> **Never rely on one provider.** The initial corridor structure always includes primary + backup, with a future option for competitive pressure.

### PSP Scoring Example: Ivory Coast

| PSP | Business | Technical | Payments | Risk | Commercial | Total (/100) |
|-----|----------|-----------|----------|------|------------|-------------|
| PSP-A (Orange Money direct) | 18 | 12 | 18 | 16 | 10 | **74** |
| PSP-B (Local aggregator) | 12 | 16 | 22 | 12 | 12 | **74** |
| PSP-C (Pan-African fintech) | 16 | 19 | 14 | 19 | 10 | **78** |

**Decision:** PSP-C scores highest (technical + compliance). PSP-B is backup (mobile money depth). PSP-A is future option for Orange Money specifically.

### Industry-Specific PSP Identification

**Crypto:**
- Filter by explicit crypto-friendly policy — ask directly, verify with references
- Check PSP's correspondent bank is also crypto-tolerant (many PSPs accept crypto flows but their bank freezes the account)
- Verify compliance with travel rule and source-of-funds verification
- Look for existing crypto clients: Yellow Card, Bundle, Valr (Africa); Bitso, Mercado Bitcoin (Brazil)

**iGaming:**
- High-risk classification — requires explicit risk appetite confirmation
- Verify chargeback/dispute handling capabilities
- Check settlement speed — gaming operators need fast fund access
- Look for experience in gambling-adjacent markets (fantasy sports, lottery)

**Forex:**
- Handle frequent, high-value, cross-border transactions
- Check multi-currency account support or FX capabilities
- Verify licensing covers forex-related payment processing

---

## 5. Corridor Launch Strategy — First 90 Days

### The Principle

> Launch narrow, learn fast, expand methodically. One primary corridor. Not five markets simultaneously.

### Phase 1: Market Discovery (Days 1–30)

**Objective:** Select the first corridor based on validated demand.

**Actions:**
- Complete market scoring framework with actual data (not estimates)
- Conduct 10+ customer discovery calls to validate demand
- Confirm regulatory feasibility with local legal advisors
- Map payment ecosystem for top 2 candidate markets
- Identify initial PSP candidates (20–30 per market)
- Assess customer pull: which markets are customers already asking for?

**Deliverables:**
- Market scorecard with data-backed scores
- Customer demand validation report
- Regulatory assessment
- Payment ecosystem map
- Initial PSP longlist

**Decision:** Select first corridor.

### Phase 2: Partner Selection (Days 30–45)

**Objective:** Select primary + backup PSP partners.

**Actions:**
- Score top 10 PSP candidates per market using 100-point scorecard
- Shortlist 5–10 for detailed evaluation
- Begin outreach via warm introductions (investor network, local advisors, conference contacts)
- Conduct discovery calls with 8–10 PSPs
- Complete due diligence on top 4–6:
  - Verify licensing documentation
  - Request 2–3 client references
  - Compliance review (AML/KYC, transaction monitoring, regulatory history)
  - Technical assessment (API docs, sandbox access, uptime history)
  - Commercial discussion (pricing, settlement, minimums)
  - Legal review of partnership terms
- Negotiate commercial terms

**Deliverables:**
- PSP scorecards for all evaluated partners
- Due diligence reports with risk rating (Green/Yellow/Red)
- Signed partnership agreements with primary + backup

### Phase 3: Integration (Days 45–75)

**Objective:** Build working integrations with primary and backup PSPs.

**Actions:**
- Build PSP abstraction layer from Day 1 (adding new PSPs must be a config change, not a rewrite)
- API integration with primary PSP sandbox
- Implement payment flow: initiation → confirmation → settlement → reconciliation
- Error handling, retry logic, alerting
- Integration testing (unit, integration, end-to-end)
- Security review (data handling, PCI scope, encryption)
- Compliance approval
- Settlement testing

**Key Architecture Decision:**
> Build the PSP abstraction layer from Day 1. Every PSP integration goes through a common interface. This is non-negotiable for scalability. Without it, adding each new PSP is a 2–4 week engineering project. With it, it's a configuration change.

**Deliverable:** Two working integrations (primary + backup) in sandbox, ready for pilot.

### Phase 4: Pilot & Launch (Days 75–90)

**Objective:** Process real transactions, validate end-to-end, then scale.

**Actions:**
- Onboard 3–5 pilot customers per corridor
- Process pilot transactions at controlled volume ($1K–$10K)
- Monitor every transaction: success rate, settlement time, failure modes, cost
- Collect customer feedback
- Document all issues and performance gaps
- Reconcile all transactions manually

**Success Criteria:**
- Transaction success rate >95%
- Settlement within committed timeframe
- Zero compliance incidents
- Customer satisfaction: "better than what I had before"
- Cost per transaction within projected margins

**If pilot succeeds:**
- Open corridor for general onboarding
- Implement automated monitoring and alerting
- Establish daily reconciliation
- Set up partner performance dashboard
- Begin negotiating volume-based pricing
- Document operational playbooks

**Deliverable:** One live corridor with metrics dashboard. Begin scoping second corridor.

### Payment Failure Management

Failures are inevitable — the question is how fast you detect, diagnose, and resolve them.

| Failure Type | Response | Action |
|-------------|----------|--------|
| Technical (PSP downtime, API error) | Auto-retry on backup PSP | Alert PSP, log incident |
| Compliance (AML block, KYC issue) | Route to compliance team | No auto-retry |
| Liquidity (insufficient funds at PSP) | Retry on backup PSP | Alert PSP for replenishment |
| Customer (insufficient balance, wrong details) | Notify customer | No retry |

**Escalation Protocol:**
- Failure rate >5% on a corridor → **immediate review**
- Failure rate >10% → **corridor hold** pending investigation
- Repeated failures from same PSP → **volume shift** to backup

---

## 6. Payment Supply Network Management

### The Principle

> After launch, the network becomes a data business. The companies that win are those that combine local partnerships, compliance discipline, payment reliability, and intelligent routing.

### Partner Performance Monitoring

Every PSP partner is tracked against these metrics:

| Metric | Target | Red Flag | Action |
|--------|--------|----------|--------|
| Transaction Success Rate | >97% | <92% | Review with PSP, shift volume |
| Cost Per Transaction | Below market | >20% above | Renegotiate or shift |
| Settlement Time | T+1 or better | T+3+ consistently | Escalate, check cash flow |
| Failure Reasons | Mostly customer-initiated | Mostly PSP-side | Technical review |
| Customer Complaints | <0.5% of txns | >2% | Joint investigation |
| Volume Contribution | QoQ growth | Declining | Assess PSP market position |
| API Uptime | >99.5% | <98% | SLA enforcement |
| Dispute Resolution | <48 hours | >5 business days | Contractual enforcement |

### Weekly PSP Review

Every week, review:
- Success rate by PSP and corridor
- Failure reasons (categorized)
- Any downtime incidents
- Settlement delays
- Customer complaints
- Volume trends

### Monthly Partner Scorecard

Rank providers based on:
- Volume contribution
- Reliability
- Cost efficiency
- Risk profile
- Customer satisfaction

**Actions:**
- Increase volume with winners
- Renegotiate pricing with high performers
- Replace weak partners
- Add new providers when volume justifies

### Smart Payment Routing

Over time, build routing intelligence:

```
Example:
Transaction A (Brazil → US, $500, crypto-related):
  PSP-A success rate: 97% | Cost: 1.8% | Settlement: T+1
  PSP-B success rate: 88% | Cost: 1.5% | Settlement: T+2
  → Route to PSP-A (reliability > cost for this corridor)

Transaction B (IC → France, $200, remittance):
  PSP-A success rate: 95% | Cost: 2.2% | Settlement: T+1
  PSP-B success rate: 96% | Cost: 2.0% | Settlement: T+1
  → Route to PSP-B (similar reliability, lower cost)
```

**Routing strategies:**
- **Cost-based:** Lowest cost PSP for each payment type, amount, corridor
- **Reliability-based:** Highest success rate for that transaction type
- **Load balancing:** Distribute volume to maintain leverage + avoid single points of failure
- **Latency-based:** Fastest settlement for time-sensitive payments

### How Transaction Data Creates Competitive Advantage

The data advantage compounds over time:

1. **Pricing intelligence:** Know the true cost of every payment type in every corridor
2. **Reliability benchmarks:** Quantify which PSPs perform best for which payment types
3. **Market demand prediction:** Volume trends reveal growth, seasonality, emerging demand
4. **Risk modeling:** Failure patterns and fraud signals improve with volume
5. **Customer insight:** Payment behavior reveals new product opportunities

> Better success rates → more customers → more volume → stronger PSP relationships → better pricing → more customers. This is the flywheel.

### Adding & Removing Partners

**When to add a new PSP:**
- Volume exceeds a single PSP's comfortable capacity
- A new PSP offers meaningfully better pricing or capabilities
- Existing PSP shows reliability degradation
- Customer demand requires a payment method not currently supported

**When to remove a PSP:**
- Success rate consistently below 90%
- Compliance issues identified
- Settlement consistently delayed
- Pricing uncompetitive despite negotiation
- Banking relationship instability (account freezes)

**Always maintain at least one alternative before removing a partner.**

---

## 7. Growth & Partnership Operating Model

### Operating Cadence

**Weekly:**
- Monday: PSP performance review (30 min) — dashboard, red flags, follow-ups
- Wednesday: Market intelligence update (30 min) — regulatory changes, competitor moves, new proposals
- Friday: Corridor operations standup (30 min) — onboarding pipeline, integration progress, escalations

**Monthly:**
- PSP Scorecard Review (60 min) — updated scores, volume/revenue, cost analysis, partner health
- Corridor Expansion Review (60 min) — performance vs. projections, demand signals, resource allocation

**Quarterly:**
- New Market Evaluation (2 hrs) — market scoring refresh, competitive landscape, go/no-go for next market, resource planning

### Growth Operations KPIs

> **Philosophy:** Under-promise, over-deliver. Every number below is a minimum floor, not a stretch target. It's better to exceed a modest target than to miss an ambitious one. Public-facing projections should be even more conservative.

**Supply Growth**
| KPI | Q1 (Prove It Works) | Q2 (Prove It Scales) | H2 (Prove It's a Business) |
|-----|----|----|-----|
| Active PSP Partnerships | 1–2 | 3–4 | 6–8 |
| Live Corridors | 1 | 2 | 4 |
| Payment Methods Supported | 2 | 3–4 | 5–6 |

**Business Growth**
| KPI | Q1 (Prove It Works) | Q2 (Prove It Scales) | H2 (Prove It's a Business) |
|-----|----|----|-----|
| Monthly Payment Volume | $25–100K | $100–300K | $500K–2M |
| Monthly Revenue | $1–4K | $5–12K | $20–80K |
| Active Customers | 3–5 | 8–15 | 25–50 |

**Performance**
| KPI | Q1 (Prove It Works) | Q2 (Prove It Scales) | H2 (Prove It's a Business) |
|-----|----|----|-----|
| Transaction Success Rate | >90% (pilot phase) | >95% | >97% |
| Settlement Time | T+2–3 (pilot phase) | T+2 | T+1–2 |
| Cost Per Transaction | Baseline | -5% | -10% |

**Partnership Health**
| KPI | Q1 (Prove It Works) | Q2 (Prove It Scales) | H2 (Prove It's a Business) |
|-----|----|----|-----|
| Partner Retention | 100% | 100% | >90% |
| Pricing Improvements | 0 (building trust) | 1 PSP renegotiated | 2–3 PSPs renegotiated |
| Time to New Corridor | 60–90 days | 45–60 days | 30–45 days |

**Why these numbers:**
- Q1 is about proving one corridor works, not scaling. Most corridors take 2–4 weeks of customer discovery + 4–8 weeks of integration. Getting 1 corridor live in 90 days is a realistic win.
- $25–100K monthly volume in Q1 is honest for pilot customers. If it's higher, great — but don't plan around it.
- Revenue of $1–4K/month in Q1 covers 1–2 people's time, not the company's burn. That's fine — this is a supply-side investment.
- Success rate starts at >90% because pilot transactions will surface edge cases. >95% by Q2 is realistic after fixing those.
- Cost reduction of -5% to -10% is achievable through volume renegotiation. -20% requires 12+ months of leverage.

---

## 8. Final Perspective

If I joined Riverpe tomorrow, my first objective would not be building the largest PSP network.

**My objective would be building the most reliable payment network.**

The winning strategy:

```
Find demand → Validate regulation → Map ecosystem → Select quality PSPs →
Launch one corridor → Optimize through data → Expand regionally
```

**Key Principles:**
1. **Corridor-first thinking** — think in routes, not markets
2. **Reliability over scale** — one working corridor beats five broken ones
3. **Data compounds** — every transaction makes the network smarter
4. **Transparency with partners** — never hide the use case, especially crypto
5. **Redundancy is non-negotiable** — 2+ PSPs per corridor, always
6. **Depth before breadth** — prove one corridor, then replicate

**In 90 days:** One live corridor with 2 PSPs, pilot customers processing real transactions, playbook documented.
**In 6 months:** Two live corridors, 3–4 PSP partnerships, growing volume, unit economics validated.
**In 12 months:** Four corridors, 6–8 PSP partners, repeatable launch playbook, moving toward profitability.

The payment supply network is the moat. Everything else is a feature.

---

*Framework v2 — Merged and enhanced. August 2026.*
