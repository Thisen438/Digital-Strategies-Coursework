# Risks, technologies to reject, and lessons on implementing and evaluating IIT's digital campus sustainability programme

Research date: 5 November 2026. Context: IIT is a private higher-education institute in Colombo (hot, humid, cooling-dominated climate). It has smart meters but no consolidated data or baseline, a new campus under construction, LKR 80m over three years, one developer plus final-year students, and an engagement app that will process personal data. The core duties of Sri Lanka's PDPA start on 1 January 2027 (date taken from the brief, not re-verified here).

Conventions used below:
- **[primary text checked]** means I read the regulator's or standard's own text in this session.
- **[secondary]** means the source is press, a law firm, an aggregator or a vendor.
- **[flag]** marks something that is unverified or contested.
- The Inferences sections give my reasoning about IIT. They are not findings from the sources.

---

## 1. Campus/building digital twins: data and maturity requirements, costs, barriers and failure points

### Takeaway
Even in research, genuinely operational building digital twins (DTs) are rare and immature. A scoping review in *Energy and Buildings* (October 2026) screened 2,301 records and found only 37 real operational DTs. Nearly half of those stayed at the "descriptive" (dashboard) level, and only 27% reported any measured performance outcome. The campus exemplar (West Cambridge) depended on an as-is BIM/IFC model, BMS integration and dense IoT sensing at one-minute resolution. IIT has none of these yet. A DT is therefore premature for IIT. The useful part is the "DT-readiness" groundwork: data, metering and open-standard handover requirements for the new campus.

### Cited Findings
- **Most "digital twins" in the literature are not operational twins.** Al-Azba & Beitelmal (2026) screened 2,301 records from Scopus, Web of Science and IEEE Xplore, and only 37 studies met all criteria for an operational building DT. Many studies labelled as DTs were static BIM models, standalone energy simulations or hypothetical designs. The review appeared in *Energy and Buildings* 369, 117935 (October 2026), DOI 10.1016/j.enbuild.2026.117935. — [HBKU record of Al-Azba & Beitelmal 2026](https://elmi.hbku.edu.qa/en/publications/beyond-the-dashboard-architecture-maturity-and-performance-outcom/); [DOI](https://doi.org/10.1016/j.enbuild.2026.117935)
- **Prerequisites and maturity in the same review:**
  - All 37 operational DTs used real-time IoT data exchange, and 97.3% (36/37) integrated BIM.
  - 48.6% remained at the descriptive level.
  - 24.3% reached prescriptive maturity, meaning the twin drives control decisions.
  - Only 27% reported quantified performance outcomes. Prescriptive twins were four times as likely to report them, with examples of a 34% electricity-cost reduction and a 14.5% cut in HVAC power.

  — [Al-Azba & Beitelmal 2026, Energy and Buildings](https://elmi.hbku.edu.qa/en/publications/beyond-the-dashboard-architecture-maturity-and-performance-outcom/)
- **The campus exemplar.** Lu, Parlikad, Woodall et al. (2020) describe the West Cambridge campus DT (*Journal of Management in Engineering* 36(3)). It was built on an as-is IFC BIM model plus facilities-management systems and IoT sensors. It integrated data from 50 environmental sensors in one building (the Institute for Manufacturing) at one-minute granularity, in addition to BMS data, and it explored open standards such as IFC. The authors present their work as lessons learned and challenges from a research demonstrator, not a business-as-usual system. — [Lu et al. 2020, accepted manuscript (UCL Discovery)](https://discovery.ucl.ac.uk/10085012/3/Lu_Developing%20a%20Digital%20Twin%20at%20Building%20and%20City%20Levels_AAM.pdf); [Cambridge repository DOI](https://www.doi.org/10.17863/CAM.45198)
- **Techno-optimism warning (2026):**
  - Systematic reviews "consistently demonstrate that BIM use in FM is fragmented and immature", with weak alignment to facility managers' information needs and limited evidence of sustained operational value.
  - Models "frequently become static artefacts".
  - DT discourse shows "techno-optimism": benefits such as predictive maintenance and autonomous decision-making are "often overstated relative to current organisational capabilities and data readiness" (citing Lu et al. 2020 and Sacks et al. 2020).

  — [Frontiers in Built Environment (2026), "From BIM to digital twins in public healthcare facility management"](https://www.frontiersin.org/journals/built-environment/articles/10.3389/fbuil.2026.1828585/full)
- **Documented barriers.** A systematic review by Jahangir et al. (ITcon, March 2024; Aarhus University authors) identifies nine external and 31 internal barriers to DT adoption. These include high initial investment cost, a scarcity of skilled workforce, difficulties with data interoperability, and resistance to change within the organisation. — [Jahangir et al. 2024, ITcon](https://itcon.org/papers/2024_08-ITcon-Jahangir.pdf)
- **Data maintenance is a persistent barrier.** A 2026 systematic review in *Buildings* 16(6):1151 finds that "even with the initial setup of digital assets, gathering and maintaining accurate information remains challenging". It names the need for standardised data frameworks and interoperability as a significant barrier, because sources use "diverse data sources with incompatible formats". — [MDPI Buildings 2026, 16(6):1151](https://www.mdpi.com/2075-5309/16/6/1151)
- **Capabilities do not yet transfer between sites.** A 2026 ITcon systematic review of operational DTs (Elias, Hutchins & Issa) concludes that the field has demonstrated meaningful operational capabilities but "has not yet assembled them into coherent architectures that transfer across sites". — [ITcon 2026, paper 43](https://itcon.org/paper/2026/43)
- **Large-scale deployment is unresolved.** A 2026 PRISMA-ScR scoping review in *Sustainability* 18(12):5869, on DT architectures for energy-efficient buildings and renewable energy communities, reports "unresolved structural challenges for large-scale real-world deployment". [flag: I took the author attribution (Cumo et al.) from a search summary.] — [MDPI Sustainability 2026, 18(12):5869](https://www.mdpi.com/2071-1050/18/12/5869)
- **A further review exists but its content was not read.** Ghansah (2025) published a systematic review of DT enablers, applications and challenges at the facility-management stage in *Smart and Sustainable Built Environment* 14(4):1194–1229. I verified only the citation; the content was behind a paywall. — [Emerald](https://www.emerald.com/sasbe/article/14/4/1194/1259577/Digital-twins-for-smart-building-at-the-facility)
- **"Smart campus" is still mostly concept, not practice.** Polin, Yigitcanlar, Limb & Washington (2023) ran a PRISMA review in *Buildings* 13(4):891, narrowing 3,601 articles to 123. They found "little evidence of a comprehensive real-world application of the smart campus" across the society, economy, environment and governance domains, which "highlights the infancy of the current conceptualization and practice". — [MDPI Buildings 13(4):891](https://www.mdpi.com/2075-5309/13/4/891)
- **Poor interoperability costs owners most.** NIST GCR 04-867 estimated that inadequate interoperability cost US capital facilities $15.8bn in 2002. Owners and operators bore $10.6bn of that, about two-thirds. The study covered design, construction and operations and maintenance, and its authors call the estimate conservative. — [NIST GCR 04-867](https://www.nist.gov/publications/cost-analysis-inadequate-interoperability-us-capital-facilities-industry)

### Inferences
- IIT meets none of the published prerequisites for an operational DT: consolidated time-series data, validated meter hierarchy, as-built BIM/IFC, integrated BMS and dense sensing. At best, a DT built now would be "descriptive", which a conventional 2D dashboard delivers at a fraction of the cost and risk.
- The cheap, high-value move is to write DT-readiness into the new-campus construction and handover contracts:
  - as-built BIM/IFC with an asset register;
  - a BMS on open protocols with exportable point lists;
  - end-use sub-metering (chillers/AHUs, lighting, plug loads, PV);
  - a consistent point-naming/metadata standard (see section 6);
  - full commissioning.

  This keeps a DT option open for year 3 or later without spending the LKR 80m now.
- A stage-gate for reconsidering a DT later: at least 12 months of clean interval data, a documented decision that needs simulation or "what-if" analysis (for example chiller-plant sequencing), and a named owner with skills to keep the model current. The literature's recurring failure is a model that becomes a "static artefact".

### Gaps
- **Costs.** I found no credible published cost figures (capex or opex) for campus or building DTs. The reviews cite "high initial investment cost" only qualitatively, and vendor pricing is opaque. The report should not quote a DT cost number.
- I could not retrieve the full list of challenges in Lu et al. (2020) or the barrier ranking in Ghansah (2025).
- I found no DT case study at a South Asian or tropical higher-education campus.

---

## 2. Blockchain for campus energy/carbon credits or token rewards: real benefit versus a conventional database, energy use, criticisms

### Takeaway
The standard decision frameworks (Wüst & Gervais 2018; NIST IR 8202) say a conventional database is preferable where there is a single writer or a trusted operator. That is exactly IIT's position as the owner of its own reward scheme and meters. Reviews of energy-sector blockchain describe most initiatives as early-stage, facing scalability, privacy, security and billing challenges. Carbon-credit tokenisation was blocked by the largest registry (Verra) in May 2022. Energy use is only a decisive objection for proof-of-work chains: Ethereum's 2022 move to proof-of-stake cut its electricity use by about 99.99%. The stronger case against blockchain for IIT is that it adds complexity without solving a problem IIT has.

### Cited Findings
- **Energy-sector blockchain is largely pre-mainstream.** Andoni et al. (2019) reviewed 140 blockchain research projects and start-ups in energy and mapped them by activity, platform and consensus. They discuss the barriers the technology must overcome to move beyond hype into mainstream adoption (*Renewable and Sustainable Energy Reviews* 100:143–174, DOI 10.1016/j.rser.2018.10.014). — [RePEc record](https://econpapers.repec.org/RePEc:eee:rensus:v:100:y:2019:i:c:p:143-174); [Heriot-Watt repository](https://researchportal.hw.ac.uk/en/publications/blockchain-technology-in-the-energy-sector-a-systematic-review-of/)
- **Smart contracts in energy are still early-stage.** Kirli et al. (2022, *RSER* 158) reviewed 178 peer-reviewed publications and 13 innovation projects. They conclude that use in the energy sector "is still in its early stages as there are many open challenges related to security, privacy, scalability and billing". — [TU Delft repository](https://repository.tudelft.nl/record/uuid:93734dee-5bb6-42a8-be7f-434622e60ef2)
- **The decision logic favours a database for IIT's situation.** Wüst & Gervais, "Do you need a blockchain?" (IACR ePrint 2017/375; IEEE CVCBT 2018), set out these rules:
  - With a single writer, "a regular database is preferred", because a blockchain gives no additional guarantees and a database performs better.
  - Where an always-online trusted third party exists, writes can be delegated to it.
  - A permissionless blockchain fits only when there are multiple, unknown, mutually distrusting writers and no trusted third party.

  — [IACR ePrint 2017/375](https://eprint.iacr.org/2017/375)
- **Critique of that framework.** David Gerard (February 2018) argues that the paper is "a bit overenthusiastic about blockchains". It ignores non-blockchain append-only ledgers such as Git, and the trusted-third-party condition is usually met in practice. [secondary: commentator blog] — [David Gerard 2018](https://davidgerard.co.uk/blockchain/2018/02/10/do-you-need-a-blockchain-probably-less-than-wust-and-gervais-think-you-do/)
- **NIST's overview.** NIST IR 8202, *Blockchain Technology Overview* (Yaga, Mell, Roby & Scarfone), was released as a draft in January 2018 and finalised in October 2018. NIST's announcement said it aimed to "go beyond the hype". The report includes a decision flowchart for judging whether a blockchain suits an application. [flag: a secondary source places it as Figure 6; I did not view the figure.] — [NIST IR 8202 (DOI)](https://doi.org/10.6028/NIST.IR.8202); [NIST news, January 2018](https://www.nist.gov/news-events/news/2018/01/nist-report-blockchain-technology-aims-go-beyond-hype)
- **Energy use depends on the consensus mechanism.**
  - The Crypto Carbon Ratings Institute estimates that the Ethereum Merge (September 2022) cut the network's electricity use by 99.988% and its emissions by 99.992%, from about 22.9 TWh/yr to about 2,600 MWh/yr. — [CCRI Ethereum report 2022](https://carbon-ratings.com/dl/eth-report-2022)
  - The Cambridge Centre for Alternative Finance (CCAF) reports a drop of about 99.99%. — [CCAF Ethereum Merge page](https://ccaf.io/cbnsi/ethereum/ethereum_merge)
  - [flag: some media quote 99.95%; the CCRI and CCAF figures are the primary estimates.]
- **Carbon-credit tokenisation was blocked by the main registry.** On 25 May 2022, Verra stopped allowing tokenisation based on retired credits. This was the model used by Toucan Protocol's "Base Carbon Tonne". Verra said it would block retirement requests linked to tokenisation, while exploring "immobilising" credits within its registry instead. BCT had fallen from US$8.31 (end of November 2021) to US$2.14 at the time of reporting. — [S&P Global, 25 May 2022](https://www.spglobal.com/energy/en/news-research/latest-news/energy-transition/052522-as-verra-halts-tokenization-of-carbon-credits-toucan-vows-to-keep-web3-ethos-alive); [carboncredits.com](https://carboncredits.com/verra-suspension-carbon-credits-proposes-immobilizing-credits); [DLA Piper, September 2022](https://www.dlapiper.com/en/insights/publications/2022/09/verra-contemplates-future-of-crypto-instruments-and-vcus)
- **Financial incentives can backfire.** In a meta-analysis of 156 field trials, "pecuniary feedback and incentives lead to a relative increase in energy usage rather than induce conservation". This is relevant to monetisable token rewards. — [Delmas, Fischlein & Asensio 2013, Energy Policy 61:729–739](https://www.ioes.ucla.edu/wp-content/uploads/2017/07/2013-Delmas-Fischlein-Asensio-EnergyPolicy.pdf)

### Inferences
- **IIT's case fails the decision test.** IIT is the single trusted operator of its meters and of any points scheme, and there is no multi-party market (it has one owner and one utility connection). A relational database with an append-only audit table gives the integrity needed at negligible cost, using skills the developer and students already have. Optionally, the audit rows can be hash-chained for tamper evidence.
- **Immutability conflicts with data-subject rights.** An immutable ledger of personal engagement data would sit badly with data-subject rights such as rectification and erasure, and with retention limits. [flag: inference; I did not check the specific PDPA sections.] This adds PDPA risk with no offsetting benefit.
- **Token rewards that can be traded or cashed** add financial-regulatory questions and may, on the Delmas finding, undermine intrinsic motivation. Non-monetary recognition (badges, departmental league tables, prizes funded from savings) avoids both problems.
- **Campus peer-to-peer energy trading** is out of scope for an institution with a single owner and connection point.

### Gaps
- I found no peer-reviewed controlled evaluation of blockchain-based campus sustainability token schemes.
- Sri Lanka's regulatory position on crypto-tokens (for example Central Bank of Sri Lanka warnings) was not verified.
- The current Cambridge Bitcoin Electricity Consumption Index figure was not retrieved, so I do not cite a Bitcoin TWh number.

---

## 3. Facial recognition for attendance or payments in schools and universities: regulatory actions, privacy concerns, relevance under data protection laws

### Takeaway
Regulators and courts have consistently found facial recognition (and other biometric identification) in education disproportionate:
- **Sweden (2019):** a GDPR fine (SEK 200,000) for a three-week, 22-student attendance trial. Consent was invalid because of the power imbalance, less intrusive means existed, and there was no DPIA or prior consultation.
- **France:** a CNIL opinion (October 2019), then annulment by a court (February 2020).
- **Poland:** a fine for fingerprint use (March 2020).
- **UK:** ICO findings against North Ayrshire (January 2023) and a reprimand to Chelmer Valley High School (July 2024).
- **New York State:** a statewide school ban (September 2023).
- **EU:** the AI Act has banned emotion recognition in education since 2 February 2025.

Sri Lanka's PDPA classes biometric data as a special category and requires impact assessments for systematic monitoring or special-category processing. Facial recognition attendance should therefore be explicitly rejected by IIT.

### Cited Findings
- **Sweden: IMY decision DI-2019-2221, 20 August 2019** [primary text checked]
  - The Secondary Education Board of Skellefteå used facial recognition in a trial at Anderstorp Secondary School to monitor the attendance of 22 students over three weeks.
  - It was fined SEK 200,000 for breaching three sets of provisions:
    - Article 5, by processing data "more intrusive as regards personal integrity and encompass[ing] more personal data than is necessary";
    - Article 9, by processing biometric data "without having a valid derogation";
    - Articles 35–36, by failing to meet the impact-assessment requirements and failing to consult the authority beforehand.
  - On consent: "the students are in a position of dependence which results in a substantial imbalance … consent cannot constitute a legal basis."
  - On proportionality: "Attendance monitoring can be carried out in other ways which involve less infringement of the students' integrity", so camera-based facial recognition was "disproportionate".
  - The Board's justification was that traditional registration "takes ten minutes per lesson" and facial recognition would "save 17 280 hours" per year.

  — [IMY (formerly Datainspektionen) decision DI-2019-2221, English version](https://www.imy.se/globalassets/dokument/beslut/facial-recognition-used-to-monitor-the-attendance-of-students.pdf); context in [IAPP analysis (2019)](https://iapp.org/news/a/how-to-interpret-swedens-first-gdpr-fine-on-facial-recognition-in-school)
- **UK: ICO letter to North Ayrshire Council (published January 2023)**
  - The council's facial recognition system for canteen payments in nine schools "is likely to have infringed data protection law".
  - The infringements covered transparency and the right to be informed, and insufficient information was given for children and parents to consent.
  - The ICO recommended improvements on data minimisation and accuracy, noting heightened risk with children's data.
  - The council stopped using the system after the ICO's interest in October 2021 and deleted the biometric data.

  — [ICO letter appendix](https://cy.ico.org.uk/media2/migrated/4023847/ico-letter-to-nac-appendix.pdf); [Biometric Update, February 2023](https://www.biometricupdate.com/202302/scottish-schools-canteen-facial-recognition-likely-infringed-gdpr-ico)
- **UK: ICO reprimand to Chelmer Valley High School, Essex (23 July 2024)**
  - The school introduced facial recognition for canteen payments in March 2023 without the legally required DPIA.
  - It wrongly relied on assumed (opt-out) consent.
  - The ICO issued five recommendations.
  - Computer Weekly reported the supplier as CRB Cunninghams. [secondary]

  — [ICO press release](https://ico.org.uk/about-the-ico/media-centre/news-and-blogs/2024/07/essex-school-reprimanded-after-using-facial-recognition-technology-for-canteen-payments); [Computer Weekly](https://computerweekly.com/news/366596461/ICO-reprimands-Essex-school-for-illegal-facial-recognition-use)
- **France: CNIL opinion (29 October 2019) and Administrative Court of Marseille (27 February 2020)**
  - The CNIL found that facial-recognition access gates trialled at two high schools in Nice and Marseille (Provence-Alpes-Côte d'Azur region) failed the GDPR's proportionality and data-minimisation principles, because less intrusive means such as badges exist.
  - The court then annulled the regional council's decision authorising the trial. It was described as the first French court decision applying the GDPR to facial recognition.

  [secondary; I did not read the primary CNIL notice or judgment] — [Biometric Update, October 2019](https://www.biometricupdate.com/201910/french-privacy-regulator-finds-facial-recognition-gates-in-schools-illegal); [IAPP, February 2020](https://iapp.org/news/a/french-court-rules-against-schools-school-facial-recognition-plans/); [Statewatch, March 2020](https://statewatch.org/news/2020/march/first-success-against-facial-recognition-in-france)
- **Poland: UODO fine on a Gdańsk primary school (March 2020)**
  - PLN 20,000 fine for processing fingerprint data of 680 children at the canteen entrance without a legal basis.
  - Alternatives (electronic cards, or giving a name and contract number) already existed.
  - Pupils without biometrics had to wait until those with biometrics had entered, which UODO held to be unjustified unequal treatment.
  - The school was ordered to delete the data.

  — [EDPB national news, 2020](https://www.edpb.europa.eu/news/national-news/2020/fine-processing-students-fingerprints-imposed-school_en)
- **United States: New York State Education Department determination (27 September 2023)**
  - The Commissioner prohibited schools from purchasing or using facial recognition technology.
  - This followed an August 2023 state Office of Information Technology Services report that found the risks outweighed the benefits.
  - Other biometrics (for example fingerprints) remain allowed, provided privacy, civil-rights and parental input are considered.

  — [NYSED press release](https://www.nysed.gov/news/2023/state-education-department-issues-determination-biometric-identifying-technology-schools); [WSKG, 28 September 2023](https://www.wskg.org/news/2023-09-28/new-york-bans-facial-recognition-in-schools-after-report-finds-risks-outweigh-potential-benefits)
- **EU AI Act (Regulation (EU) 2024/1689)**
  - Article 5(1)(f) prohibits AI systems that infer emotions of people in workplaces and education institutions from biometric data, except for medical or safety reasons. It has applied since 2 February 2025.
  - Annex III point 3 lists high-risk education uses: admission or assignment to institutions, evaluating learning outcomes, and monitoring prohibited behaviour during tests.
  - [flag: sources conflict on when the Annex III high-risk obligations apply; several report postponement to 2 December 2027.]

  — [Future of Privacy Forum analysis](https://fpf.org/blog/red-lines-under-eu-ai-act-unpacking-the-prohibition-of-emotion-recognition-in-the-workplace-and-education-institutions/)
- **Sri Lanka: PDPA No. 9 of 2022**
  - "Special categories of personal data" include biometric data, alongside racial or ethnic origin, health, genetic data and others.
  - Section 24 requires a personal data protection impact assessment for:
    - systematic and extensive evaluation of personal data or special categories, including profiling;
    - systematic monitoring of publicly accessible areas or telecommunication networks;
    - processing of special categories on a prescribed scale.
  - The Data Protection Authority issued draft PDPIA regulations for public consultation.

  [secondary for the Act summary; I did not confirm whether the PDPIA regulations are final] — [DLA Piper, Data Protection Laws of the World: Sri Lanka](https://www.dlapiperdataprotection.com/?c=LK&t=law); [DPA Sri Lanka draft PDPIA regulations](https://dpa.gov.lk/guid/DPA%20Final%20Draft_PDPIA%20Regulations-for%20Public%20ConsultationV%201.0.pdf)

### Inferences
- **The core reasoning transfers to IIT.** IIT is private, so it cannot rely on the "public interest task" basis Skellefteå argued. The power imbalance the Swedish authority relied on (students depend on the institution for attendance records, grades and progression, and staff depend on it for employment) applies equally, which makes consent fragile. A legitimate-interest or necessity argument would struggle because less intrusive alternatives exist: QR/NFC check-in, LMS login, roll call, ID cards.
- **The benefit side is negligible for sustainability.** Attendance is not a sustainability KPI, and Skellefteå's "time saved" justification was rejected as disproportionate. Recommend a written "no biometric identification and no emotion recognition" principle in the engagement app's design charter and DPIA.
- **Occupancy for HVAC control** can use non-identifying sensing: CO₂, PIR, people-counters without image retention, or aggregated Wi-Fi association counts. Even aggregated Wi-Fi analytics should go through a DPIA, because they can amount to "systematic monitoring" under PDPA s.24.

### Gaps
- I found no Sri Lankan DPA guidance specific to biometrics in education, and no Sri Lankan enforcement yet. Core duties begin 1 January 2027 (per the brief).
- A 2025 PDPA amendment (reported as Act No. 22 of 2025) appears in a Wikipedia mirror but was not verified against the gazette.

---

## 4. Computer-vision "smart bins": evidence of cost and benefit versus simple weighing and audits

### Takeaway
Independent evidence that computer-vision (CV) sorting bins beat simple methods is thin:
- Lab and student prototypes report 84–96% classification accuracy, but struggle with transparent plastics and glass.
- I found no independent cost data.
- The best-evidenced AI waste field trial (East Lansing, USA) got its 23% contamination reduction from feedback postcards to households, with AI used only as the inspection tool.
- Fill-level sensor savings mostly come from correcting over-frequent collection schedules.

By contrast, simple food-waste measurement with scales and staff action returned about 7:1 (benefit to cost) across 114 restaurants. For IIT, start with periodic waste audits (characterisation), weighing, signage and feedback.

### Cited Findings
- **Prototype accuracy.**
  - An Arizona State University edge-AI bin prototype (2025) reached 84% overall accuracy with 310 ms inference on a Raspberry Pi 5. Transparent plastics and glass were weak points. It was a student research project, not a field trial. — [ASU FURI report (2025)](https://forge.engineering.asu.edu/wp-content/uploads/2025/06/Dalbins_FURI.pdf)
  - A UCL mechanical-engineering student design project (2020) reports material classification above 96% accuracy, with no deployment or cost data. — [UCL AutoSort 2020](https://mecheng.ucl.ac.uk/gdp/mechanical-engineering-group-design-projects/sustainable-design/ucl-autosort-team-2020)
- **Field trial where the benefit came from feedback (East Lansing, Michigan).**
  - A 24-week pilot from September 2022 used AI cameras on collection trucks to flag contaminated carts; flagged households received educational postcards.
  - Those households cut contamination by 23% and set out carts 45% more often than a control group.
  - Postcards were sent in error 0.5% of the time.
  - Ohio State University ran the statistical analysis.

  — [Michigan EGLE, 11 April 2024](https://www.michigan.gov/egle/newsroom/mi-environment/2024/04/11/east-lansing-finds-an-intelligent-solution-to-household-recycling-errors); [WKAR, 24 February 2024](https://www.wkar.org/wkar-news/2024-02-24/ai-boosts-recycling-efforts-in-east-lansing)
- **Campus robotic sorter with no published results.** The rStream unit at UMass Amherst can process up to one ton per hour. I found no published contamination or cost results. — [Recycling Today](https://www.recyclingtoday.com/news/rstream-pilots-auditpro-technology-for-sorting-waste-and-recyclables)
- **Fill-level sensors: savings mainly from fixing schedules.**
  - Prague 11 (18-month pilot, 199 slow-filling glass containers): collections fell to 35% of the previous total, saving CZK 2.88m against a one-time setup cost of CZK 0.8m. [secondary press] — [Expats.cz](https://www.expats.cz/czech-news/article/prague-s-smart-glass-bins-cut-collections-by-two-thirds-save-millions)
  - Cambridge City Council (UK) trialled 267 sensors. Its scrutiny report notes early evidence of savings from routing, and that data show many paired bins are underused, with some taking over 100 days to fill. — [Cambridge City Council scrutiny report](https://democracy.cambridge.gov.uk/documents/s71219/Scrutiny%20Report%20on%20Task%20and%20Finish%20work%20for%20Litter%20Strategyv4.pdf)
- **Vendor claims are self-reported.**
  - Sensoneo reports a 30% collection-cost reduction in Nitra. — [Sensoneo case study](https://www.casestudies.com/company/sensoneo/case-study/nitrianske-komunalne-sluzby-customer-case-study)
  - Victor Stanley claims 20–40% savings and declined to disclose bin costs. — [Technical.ly](https://technical.ly/startups/victor-stanley-smart-trash-bin.md)
  - [flag: both baselines are usually fixed schedules.]
- **Simple measurement pays (Champions 12.3, 2019).**
  - Across 114 restaurant sites in 12 countries, the average benefit-cost ratio was 7:1.
  - 76% of sites recouped their investment within the first year and 89% by year two.
  - Kitchen food waste fell by an average of 26% within a year.
  - The successful measures were measuring and monitoring food waste, staff training on handling and storage, and menu redesign.

  — [Champions 12.3 release (2019)](https://champions123.org/release-new-report-finds-restaurants-save-significant-money-fighting-food-waste); [WRI/WRAP report PDF](https://food.ec.europa.eu/system/files/2021-04/fw_lib_wri-business-case-restaurants_2019.pdf)
- **Broader food-waste dataset.** An earlier dataset of about 1,200 business sites across 700 companies found that half saw a 14:1 or greater return. It is not restaurant-specific. — [WRI (2017)](https://www.wri.org/insights/numbers-business-case-reducing-food-loss-and-waste)
- **The campus audit approach.** Smyth, Fredeen & Booth (2010) treat a waste characterisation (audit) study as the first step in campus waste-management planning at the University of Northern British Columbia (*Resources, Conservation and Recycling* 54(11):1007–1016, DOI 10.1016/j.resconrec.2010.02.008). [I verified the citation and approach, not detailed results.] — [IDEAS/RePEc](https://ideas.repec.org/a/eee/recore/v54y2010i11p1007-1016.html)

### Inferences
- **For a single compact campus, the pattern of benefits points to low-tech first:**
  - The measurable gains came from feedback (East Lansing postcards), measurement plus staff action (Champions 12.3), and schedule correction (Prague, Cambridge).
  - A quarterly waste audit run as a student practical, scales at canteen and food outlets with digital entry into the same data platform, and better bin signage capture most of the value.
- **CV bins carry extra burdens:**
  - unknown capex and subscription costs;
  - camera maintenance in heat and humidity (fogging, insects, dust);
  - connectivity requirements;
  - privacy: cameras in public areas may capture people, which raises a PDPA DPIA question.
- **Sensors only if the hauler contract allows it.** Fill-level sensors are worth considering only if IIT's waste contract is priced per collection and bins are demonstrably collected half-empty. A two-week manual fill log by cleaning staff can test that first.

### Gaps
- I found no independent cost data for commercial CV recycling bins, and no peer-reviewed RCT of CV bins on a campus.
- The Ohio State peer-reviewed paper on East Lansing was described as "in the works". I did not locate it.

---

## 5. AI forecasting/optimisation for building energy: data prerequisites and the energy footprint of AI

### Takeaway
Data-driven forecasting works when there is long, clean, granular metered data plus metadata and weather. The ASHRAE Great Energy Predictor III competition (2,380 meters, 1,448 buildings) found that preprocessing and feature engineering mattered most, and that winners used gradient-boosting ensembles rather than exotic AI. IIT does not yet have a clean history, and the new campus has none at all.

The AI footprint concern applies mainly to large general-purpose and generative models. Task-specific models are orders of magnitude cheaper to run, and a gradient-boosting forecaster for a campus is trivial in energy terms.

### Cited Findings
- **Macro framing (IEA *Energy and AI*, 2025).** About 300 TWh of potential building savings from AI, against data-centre electricity of 415 TWh in 2024 rising to about 945 TWh by 2030. [figures as supplied in the brief; not re-fetched in this session] — [IEA, Energy and AI (2025)](https://www.iea.org/reports/energy-and-ai)
- **What wins in practice (ASHRAE GEPIII).** Miller et al. (2020), *Science and Technology for the Built Environment* 26(10):1427–1447:
  - The competition ran on Kaggle in late 2019, using 2,380 meters from 1,448 buildings.
  - 3,614 teams in 94 countries made 39,403 submissions.
  - Top entries were large ensembles of mostly gradient-boosting tree models such as LightGBM, and preprocessing was decisive.

  — [arXiv 2007.06933](https://arxiv.org/abs/2007.06933)
- **Data preparation matters most.** A follow-up survey of top teams (Miller, Hao & Fu, 2022) found that "preprocessing and feature extraction phases were the most important aspects of creating the best modeling approach". — [arXiv 2202.02898](https://arxiv.org/pdf/2202.02898v1.pdf)
- **A reference dataset needed heavy cleaning.** Building Data Genome 2 (Miller et al., 2020, *Scientific Data* 7:368) contains 3,053 meters from 1,636 buildings, hourly for two full years (2016–2017). The paper documents the cleaning and assembly of meter time series, metadata and weather data, and the repository separates raw from cleaned data. — [arXiv 2006.02273](https://arxiv.org/abs/2006.02273v4)
- **AI footprint depends on model type.** Luccioni, Jernite & Strubell (ACM FAccT 2024) measured energy and carbon per 1,000 inferences. Multi-purpose generative architectures were "orders of magnitude more expensive than task-specific systems", even controlling for parameter count. — [arXiv 2311.16863](https://arxiv.org/abs/2311.16863)
- **Non-AI first: commissioning finds the faults.** Commissioning 643 buildings uncovered more than 10,000 energy-related deficiencies (in the third of projects with data). Fixing them gave 16% median whole-building savings with a 1.1-year payback in existing buildings. — [Mills 2011, Energy Efficiency 4:145–173](https://rd.springer.com/content/pdf/10.1007/s12053-011-9116-8.pdf) (details in section 6)

### Inferences
- **Minimum data prerequisites before IIT attempts ML forecasting or optimisation:**
  - at least 12 months of validated 15-minute or hourly data per main meter, covering both monsoons, semesters, exams and vacations;
  - local weather data including humidity, since latent cooling load matters in Colombo;
  - timetable and occupancy proxies;
  - a meter hierarchy and floor areas;
  - automated data-quality checks (gaps, flat-lines, spikes, meter resets).
- **Start with a transparent regression baseline** (energy against cooling degree days plus teaching days). It is sufficient for measurement and verification (section 8) and for anomaly alerts. Add ML only once that baseline is stable.
- **The new campus cannot use historical ML at first.** It should rely on the design energy model, commissioning, and then a calibrated baseline after 12 months of operation (IPMVP Option D, then C).
- **Avoid compute-heavy features without a clear payoff.** Large-language-model chatbots in the engagement app should not be added unless they show measurable value. This is consistent with Luccioni et al.

### Gaps
- I found no study specifying a minimum data length for ML forecasting in tropical campus buildings.
- I did not re-verify the IEA figures in this session (accepted as given in the brief).

---

## 6. Failure modes in campus energy dashboards and IoT, with mitigations

### Takeaway
The documented failures are mainly organisational and data-related:
- engagement decays within weeks;
- feedback or competition savings are modest (7.4% average, smaller in rigorous studies) and partly reverse once a campaign stops;
- raw meter data needs systematic cleaning;
- building faults go undetected without commissioning;
- proprietary BMS metadata locks owners in;
- building systems are an established attack path (Target 2013; tens of thousands of exposed BACnet devices);
- turnover-driven knowledge loss is quantifiable.

Each has a known mitigation, summarised in the Inferences.

### Cited Findings

#### a) Data quality and gaps
- **Cleaning is unavoidable.** BDG2 had to be cleaned and assembled before release (raw versus cleaned folders) — [Miller et al. 2020](https://arxiv.org/abs/2006.02273v4). GEPIII winners found preprocessing to be the most important step — [Miller, Hao & Fu 2022](https://arxiv.org/pdf/2202.02898v1.pdf).
- **Feedback devices fail and get abandoned.** In a study of 23 Australian households with energy feedback, initially high engagement gave way to "disinterest, neglect and in certain cases, technical malfunction". — [Snow et al. (2013), "Curiosity to cupboard: self reported disengagement with energy use feedback over time", QUT ePrints](https://eprints.qut.edu.au/65130)

#### b) Sensor/meter maintenance and commissioning
- **Mills (2011) meta-analysis** (*Energy Efficiency* 4:145–173) of 643 non-residential buildings (99 million ft², US$43m of commissioning spend):
  - The third of projects with data revealed more than 10,000 energy-related deficiencies.
  - Correcting them gave median whole-building savings of 16% in existing buildings (payback 1.1 years) and 13% in new construction (payback 4.2 years).
  - Median commissioning cost was US$0.30/ft² for existing buildings and US$1.16/ft² for new construction.
  - Median benefit-cost ratios were 4.5 (existing) and 1.1 (new).
  - Comprehensive commissioning gave nearly twice the overall median savings.

  — [Mills 2011 (Springer PDF)](https://rd.springer.com/content/pdf/10.1007/s12053-011-9116-8.pdf); [OSTI record](https://www.osti.gov/biblio/985240-building-commissioning-golden-opportunity-reducing-energy-costs-greenhouse-gas-emissions)

#### c) "Dashboard fatigue", novelty and decay of feedback effects
- **Repeated feedback shows cycles of action and backsliding (Allcott & Rogers 2014).** In the Opower home energy report programme (*American Economic Review* 104(10):3003–3037), early reports produced repeated cycles of action and backsliding that faded over time. When reports stopped after two years, effects were "relatively persistent", decaying at 10–20% per year. Households kept responding to repeated reports even after two years. — [NBER w18492](https://www.nber.org/papers/18492); [RePEc](https://econpapers.repec.org/RePEc:aea:aecrev:v:104:y:2014:i:10:p:3003-37)
- **Average effects are modest and shrink with study rigour (Delmas, Fischlein & Asensio 2013).** Across 156 field trials (1975–2012, more than 500,000 subjects; counts differ slightly between sources):
  - The average electricity reduction was 7.4%.
  - "The conservation effect diminishes with the rigor of the study."
  - Individualised audits and consulting outperformed historical and peer-comparison feedback.

  — [Energy Policy 61:729–739 (PDF)](https://www.ioes.ucla.edu/wp-content/uploads/2017/07/2013-Delmas-Fischlein-Asensio-EnergyPolicy.pdf)
- **Campus competition: partial rebound afterwards (Konis, Orosz & Sintov 2016, *Energy and Buildings* 116).**
  - 39 eight-occupant suites in a freshman residence hall had 15-minute circuit-level metering.
  - During a three-week competition (Fall 2014), whole-building demand fell 6.4%, and 12% during peak hours.
  - Afterwards, on weather-normalised HVAC demand, 19 suites rebounded significantly, 12 cut further, and the rest held at competition levels.
  - Persistence was associated with self-efficacy, pro-environmental behaviour and a sense of affiliation with other residents.

  — [OSTI 1290124 (DOI 10.1016/j.enbuild.2016.01.005)](https://www.osti.gov/pages/biblio/1290124)
- **Usage falls after about a month.** A doctoral thesis on eco-feedback reports a novelty effect in which use of the devices "declines significantly after a month". It found no evidence that consumption returned to pre-feedback levels. [flag: thesis author not verified; Universidade da Madeira repository] — [digituma.uma.pt thesis record](https://digituma.uma.pt/entities/publication/051c3229-b3b6-434e-86fd-97de220a4331/full)

#### d) Rebound effects
- **Direct rebound is generally below 30%.** Sorrell, Dimitropoulos & Sommerville (2009) conclude that direct rebound for household energy services in the OECD is "generally below 30%". They flag several sources of bias that can make rebound look larger (*Energy Policy* 37(4):1356–1371). — [RePEc](https://econpapers.repec.org/RePEc:eee:enepol:v:37:y:2009:i:4:p:1356-1371)

#### e) Vendor lock-in and interoperability
- **Owners bear most of the cost.** Inadequate interoperability cost US capital facilities $15.8bn per year (2002), with $10.6bn falling on owners and operators. — [NIST GCR 04-867](https://www.nist.gov/publications/cost-analysis-inadequate-interoperability-us-capital-facilities-industry)
- **Building metadata is vendor-specific.** De-facto industry practice uses "unstructured vendor- and building-specific idioms intended for human consumption rather than programmatic manipulation". Brick (open-source, BSD-licensed) models concepts for portable software. Project Haystack is a semi-structured tagging scheme (Academic Free License 3.0), and a 2020 study found "systemic interpretability and consistency issues" in Haystack. — [Frontiers in Built Environment 2020, 10.3389/fbuil.2020.558034](https://www.frontiersin.org/article/10.3389/fbuil.2020.558034)
- **A convergent standard is in progress.** ASHRAE, Project Haystack and Brick announced in 2018 that they would align on the proposed ASHRAE Standard 223P. [flag: I did not verify whether 223P has been finalised.] — [AutomatedBuildings, February 2018](https://automatedbuildings.com/releases/feb18/180228111001ashrae.html)

#### f) Cybersecurity of building systems
- **Target, 2013 (entry via an HVAC/refrigeration vendor's credentials).**
  - Attackers entered Target's network on 15 November 2013 using credentials stolen from Fazio Mechanical Services, a refrigeration and HVAC contractor.
  - About 40 million card accounts were exposed between 27 November and 15 December 2013, and up to 70 million other records were compromised.
  - Fazio said its link was used for billing, contracts and project management, not remote HVAC monitoring.

  — [Krebs on Security, 5 February 2014](https://krebsonsecurity.com/2014/02/target-hackers-broke-in-via-hvac-company/); [InfoWorld](https://www.infoworld.com/article/2192027/target-contractor-says-it-was-victim-of-cyber-attack.html)
- **Casino fish-tank thermometer, reported April 2018.** Darktrace CEO Nicole Eagan told the WSJ CEO Council in London that attackers entered an unnamed North American casino's network through an internet-connected fish-tank thermometer and reached its high-roller database. [flag: a single vendor anecdote with no independent confirmation; a separate July 2017 Darktrace case also involved a fish tank.] — [Security Affairs, April 2018](https://securityaffairs.com/71433/hacking/fish-tank-hack.html); [Entrepreneur](https://entrepreneur.com/business-news/a-casino-gets-hacked-through-a-fish-tank-thermometer/368943)
- **Exposure studies.**
  - DIVD case 2022-00005 (Dutch Institute for Vulnerability Disclosure; scan in December 2021, case closed April 2022): 29,736 BACnet systems exposed to the internet, of which 12,572 were vulnerable; owners were notified. — [DIVD report](https://vintage.divd.nl/reports/2022-00005%20-%20Exposed%20BACnet%20Devices)
  - Project SHINE (2014, Shodan-based): about 2.2 million control-system-related devices exposed, including 13,475 HVAC and building-automation devices. — [ControlTrends](https://controltrends.org/building-automation-and-integration/10/cyber-security-eye-opener-project-shine-shodan-intelligence-extraction-reveals-magnitude-of-internet-connected-critical-control-systems/)
  - A TUM team ran Internet-wide measurements of BACnet's exposure to DDoS amplification. — [TUM publication record](https://portal.fis.tum.de/en/publications/security-implications-of-publicly-reachable-building-automation-s/)
  - [flag: scan figures from different years measure different things and are not directly comparable.]
- **Standard guidance.** NIST SP 800-82 Rev. 3, *Guide to Operational Technology (OT) Security* (September 2023), explicitly covers building automation systems. It provides topologies, threats, vulnerabilities and safeguards, plus an SP 800-53 overlay with low, moderate and high baselines. — [NIST SP 800-82r3 (DOI)](https://doi.org/10.6028/NIST.SP.800-82r3); [NIST announcement](https://content.govdelivery.com/accounts/USNIST/bulletins/372dc12)

#### g) Staff turnover and knowledge loss (relevant to student developers)
- **Rigby, Zhu, Donadelli & Mockus (ICSE 2016)** studied Chrome and a project at Avaya:
  - A file counts as "abandoned" when 90% or more of its owners have left.
  - Projects were susceptible to losses more than five times the expected loss.
  - Simplistic "truck factor" estimates exaggerate the potential for loss.
  - Recommending successors was correct 34–48% of the time and reduced expected loss by up to 15%.

  [secondary summaries; full text not read] — [DBLP record](https://dblp.dagstuhl.de/rec/conf/icse/RigbyZDM16.html); [Never Work in Theory review](https://neverworkintheory.org/2021/09/30/quantifying-and-mitigating-turnover-induced-knowledge-loss.html)

### Inferences (mitigations for IIT)
- **Data quality**
  - Keep a meter register (ID, location, CT ratio, parent meter, floor area served).
  - Reconcile monthly against CEB/LECO utility bills.
  - Set automated completeness and flat-line alerts.
  - Publish a data-quality score for each meter, so dashboards are never shown on unvalidated data.
- **Commissioning**
  - Make independent commissioning, and ideally monitoring-based commissioning, a contract requirement for the new campus. Mills' medians correspond to roughly US$12.5/m² for new construction and US$3.2/m² for retro-commissioning (2009 dollars; my conversion).
  - Retro-commission the existing campus: schedules, setpoints, chiller sequencing.
  - On Mills' evidence, this is probably the highest-return action available.
- **Engagement decay**
  - Plan campaigns in semester-length bursts.
  - Make feedback actionable and individual: room or department level, with specific actions. This follows Delmas' finding that audits and advice beat comparisons.
  - Build affiliation and self-efficacy, as in Konis et al.
  - Lock in savings structurally (BMS schedules, setpoints) rather than relying on sustained attention.
  - In benefit forecasts, assume behavioural savings decay once a campaign stops (Allcott & Rogers: 10–20% per year after two years of treatment).
- **Rebound in a hot, humid climate**
  - Efficiency gains in cooling may be partly taken back through lower setpoints or longer air-conditioning hours (inference; I found no cooling-specific rebound figure).
  - Pair efficiency measures with a setpoint policy (for example 24–25 °C, subject to comfort checks) and monitor setpoint drift.
- **Lock-in**
  - Specify open protocols (for example BACnet/IP) and full points-list export.
  - Specify IIT ownership of all data, with documented APIs and data export on contract exit.
  - Use a metadata convention (Brick or Haystack tags) and avoid cloud-only proprietary platforms.
- **Cybersecurity**
  - Never expose the BMS or IoT devices directly to the internet; segment OT/IoT onto separate networks (VLANs).
  - Route vendor remote access through MFA and a monitored jump host, as a lesson from Target.
  - Maintain an asset inventory, change default credentials, and plan firmware updates.
  - Adopt the NIST SP 800-82r3 low-baseline controls proportionately.
- **Student-developer turnover**
  - The permanent developer owns the core codebase and architecture; students build bounded modules against documented APIs.
  - Repositories sit under an IIT organisation account; code review is mandatory.
  - Each module has at least two knowledgeable people.
  - Hold handover sprints before each cohort leaves.
  - Prefer a boring, mainstream stack.

### Gaps
- I found no campus-specific longitudinal study of dashboard page-views or usage decline. The evidence is from households and residence halls.
- I found no verified rebound estimate for space cooling. One secondary review reports a cooling range of 0–50%, but I could not confirm its source.
- I found no Sri Lankan data on exposed BMS or IoT devices.

---

## 7. Governance and implementation: phasing/MVP, steering groups and data owners, benefits realisation, why IS projects fail to deliver benefits

### Takeaway
Two bodies of evidence frame the risk:
- Higher-education sustainability efforts falter mainly from a lack of senior support and investment: Ávila et al. (2017) surveyed 301 experts at 172 universities.
- IT investments routinely under-deliver benefits. In Ward & Daniel's survey, 57% of organisations said fewer than half of their projects delivered the expected benefits. McKinsey and Oxford found that large IT projects delivered 56% less value than predicted.

The remedies are:
- explicit benefit ownership, using a benefits dependency network;
- stage-gated, MVP-first delivery (discovery → alpha → beta → live);
- data-governance decision rights for data owners;
- self-financing through a green revolving fund (median ROI 28–32%).

### Cited Findings
- **Senior support is the critical barrier in higher education.** Ávila et al. (2017), *Journal of Cleaner Production* 164:1268–1278, surveyed 301 experts from 172 universities on every continent. Barriers were similar across regions and need more backing from university administrations. Senior leaders' commitment is often lacking, and bottom-up initiatives without senior support tend to fail over time. — [JCU research repository](https://researchonline.jcu.edu.au/50861/)
- **Benefits come from change, not technology alone (Ward & Daniel).** *Benefits Management* (Wiley, 2nd edition, 2012) argues that business benefits depend "not only on the implementation of IS and IT, but also on changing organizational processes and relationships and the roles and working practices of people". The Benefits Dependency Network is a cause-effect map showing how improvements arise from business changes combined with new IT capabilities. It makes clear "who needs to become accountable for making the specific changes and delivering the benefits". — [O'Reilly, chapter 2](https://www.oreilly.com/library/view/benefits-management-delivering/9780470094631/ch02.html); [Perlego listing](https://www.perlego.com/fr/book/1004122/benefits-management-how-to-increase-the-business-value-of-your-it-projects-pdf)
- **Most organisations under-deliver.** Ward & Daniel's survey (2008), reported in the book, found that in 57% of organisations "less than half of the projects they undertook delivered the expected benefits". [flag: survey sample and method not verified; excerpt via Perlego] — [Perlego](https://www.perlego.com/fr/book/1004122/benefits-management-how-to-increase-the-business-value-of-your-it-projects-pdf)
- **Companion article.** Peppard, Ward & Daniel, "Managing the realization of business benefits from IT investments", *MIS Quarterly Executive* 6(1). [flag: year listed as 2007 in some indexes and 2008 in others.] — [AIS eLibrary](https://aisel.aisnet.org/misqe/vol6/iss1/3/); [Open University ORO](https://oro.open.ac.uk/11227)
- **Large IT projects (McKinsey with Oxford's BT Centre for Major Programme Management, 2012).**
  - Research on more than 5,400 IT projects found that large projects (initial budget above US$15m) run on average 45% over budget and 7% over time, and deliver 56% less value than predicted.
  - 17% of IT projects go so badly that they can threaten the existence of the company.

  — [McKinsey (2012)](https://www.mckinsey.com/capabilities/transform/our-insights/delivering-large-scale-it-projects-on-time-on-budget-and-on-value)
- **"Black swan" overruns.** Oxford's analysis (Flyvbjerg & Budzier, 2011) found that one in six IT projects had an average cost overrun of 200% and a schedule overrun of almost 70%. — [Phys.org, August 2011](https://phys.org/news/2011-08-timebombs.pdf)
- **Phased, MVP-first delivery (GOV.UK Service Manual).** The model has four phases: discovery, alpha, beta and live. Discovery explores the problem before committing to build, and alpha tests different solutions. Beta's length depends on the scope of the minimum viable product, and work continues after live. Services are assessed against the Service Standard at the end of discovery, alpha and beta. — [GOV.UK, beta phase](https://www.gov.uk/service-manual/phases/beta); [GOV.UK, live phase](https://www.gov.uk/service-manual/phases/live.html); [Welsh CDPS, the phases of agile delivery](https://digitalpublicservices.gov.wales/guidance-and-standards/service-manual/delivering-services-agile-way/the-phases-of-agile-delivery)
- **Data governance means decision rights (Khatri & Brown 2010).** *Communications of the ACM* 53(1):148–152 defines data governance as "who holds the decision rights and is held accountable for an organization's decision-making about its data assets". It adapts Weill & Ross's IT-governance framework into five decision domains: data principles, data quality, metadata, data access and data lifecycle. [flag: only "data principles" was confirmed in search snippets; the other four are from the well-known framework and the DOI.] — [ACM DOI 10.1145/1629175.1629210](https://doi.org/10.1145/1629175.1629210)
- **Green revolving funds (Sustainable Endowments Institute).**
  - The 2011 survey of 52 schools found a median annual return of 32% and a median payback of 4 years.
  - The 2012 report (79 funds at 76 institutions) found a median annual ROI of 28%.

  — [SEI, Greening the Bottom Line 2012 (PDF)](https://greenbillion.org/wp-content/uploads/2012/11/Greening-the-Bottom-Line-2012.pdf); [Inside Higher Ed (2011)](https://www.insidehighered.com/node/42729)
- **Smart-campus practice is immature across all four domains, including governance.** — [Polin et al. 2023](https://www.mdpi.com/2075-5309/13/4/891)

### Inferences (IIT-specific design)
- **Steering group**
  - Chair: a senior executive (for example the COO or Registrar), reflecting Ávila's finding on senior commitment.
  - Members: Facilities (data owner for meters and the BMS, and benefit owner for kWh and water KPIs); IT (data custodian and security); Finance (benefits tracking and the revolving fund); an academic lead (student projects and curriculum links); a student union representative; and the Data Protection Officer (PDPA, DPIA sign-off for the app).
  - Meets monthly in year 1, then quarterly.
- **Benefits register (Ward & Daniel)**
  - For each benefit, record: owner, metric, baseline, target, measurement method (IPMVP option), and review date.
  - Map each app or dashboard feature to the business change it enables. Features with no linked business change and benefit owner are not built.
- **Phasing map (reject / defer / adopt)**
  - Reject: facial recognition or biometric attendance, emotion recognition, blockchain or crypto tokens.
  - Defer to a year-3 stage-gate: a campus digital twin, CV smart bins, advanced AI optimisation.
  - Adopt now:
    - Phase 0 (months 0–6): discovery, data audit and meter register; start baseline data collection; retro-commission quick wins; write open-protocol, metering and commissioning clauses into new-campus contracts.
    - Phase 1 (months 6–18): MVP internal dashboard on validated data; regression baseline; first measured savings.
    - Phase 2 (months 18–36): engagement app built privacy-by-design, with DPIA completed before launch and PDPA-ready by 1 January 2027; M&V of measures; optional analytics if the data-quality gates are met.
- **Finance**
  - Ring-fence part of the LKR 80m as a revolving fund, recycling verified savings from quick wins into the next measures.
  - This aligns finance with M&V (section 8) and protects the programme beyond the three-year grant.

### Gaps
- I found no evidence specific to South Asian higher education on MVP-first sustainability programmes or steering-group effectiveness.
- I did not verify Ward & Daniel's survey method.
- The GOV.UK phase durations quoted by secondary sites (4–8 weeks for discovery, 6–8 weeks for alpha) were not confirmed on GOV.UK itself.

---

## 8. Evaluation: baselining and normalising energy/water KPIs, M&V of savings (IPMVP, ASHRAE Guideline 14), and target-setting good practice

### Takeaway
Credible evaluation needs four things:
- **A baseline:** 12 months representing a full operating cycle (an academic year for IIT).
- **Normalisation:** use the drivers (degree days, occupancy or FTE, floor area) to track the same site over time. Be careful using them for cross-institution comparison; AASHE dropped degree-day normalisation in STARS 3.0 as "ineffective, and possibly counterproductive".
- **M&V:** follow IPMVP options and use ASHRAE Guideline 14 statistical criteria for model fit.
- **Targets:** set absolute targets with intensity metrics alongside. Follow GHG Protocol base-year rules: the new campus counts as "organic growth", so the base year is not recalculated. Use SBTi's 4.2%/yr (1.5 °C) as an ambition reference. SBTi's Corporate Net-Zero Standard V2.0 was published on 11 June 2026.

### Cited Findings
- **IPMVP basics.**
  - Option C uses whole-facility (utility) meters and needs both baseline and reporting-period data.
  - "Driving factors (e.g. degree days, production)" are usually needed to calculate savings.
  - Option D (calibrated simulation) is used when there is no baseline data, which is relevant to the new campus.
  - The baseline period represents a normal operating cycle.
  - The 2022 IPMVP Core Concepts were released in March 2022.
  - [flag: I did not read the 2022 text itself.]

  — [EVO, IPMVP page](https://evo-world.org/en/products-services-mainmenu-en/protocols/ipmvp); [UT Austin M&V Framework draft (December 2019)](https://utilities.utexas.edu/sites/default/files/M%26V-Framework_DRAFT_2019-12-12.pdf); [UNEP-CCC webinar, 2022 IPMVP Core Concepts](https://globalesconetwork.unepccc.org/events/release-of-the-2022-ipmvp-core-concepts-highlights/)
- **The "savings over 10%" rule for Option C.**
  - The 10% language originates in the 2002 IPMVP Option C guidance, and EVO notes the wording has been updated several times. — [EVO M&V Focus, November 2020, "Detecting savings under 10% using IPMVP Option C"](https://evo-world.org/en/m-v-community/mv-focus/883-october-2020-m-v-focus-issue-7/1192-detecting-savings-under-10-using-ipmvp-option-c)
  - Secondary summaries say savings should exceed about 10% of baseline when only monthly data exist, while daily or hourly models can detect smaller savings. An ACEEE 2020 analysis of 192 buildings reports detection down to about 3%. [secondary] — [GlacierGrid summary](https://glaciergrid.com/resources/research-and-impact/the-power-of-ipmvp-unlocking-the-true-potential-of-energy-savings)
- **ASHRAE Guideline 14 model-fit criteria.**
  - Commonly cited thresholds: monthly NMBE within ±5% and CV(RMSE) ≤15%; hourly NMBE within ±10% and CV(RMSE) ≤30%.
  - NMBE (bias) and CV(RMSE) (scatter) must both pass.
  - The 2014 edition has been superseded by a 2023 edition.
  - [flag: one documentation source lists hourly NMBE as ±5%; check the primary text before quoting.]

  — [ORNL, "Suitability of ASHRAE Guideline 14 metrics for calibration"](https://impact.ornl.gov/en/publications/suitability-of-ashrae-guideline-14-metrics-for-calibration/); [UTK (2016) PDF](https://web.eecs.utk.edu/~jnew1/publications/2016_ASHRAE_G14.pdf); [arXiv 2603.01198 (cites the 2023 edition)](https://arxiv.org/pdf/2603.01198); conflicting value in [energykit docs](https://energykit.readthedocs.io/en/latest/api/benchmark.html)
- **Normalisation: lessons from AASHE STARS.**
  - STARS v2 scored building energy per gross floor area per degree day. The base was 65 °F (18 °C) for both heating and cooling degree days, and the threshold was 65 Btu/ft²/°F-day (389 per m² per °C-day).
  - AASHE's later analysis concluded that "energy-intensive space and degree days were ineffective, and possibly counterproductive" as normalisation factors for comparing institutions, and removed them in STARS 3.0.

  — [AASHE analysis](https://stars.aashe.org/?p=8577); [AASHE, "Assessing energy use intensity in STARS 3.0 and beyond"](https://stars.aashe.org/news/assessing-energy-use-intensity-in-stars-3-0-and-beyond/); [example OP-5 report](https://reports.aashe.org/institutions/3388/report/2021-05-06/OP/energy/OP-5/documentation)
- **Weather-normalised evaluation in practice.** Konis et al. (2016) used weather-normalised HVAC demand to judge whether savings persisted after a residence-hall competition. — [OSTI 1290124](https://www.osti.gov/pages/biblio/1290124)
- **Hot-humid benchmark (Singapore).**
  - In 2017, average energy use intensity was 358 kWh/m²/yr for universities and 124 kWh/m²/yr for polytechnics. The source is a BCA roadmap citing the BCA Building Energy Benchmarking Report 2018.
  - EUI is defined as annual electricity (kWh) divided by gross floor area.
  - Educational buildings account for about 11% of total energy consumption in the building data covered.

  — [BCA SLE tech roadmap report](https://www1.bca.gov.sg/docs/default-source/docs-corp-buildsg/digitalisation/sle_tech_roadmap_report.pdf)
  - BCA published formal benchmarks until 2022. 2023 EUI data were released without benchmarks. — [NUS IREUS summary (January 2025)](https://ireus.nus.edu.sg/wp-content/uploads/2025/01/Refining-Energy-Use-Benchmarks-for-Commercial-Properties-in-Singapore-Summary_-20250122.pdf)
- **GHG Protocol Corporate Standard (revised edition), Chapter 5 "Tracking Emissions Over Time"** [primary text checked]
  - Base-year emissions are recalculated for significant structural changes, methodology changes and errors.
  - The standard "makes no specific recommendations as to what constitutes 'significant'", though some programmes set numerical thresholds.
  - "Base year emissions and any historic data are not recalculated for organic growth or decline". Organic growth includes "closures and openings of operating units that are owned or controlled by the company".
  - The significance threshold is for the company or verifier to determine.

  — [GHG Protocol Corporate Standard (PDF)](https://ghgprotocol.org/sites/default/files/standards/ghg-protocol-revised.pdf)
  - Examples of thresholds in practice: Eastman uses 5% of base-year emissions — [Eastman GHG recalculation policy](https://Eastman.com/content/dam/eastman/corporate/en/sustainability/governance/resources/ghg-recalculation-policy.pdf). The California Climate Action Registry used 10%. [secondary]
- **SBTi ambition levels.**
  - Near-term criteria set a minimum 4.2% annual linear reduction in scope 1+2 emissions for 1.5 °C alignment (about 42% by 2030 from a 2020 base) and 2.5% for well-below 2 °C, over a 5–10-year timeframe. [secondary summaries of the SBTi near-term criteria] — [Salesforce Trailhead module citing SBTi](https://trailhead.salesforce.com/content/learn/modules/science-based-target-setting-and-emissions-forecasting/prepare-for-science-based-targets)
  - [flag: one low-quality source claims SBTi halved required 2030 cuts. That is unverified and contradicted by the other sources.]
- **SBTi Corporate Net-Zero Standard V2.0 (current status).**
  - Published 11 June 2026, usable for target validation from 1 February 2027, and reported as mandatory from 2028.
  - Companies with targets due in 2026–27 are advised to stay on V1.3 until their next cycle.
  - It introduces size- and sector-differentiated target-setting and an implementation hierarchy.

  — [SBTi CNZS V2.0 (PDF)](https://files.sciencebasedtargets.org/production/files/Corporate-Net-Zero-Standard-version-2.pdf); [SBTi blog](https://sciencebasedtargets.org/blog/the-corporate-net-zero-standard-v2-0-is-here-what-comes-next); [Rödl & Partner, 25 June 2026](https://www.roedl.com/en/insights/science-based-targets-the-new-corporate-net-zero-standard-version-2-0-is-here-our-action-recommendations/)
- **Evaluate with comparison groups.** Weaker study designs show larger savings, so an internal evaluation of the app needs a comparison group. — [Delmas et al. 2013](https://www.ioes.ucla.edu/wp-content/uploads/2017/07/2013-Delmas-Fischlein-Asensio-EnergyPolicy.pdf)

### Inferences
- **Baselines**
  - Existing campus: build a monthly baseline from 24–36 months of utility bills now. Start a 15-minute or hourly baseline from the first month of validated smart-meter data, and run it for 12 months covering both monsoons, both semesters and vacations.
  - New campus: treat as organic growth. Do not recalculate the base year; report it as a separate line, then set its own operational baseline after 12 months (IPMVP Option D, then C).
- **Normalisation choice for Colombo**
  - Temperature seasonality is small, so the academic calendar (teaching days, exams, vacations) and humidity are likely bigger drivers than cooling degree days.
  - Test cooling degree days (base about 18 °C, or a fitted balance point) against teaching days in a regression, and keep the variables that are statistically significant.
  - Report absolute kWh, absolute tCO₂e, kWh/m² GIA and kWh per FTE (students plus staff). Report water as m³ per FTE.
  - Use per-m² and per-FTE intensities for trend tracking. Cross-institution comparison (for example with Singapore's 358 kWh/m²/yr for universities) is context, not a target, given AASHE's warning.
- **M&V**
  - Discrete measures with savings below 10% (for example chiller scheduling): Option A or B with sub-metering.
  - Whole-campus programme: Option C with interval data.
  - Models must meet Guideline 14 fit criteria before savings are claimed.
  - App or behaviour programmes: a staggered roll-out or matched comparison buildings.
- **Targets**
  - Set an absolute scope 1+2 reduction path. Use SBTi's 4.2%/yr as an ambition reference rather than a formal validation, given the gaps below.
  - Add intensity targets and an annual review.
  - Write and publish a base-year recalculation policy in advance, with a threshold such as 5%.

### Gaps
- I did not verify whether SBTi validates targets for higher-education institutions, so treat the 4.2%/yr figure as a reference only.
- Sri Lanka's grid emission factor and local higher-education energy benchmarks were not researched here; they may be covered by another researcher.
- I did not read the IPMVP 2022 and ASHRAE Guideline 14-2023 primary texts; thresholds come from secondary and academic summaries.
- I found no peer-reviewed tropical-campus study comparing cooling degree days with occupancy-based normalisation.
