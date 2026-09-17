# iMicroSeq testing package

**Version 1.2 — draft for testing round 1, revised 2026-09-16**

Materials for testing the iMicroSeq contextual data specification with collaborators, modelled on
the iterative subgrant testing used for the [PHA4GE Wastewater Contextual Data
Specification](https://github.com/pha4ge/wastewater-contextual-data-specification).

The specification under test is iMicroSeq v1.0: **155 fields — 13 required, 48 recommended,
94 optional** — as exported to `3. Specification Development/schema_slots.tsv` and
`schema_enums.tsv` on 2026-09-16.

Testers use the DataHarmonizer to apply the specification, but **the specification is what is under
test, not the DataHarmonizer**. The instructions say so up front.

---

## Start here

| If you are… | Read |
|---|---|
| A tester | `iMicroSeq_Testing-Instructions_v1.2.docx`, then `iMicroSeq_Worked-Example-Scenarios_v1.2.docx` |
| Recruiting testers | `iMicroSeq_Tester-Call-Out_v1.2.docx` |
| Running the round | This file, then the "Before you circulate" checklist below |

---

## Contents

```
Testing/
├── README.md                                        this file
├── iMicroSeq_Testing-Instructions_v1.2.docx         the testing protocol, Parts A–D
├── iMicroSeq_Worked-Example-Scenarios_v1.2.docx     the three scenarios, written out
├── iMicroSeq_Tester-Call-Out_v1.2.docx              recruitment invitation
├── Answer Keys/
│   ├── iMicroSeq_Blank-Template_v1.2.xlsx           empty template + full field guide
│   ├── iMicroSeq_AnswerKey_S1_Municipal-Wastewater_v1.2.xlsx
│   ├── iMicroSeq_AnswerKey_S2_Drinking-Source-Water_v1.2.xlsx
│   ├── iMicroSeq_AnswerKey_S3_Leachate-Mining-AMR_v1.2.xlsx
│   ├── Archive/                                     superseded v1.1 keys and v1.0 blank template
│   └── Not in round 1/                              two scenarios parked for a later round (not updated to the 2026-09-16 spec)
│       ├── iMicroSeq_AnswerKey_Surface-Water-Watershed_v1.0.xlsx
│       └── iMicroSeq_AnswerKey_Marine-Aquaculture-Host_v1.0.xlsx
├── Feedback/
│   ├── iMicroSeq_Testing-Feedback-Form_v1.2.docx    earlier Word draft - superseded by the Google Form, whose questions and order now differ
│   ├── iMicroSeq_Field-Level-Feedback_v1.2.xlsx     optional; 6 sheets, incl. all 155 fields pre-listed
│   └── Archive/                                     superseded v1.1 files
└── Archive/                                         superseded v1.1 documents
```

The feedback form testers complete is the Google Form at https://forms.gle/tQaS8h7wcqxSaghE6. It is
the only required return; the field-level workbook is optional.

---

## The three scenarios

Round 1 uses three scenarios, not five. The point of Part B is to make testers fluent enough in the
template that Part C tells us about the *specification*, not about their curation skill — so the
scenario load is deliberately light and the weight of the round sits on the tester's own use case.
All content is fictional and flagged as such.

| | Scenario | Records | What it stresses |
|---|---|---|---|
| **S1** | Municipal wastewater treatment plant influent | 4 | Composite autosampling, catchment population, flow and physicochemistry, PMMoV normalisation, all three diagnostic target blocks, a negative control as its own record |
| **S2** | Source and drinking water, community-triggered | 3 | Groundwater and distribution systems, bag-mediated filtration, community observation terms, 16S amplicon, `Restricted Access` for governance-sensitive fields |
| **S3** | Landfill leachate and mining-influenced water | 3 | Mining and landfill land uses, leachate and runoff, passive sampling and pooling, pH and conductivity extremes, AMR gene targets |

Testers curate all three. The surface-water/watershed and marine-aquaculture scenarios are kept in
`Answer Keys/Not in round 1/` for a later round.

### Everything in them is fictional, and says so

Projects are prefixed `[FICTIONAL]`, organisations carry `(fictional organisation)`, personal names
carry `(fictional name)`, emails and URLs use the reserved `example.org` domain, coordinates are
patterned decimals pointing at no real facility, and the sheet tabs read `Answer Key (FICTIONAL)`
and `Scenario (FICTIONAL)` with a banner line at the foot of the scenario text. Kettle Harbour,
Nickelford and Cedar Ridge Environmental Consulting do not exist.

Each answer key workbook has three sheets:

- **Answer Key (FICTIONAL)** — the formatted template view, colour-coded yellow / purple / white for
  required / recommended / optional.
- **DH_import** — the same records with a single header row, for import into the DataHarmonizer.
- **Scenario (FICTIONAL)** — the narrative, what the scenario is testing, and the fictional-data
  banner.

Every answer key validates against the 2026-09-16 specification with **zero errors and zero
warnings**. Recommended fields that do not apply carry an explicit null
value rather than a blank — that is a deliberate teaching point, not padding.

---

## The testing protocol in brief

| Part | What the tester does | Roughly |
|---|---|---|
| A — Orientation | Read the SOP and reference guide; open the template; record a first impression | 30 min |
| B — Worked scenarios | Curate each scenario, **validate it in the DataHarmonizer**, save, then compare against the answer key | 1.5–2 h |
| C — Your own data | Curate 10–20 of their own records and **validate them**, locally — the file is never returned | 2–3 h |
| D — Feedback | Feedback form (Google Form, required — the only deliverable); field-level workbook and 45 min debrief optional | 30–45 min |

Validation is part of the curation loop in Parts B and C rather than a separate part (agreed
2026-09-16). Setting up the DataHarmonizer (download the .zip from the iMicroSeq repository's
`Template` folder, unzip, open `web/dist/index.html`, pick the iMicroSeq template) is Section 4 of the
instructions. Total 4–6 hours, all of it on the tester's own machine in the DataHarmonizer. A tester who stops
after Part B still contributes something usable. Testers are not asked to share any of their own
data — the specification is what is under test, not their records.

---

## Before you circulate this package

- [ ] **Ethics.** Confirm whether this round falls under the existing SFU REB approval covering the
      needs assessment, needs an amendment, or is exempt as quality improvement. Insert the agreed
      consent statement in the Testing Instructions (§6) and the Call-Out. Both currently carry a
      placeholder callout saying so.
- [x] **Contact details.** Done — all four documents carry Emma Griffiths, emma_griffiths@sfu.ca.
- [x] **DataHarmonizer .zip.** `Template/DataHarmonizer.zip` is in the repository and linked from §4 of the
      Testing Instructions.
- [x] **Feedback form.** Live as a Google Form and linked from the Testing Instructions.
- [ ] **Spec source fixes.** `conductivity measurement unit` has range `ConductivityMeasurementUnit`
      (missing `Menu`); `host age unit` points at `HostAgeUnitInternationalMenu`, which does not exist;
the term
      `Excretory system (organizational term)` has no ontology ID. Check these in the template build.
- [ ] **Return route.** The feedback form is submitted online. Optional extras (field-level workbook, Part B
      files) are emailed to Emma Griffiths — confirm. Testers keep their own data: all testing is local.
- [ ] **Deadline.** Set the return date and replace the highlighted placeholder in §6 of the Testing Instructions.
- [x] **New term request route.** The issue forms (new term, bulk new term, new field, change field,
      change term) are live in the iMicroSeq repository; the instructions link to them.

---

## Analysing the returns

The feedback instruments are designed so that returns can be aggregated rather than read one by one.
The Google Form is required; the field-level workbook sheets below are optional, so expect fewer of them:

- **Feedback form (Google Form)** — sections: About you; Privacy and data sharing; Effort; Fitness for
  purpose; Gaps in the specification; Completing the exercise (Parts B and C); Adoption; Closing remarks.
  Export responses to a sheet and:
  - tabulate the **Fitness for purpose** grid — eleven statements rated strongly disagree to strongly
    agree, required on every submission; a mean below "neutral" on any statement is a flag;
  - tabulate the **SOP grid** (Curation, DataHarmonizer and NTR SOPs) and the **modules** checkbox
    question the same way;
  - treat **Gaps in the specification** (missing fields, missing terms) as the main source of the new
    term request backlog, and **Completing the exercise** (scenario differences, unplaced narrative
    information, validation messages) as the main source of definition fixes;
  - use **Privacy and data sharing** to find fields that cannot be shared onward, and **Adoption**
    for barriers to uptake.
- **Field-level workbook, `Field feedback` sheet** — pre-populated with all 155 fields, with
  drop-downs in the "usable?" and "do you hold this data?" columns. Count by field to find the
  fields that broke for more than one tester.
- **`Missing fields` and `Missing terms` sheets** — add to the backlog from the form's Gaps section.
  Sort by the priority column.
- **`Scenario comparison` sheet** — S1–S3. Where several testers diverge from the answer key on the
  same field, the field definition is at fault, not the testers.
- **`Validation issues` sheet** — validation messages testers found wrong or unclear; each one points
  at a rule in the specification (or a drift between the template and the specification).

Feed the results into a revision list versioned `x.y.z`, where `x` is a field-level change, `y` a
term or identifier change, and `z` a definition, guidance or formatting change — the same scheme
the PHA4GE wastewater specification uses.

---

## Known gaps already built into the scenarios

These are flagged to testers as "known rough edges" so we find out whether they matter in practice:

- No environmental site term for a distribution main (S2). The treated-water sample now uses the new
  `Drinking water treatment plant [ENVO:03600004]` term.
- Only one `presampling activity` per record, so a weather event displaces a process event (S1).
- `gene symbol` and `assay target name` are free text with no controlled vocabulary (S3).
- `organism` is required but has no sensible single value for shotgun metagenomics (S3).
- No explicit parent-sample / derived-from linkage between a sample, a subsample and an isolate;
  `sampling event ID` is doing that work by convention (not exercised in round 1, but still open).
- No `environmental material` term for river or lake sediment — only `Wastewater sediment`
  (not exercised in round 1; it was the surface-water scenario's main finding).

Several of these correspond directly to gaps the needs assessment identified — sample lifecycle
linkage, environmental context beyond wastewater, and assay metadata — so testing round 1 doubles
as a check on whether the specification closed them.

---

## Version history

**v1.2 — 2026-09-16.** Specification-not-tool framing, DataHarmonizer set-up, validation folded into
curation, and all test data brought up to the 2026-09-16 specification export.

- **Testing Instructions rewritten** for clarity, with figures: an "in one sentence" statement that
  the specification is under test and the DataHarmonizer is not; a new §4 on downloading and opening
  the DataHarmonizer .zip from the iMicroSeq repository (filename placeholder highlighted); a
  troubleshooting table; and short numbered steps.
- **Validate is now a step inside Parts B and C** (curate → validate → fix → note → save). The
  separate "Validate and export" part is gone, so the protocol is Parts A–D. The export step is no
  longer in the tester instructions, and the standalone validation folder is no longer part of testing.
- **Answer keys and blank template updated to the 2026-09-16 spec (155 fields, 13 required):**
  columns reordered to match the spec; the two new required fields `data steward contact name` and
  `data steward contact email` filled in; `geo loc name (state/province/territory)` now carries GAZ
  terms (`Ontario [GAZ:00002563]`, `Manitoba [GAZ:00002571]`); S1 daily flow unit is now
  `cubic meter per day (m^3/day)` (previously m^3/h, a workaround); S2 treated water uses
  `Drinking water treatment plant [ENVO:03600004]`; S3 downstream lake uses
  `Freshwater lake [ENVO:00000021]`; S2's Answer Key sheet had a shorter organisation name than its
  DH_import sheet — both now match. All three keys validate with zero errors and zero warnings.
- **Column order matches the DataHarmonizer.** The DataHarmonizer groups fields by section (in order of
  first appearance) and only imports a file whose two header rows match its grid exactly. In the TSV,
  `available data types` / `available data type details` sit in `Sample collection` but after
  `Sample processing`, so the keys, blank template and field-level workbook put them at the end of
  Sample collection, where the DataHarmonizer does. The host fields follow the schema order
  (host (common name), host (scientific name), host age, host age unit, host age bin), all in one
  `Host information` section now that the `Host Information` spelling has been fixed in the spec.
- Worked Example Scenarios, Call-Out, Feedback Form and Field-Level Feedback workbook brought into
  line: counts, filenames, section names, validation now in Parts B and C, the second-validation-tool
  question removed, and the two new fields added to the field list.
- Superseded files moved to `Archive/` subfolders.
- **Package moved to GitHub** (`Testing/` in the iMicroSeq repository). The instructions link to the
  repository folders, `Template/DataHarmonizer.zip` (opened from `web/dist/index.html`) and the
  feedback form, which is now a **Google Form and the only required return**. The field-level
  feedback workbook is optional. The instructions, Call-Out and field-level workbook follow the
  Google Form's questions: notes from Parts B and C feed its Gaps and Completing the exercise
  sections, time spent is no longer asked for, the debrief is arranged by email, and organisations
  (not individuals) are acknowledged if they agree in the form.

**v1.1 — 2026-09-03.** Testing scope narrowed and the local, no-data-sharing model made explicit.

- Testing is stated throughout as local: testers work in the DataHarmonizer on their own machine,
  nothing is uploaded, and **their own data is never returned to us**. Only the feedback instruments
  come back (plus, optionally, the fictional scenario files). Changed in the Call-Out, Testing
  Instructions (§1 callout, §3, Part C callout, §4 table, §5 return table, §6 ethics note) and the
  feedback form.
- The specification is framed as a **common denominator, not a superset** — a core set the majority
  of groups could realistically complete. Three new Likert statements in the feedback form test that
  directly, and §6 asks testers to separate setting-specific gaps from field-wide ones.
- **Five scenarios reduced to three**: S1 municipal wastewater, S2 drinking and source water,
  S3 landfill leachate and mining-influenced water. All three are curated by every tester. The
  surface-water/watershed and marine-aquaculture scenarios are parked, unchanged, in
  `Answer Keys/Not in round 1/`.
- All scenario and answer key content **relabelled as unambiguously fictional** (see above), and real
  place names and coordinates removed — S1's coordinates had been real ones.
- Contact details filled in throughout: Emma Griffiths, emma_griffiths@sfu.ca.
- Files revised in this round carry `_v1.1`. The specification itself, the Master Reference Guide,
  the Curation SOP and the blank template are unchanged at v1.0.

**v1.0 — 2026-08-05.** First draft of the testing package.
