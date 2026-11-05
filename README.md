# Digital Strategies Coursework (6BUIS019C)

Group coursework for **6BUIS019C Digital Strategy** (IIT / University of Westminster, 2026/27): a consulting report on **"Advancing Sustainability at IIT"**.

_Last updated: 5 November 2026_

## The assignment

| | |
|---|---|
| Module leader | Ms Shonali Aponso |
| Format | Group of 4; a single report submitted by one member via Blackboard |
| Weighting | 50% of the module (qualifying mark 30%) |
| Word limit | **3,250 words** (content may not be moved into images to get around it) |
| Due | **Tuesday 17 November 2026, 1:00 pm** |
| Referencing | Harvard or Vancouver |
| Learning outcomes | LO2 strategic analysis, LO3 digital strategy, LO4 technology assessment, LO6 teamwork |

### The client
We act as junior consultants for IIT's new **Sustainability Office**, which has a Head of Sustainability and a Digital Transformation Lead. The key facts from the brief:

- **Ambition:** Sri Lanka's leading sustainable technology campus by 2030
- **Budget:** a ring-fenced **LKR 80 million** over the first three years, delivered in phases and starting with a minimum viable set of tools. Savings are reinvested.
- **Delivery team:** one experienced developer plus final-year students. Existing IT and facilities should be reused.
- **Main problem:** smart meters and recycling exist, but the data isn't consolidated, there's no baseline, there's no end-of-life process for IT equipment, and club and lecturer activity isn't coordinated
- **Context:** a move to a new green campus in Ratmalana, currently under construction
- **Seven draft goals**, linked to the SDGs:
  1. Low-carbon campus
  2. Responsible IT and e-waste
  3. Circular, zero-waste campus
  4. Water and green spaces
  5. Sustainability in learning and research
  6. Inclusion and digital access
  7. Transparent governance (GRI report, and a UI GreenMetric or THE Impact Rankings entry by 2028)

### Report structure and marks

| Section | Weight | Key requirements |
|---|---|---|
| Introduction | 5% | Purpose, scope, HE sustainability context |
| Strategy Development Approach | 5% | How the team built the strategy (visual encouraged) |
| Strategic Analysis | 20% | **Exactly one** internal framework (10%) + **one** external framework (10%), each justified; ends with a GenAI box |
| Business Recommendations | 25% | Long list → criteria → focused programme (15%); MVP value proposition (5%); MVP business process map (5%); GenAI box |
| Digital Strategy | 30% | Application portfolio and architecture (15%); alignment with the initiatives (5%); implementation roadmap, evaluation, assumptions and risks (10%); one rejected "attractive" technology; GenAI box |
| Project Review for Professional Learning | 10% | Two strengths, two weaknesses, a per-member skills table |
| Report Presentation | 5% | ToC, page numbers, captions, references, author/contribution table |

The three **mandatory appendices** are A: Group Work Plan, B: Feedback Action Log (covering the three Strategic Review Meetings) and C: Individual Contribution Statements.

**GenAI boxes:** each is at most 250 words and gives two specific examples. If GenAI was used in a section and the box is missing, **that section gets no marks**.

## What's in this repo

| File | Section | What it contains |
|---|---|---|
| [`IIT_PEST_Technological_Factors - Thisen.docx`](IIT_PEST_Technological_Factors%20-%20Thisen.docx) | External analysis | PEST Technological factors T1–T5 |
| [`IIT_SWOT_Opportunities.docx`](IIT_SWOT_Opportunities.docx) | External analysis | SWOT Opportunities O1–O5, full version (~870 words) |
| [`IIT_SWOT_Opportunities_Table.docx`](IIT_SWOT_Opportunities_Table.docx) | External analysis | Same five opportunities as a table (~400 words) |
| [`IIT_McKinsey_7S_Whole_Organisation.docx`](IIT_McKinsey_7S_Whole_Organisation.docx) | Internal analysis | **Current 7S**: IIT as a whole, current vs desired state, enablers/barriers, org chart |
| [`IIT_McKinsey_7S_Internal_Analysis.docx`](IIT_McKinsey_7S_Internal_Analysis.docx) | Internal analysis | Older 7S, written as prose and focused on sustainability (superseded) |
| [`IIT_Organisational_Structure.png`](IIT_Organisational_Structure.png) | Internal analysis | IIT organisation chart (Figure 1 of the 7S) |
| [`IIT_Corporate_Structure_Analysis.docx`](IIT_Corporate_Structure_Analysis.docx) | Internal analysis | Mintzberg / Johnson et al. structure critique, 8-row rating table |
| [`IIT_Business_Recommendations.docx`](IIT_Business_Recommendations.docx) | Business Recommendations | Long list, scoring, programme, synergies, alternatives, MVP canvas, draft AI box |
| [`IIT_MVP_Process_Map.png`](IIT_MVP_Process_Map.png) | Business Recommendations | Swimlane map of the Data Hub's monthly cycle |
| [`6BUIS019C_Coursework_Specification_2026_Version-3 (1).pdf`](6BUIS019C_Coursework_Specification_2026_Version-3%20(1).pdf) | — | Assessment specification (annotated with who owns which part) |

According to the notes on the spec's marking scheme, Strategic Analysis is with Thisen and Ranuli, and the initial long list for Business Recommendations came from Diddy and Manthi. The Digital Strategy is planned for after Part 4.

## Strategic Analysis

### External: PEST (Technological)
| # | Factor | Classification | Impact |
|---|---|---|---|
| T1 | Shift to data-driven, connected building operations | Opportunity | High |
| T2 | Maturing, affordable clean energy (solar costs down ~90% since 2010; Sri Lanka rooftop solar >1,700 MW) | Opportunity | High |
| T3 | Spread of AI and advanced analytics (but data-centre energy demand is rising) | Opportunity with a threat | Medium |
| T4 | Fast device turnover and e-waste (Sri Lanka has no mandatory EPR scheme) | Threat with a circular opportunity | High |
| T5 | Growing connectivity, but ~40% of Sri Lankans are offline | Opportunity with a threat | Medium |

**Insight:** the technology is mature and affordable. The challenge is integration, data quality and responsible use, so IIT should integrate and measure first.

### External: SWOT Opportunities
| # | Opportunity | Impact |
|---|---|---|
| O1 | Growing visibility of sustainability rankings (THE Impact Rankings: 2,526 universities) | High |
| O2 | Student and employer demand for green skills | Medium–High |
| O3 | Mandatory SLFRS S1/S2 disclosure for Sri Lankan companies | Medium |
| O4 | Affordable clean energy and monitoring during the Ratmalana move | High |
| O5 | National policy momentum on climate and digital inclusion | Medium |

**Insight:** every opportunity runs into the same internal barrier: no consolidated data and no coordination.

### Internal: McKinsey 7S (current version)
The 7S is justified as purely internal (PEST covers external), whole-organisation, focused on how the elements fit together (Waterman, Peters and Phillips, 1980), and suited to checking whether IIT is ready for change. Each S compares IIT's current status with its target state: a leading regional institution and Sri Lanka's leading sustainable technology campus by 2030.

| Element | Main enablers (+) | Main barriers (–) |
|---|---|---|
| Strategy | 35-year reputation; own UGC-approved BBA; distinctive 2030 goal | Depends on partner degrees; growth spread thinly; goals have no baseline or costed plan |
| Structure | Fast top-down decisions; new Sustainability Office; Ratmalana redesign | Functional silos; units added ad hoc; Sustainability Office has no authority |
| Systems | ISO 9001 quality system; strong in-house IT | Multiple partner QA systems; no joined-up operational data; no public reporting |
| Shared values | Values lived through SDGP, placements, competitions | Eleven values is too many; sustainability isn't a core value |
| Style | Entrepreneurial; quick commitment (LKR 80m) | Activity not turned into measured results; relies on a few senior people* |
| Staff | Motivated students and staff; final-year capacity | Little spare staff time*; student turnover loses knowledge; tiny specialist teams |
| Skills | Software, AI, data science, analytics | Smaller research output*; no carbon accounting / GRI / e-waste expertise |

\* marked as an assumption in the document.

**Overall finding:** the soft elements (shared values, staff, skills) are fairly close to the target. **The biggest gaps are in Structure and Systems.** Closing them needs cross-department responsibilities and shared data, not just new technology.

### Internal: corporate structure analysis
In Mintzberg's (1979) terms, IIT is a **functional structure with a strong strategic apex**. Of the eight parts rated: **Strength** – support/specialist units, quality and compliance; **Mixed** – ownership and governance, top management, academic schools, partner university model, campuses; **Weakness** – the Sustainability Office. Its key line is that "Sustainability has an owner but no power". The proposed fix is a **cross-functional sustainability steering group**, chaired by senior management, with a data owner from each school, facilities, IT and students. This adds a matrix-style link across the silos without restructuring.

The org chart shows Informatics Group → Senior Management → Academic Schools, Student Services, Professional & Outreach, Corporate Functions, Sustainability Office and Campuses, with academic partners linked by dashed validation lines. Finance/HR/Admin, IT Services and Facilities & Estates are **assumed** (starred).

## Business Recommendations: "Measure, Manage, Engage, Share"

Ten initiatives were scored from 1 to 5 against weighted criteria: **Impact 30%, Fit with analysis 20%, Cost and feasibility 20%, Digital dependence 15%, Speed to value 15%**. Initiatives scoring **≥ 3.7** were selected.

| # | Initiative | Score | Timing | Goals |
|---|---|---|---|---|
| 1 | **Campus Sustainability Data Hub (MVP)** | 5.00 | Year 1 | 1, 3, 4, 7 |
| 2 | IT Asset Lifecycle and E-waste Tracker | 4.20 | Years 1–2 | 2, 3 |
| 3 | Smart Energy and Water at Ratmalana | 4.10 | Years 2–3 | 1, 4 |
| 4 | GreenIIT app with reuse marketplace | 4.00 | Years 2–3 | 3, 5 |
| 5 | Open Reporting, Rankings and Living Lab | 3.75 | Years 3–5 | 5, 7 |

**Not selected:** smart transport app (3.30), commercial sustainability suite (3.05), outreach platform (2.95), AI digital twin (2.90), blockchain green tokens (2.10).

- **Synergies:** the Data Hub feeds Initiatives 3–5. Reusable devices from the Asset Tracker go to DDL schools outreach. Savings from Initiatives 1 and 3 fund 4 and 5. The Living Lab adds student capacity.
- **Non-digital enabler:** the steering group, set up in Year 1.
- **Trade-offs:** building-level, opt-in data (Personal Data Protection Act No. 9 of 2022); a mobile-first app in English, Sinhala and Tamil; meters on a separate network.
- **Suggested goal changes:** use 2027 Data Hub data (or a declared estimate from bills) as the baseline; tag every device first; enter UI GreenMetric before THE.
- **MVP value proposition:** a Value Proposition Canvas (Osterwalder et al., 2014). The fit is strongest for the Head of Sustainability and facilities, and weakest for students until the app arrives in Year 2.
- **MVP process map:** a swimlane diagram with five lanes (meters, Data Hub, facilities, Sustainability Office, steering group/users) and two decisions ("data complete and valid?", "use above target?"). Monthly reporting feeds a quarterly target review.

## Key findings

- The technology is mature. The gap is integration and data (PEST T1, T2, T4).
- The strongest opportunities are rankings, green skills and the Ratmalana campus (SWOT O1, O2, O4).
- The biggest internal gaps are Structure and Systems (7S). Values, people and skills are strong.
- The Sustainability Office has responsibility but no authority, so it needs a steering group.
- IIT can't improve what it doesn't measure, so the Data Hub comes first.

## Open issues

1. **Only one framework per side is allowed.** The 7S doc pairs **7S (internal) with PEST (external)**, but the team has also been using SWOT, and its Opportunities are external material. The team needs to settle on one internal and one external framework, then make the other material fit or drop it. The recommendations draft currently cites PEST, SWOT and 7S together.
2. **Word count.** The analysis sections alone (PEST ~1,000 + SWOT + 7S ~1,050 + structure ~1,000) and the recommendations (~1,600) already exceed the 3,250-word limit for the whole report, before the Introduction, Approach, Digital Strategy (30%) and Project Review are written.
3. **"Four" vs five initiatives.** The spec's Digital Strategy wording mentions aligning with "the four business initiatives". The programme has five, so check this with the tutor or reduce the programme to four.
4. **GenAI boxes.** The recommendations box is a draft that the team must rewrite to describe what it actually did. Boxes are also needed for Strategic Analysis and the Digital Strategy, each with two specific examples.
5. **Digital Strategy not started.** It still needs the application portfolio and architecture, alignment with the initiatives, a roadmap, evaluation/KPIs, assumptions and risks, and one rejected technology. The AI digital twin or blockchain could serve as the rejected technology.
6. **Assumed parts of the org chart** need checking against official IIT information.
7. **Mandatory appendices A–C**, the author/contribution table and the Project Review still need to be put together.
8. **References** need merging into a single list. The citation labels differ between docs (e.g. `IIT (2026)` vs `IIT (2026a)`).

## Next steps

- [ ] Agree on the internal and external frameworks (7S + PEST, or SWOT)
- [ ] Agree the word split across sections and cut to fit 3,250
- [ ] Draft the Digital Strategy (portfolio, architecture, roadmap, risks)
- [ ] Rewrite the three GenAI boxes from the team's real use
- [ ] Write the Introduction, Strategy Development Approach and Project Review
- [ ] Compile Appendices A–C and the contribution table
- [ ] Merge everything into one report with consistent references, a ToC and figure captions
- [ ] Submit on Blackboard by **17 Nov 2026, 1:00 pm**
