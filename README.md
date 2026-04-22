# Indigenous Knowledge Books: Linked Data Dataset

**Author:** avgeller
**License:** [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)
**Course:** MLIS - LS563 Linked Data U of A (first course project)
**Version:** 1.0: April 2026

---

## Table of Contents
- [Dataset Description](#dataset-description)
- [Repository Contents](#repository-contents)
- [Ethics and Positionality](#ethics-and-positionality)
  - [Positionality and Intent](#positionality-and-intent)
  - [Ethical Stance and Data Sovereignty](#ethical-stance-and-data-sovereignty)
  - [Source Conflict Policy](#source-conflict-policy)
  - [Limits of Claims](#limits-of-claims)
  - [Potential Harms and Mitigations](#potential-harms-and-mitigations)
  - [Feedback, Corrections, and Accountability](#feedback-corrections-and-accountability)
  - [Benefit and Reciprocity](#benefit-and-reciprocity)
- [Ontologies and Controlled Vocabularies](#ontologies-and-controlled-vocabularies)
- [Linking Strategy](#linking-strategy)
- [Sample Triples](#sample-triples)
- [Data Notes](#data-notes)
- [Known Limitations and Future Iterations](#known-limitations-and-future-iterations)
  - [CARE Principles Alignment](#care-principles-alignment)
- [Resources](#resources)
- [Sources and Inspiration](#sources-and-inspiration)
- [A Note on AI Assistance](#a-note-on-ai-assistance)

---
# Indigenous Knowledge Books — Linked Data Dataset

## Dataset Description

This dataset contains 50 linked data records of books focused on Indigenous Knowledge, inspired by the Kaggle dataset by ziya07 (2025), Indigenous knowledge systems. It was created to make works by predominantly Indigenous authors more accessible through culturally relevant metadata. The dataset also includes a sample of five books by non-Indigenous authors whose work meaningfully engages with Indigenous perspectives, recognizing the role of cross-cultural scholarship.

The dataset draws on the X̱wi7x̱wa Library Classification System (Indigenous Knowledge Organization, University of British Columbia), using Indigenous-centered subject headings and classification codes in place of Eurocentric frameworks. The dataset distinguishes Indigenous authors' backgrounds from the backgrounds of non-Indigenous authors. While this information may need refinement, it represents the dataset owner's best effort for a first Linked Data course project.

The intent is that this dataset serves as one contribution to a broader, ongoing conversation around intellectual property rights and provenance for Traditional Knowledge (TK) through linked data ontologies. Other projects and initiatives exist in this space; this adds one more entry point: open to iteration and community contribution, including additional authors, contributors, titles, and (where available) author-identified background information.

---

## Repository Contents

| File | Description |
|------|-------------|
| indigenous-knowledge-books.ttl | RDF/Turtle file containing 50 linked data book records |
| indigenous-knowledge-books-mapping.xlsx | Mapping table documenting RDF properties, vocabularies, and transformation notes |
| indigenous-knowledge-books.csv | Source dataset (50 records) |
| ld_model_indigenous-knowledge-books.drawio | Linked data model diagram (DrawIO) |
| README.md | This file |

---

## Ethics and Positionality

### Positionality and Intent

This dataset was built by a fourth-generation descendant of great-grandparents who emigrated from Western and Eastern Europe in the late 1800s and early 1900s who were forced to assimilate upon arrival in New York and New England, and who over generations benefited from housing security and access to higher education that the assimilation made possible. Knowledge of those ancestors stops at arrival, nothing is known beyond that.

Not knowing back seven generations is a gap that sits with this researcher. A lot is quietly lost through assimilation and the pull toward belonging to a dominant society: roots, foundations, the motivations that have shaped how communities and institutions behave today. Archives have the capacity to trace some of that back: migration patterns, ancestral experience, and the longer threads that connect past decisions to present realities. That is part of why archiving resonates personally here, and why the work of description and access feels like it carries weight beyond the technical.

This project does not claim to represent Indigenous perspectives. What it aims to do is make works by Indigenous authors more findable and accessible through metadata that prioritizes self-identification and community-preferred terminology. What it does not aim to do is speak on behalf of any Nation, community, or individual, or treat this dataset as a finished or authoritative resource.

### Ethical Stance and Data Sovereignty

This project seeks to align, where applicable, with Indigenous data governance approaches including the CARE Principles for Indigenous Data Governance (Collective Benefit, Authority to Control, Responsibility, Ethics). Nation-specific protocols and community preferences should guide any reuse especially for culturally sensitive information.

Where TK (Traditional Knowledge) Labels or community-defined permissions exist for a work or author, those should be respected and, where feasible, surfaced in the metadata. Some knowledge is not meant to be linked or made open; that boundary matters and should be honored.

### Source Conflict Policy

When sources conflicted on an author's name, affiliation, or background, the following preference order was applied:

1. Creator self-identification - author-maintained websites, published interviews, or stated bios
2. Nation, community, or Indigenous organization sources — tribal websites, official Nation directories, and Indigenous institutional records
3. Institutional records with clear provenance — university faculty profiles, publisher pages, and library catalogs
4. Secondary sources — encyclopedias, journalism, speaker agencies, and general reference works

For reconciling community, Nation, and group affiliations, Wikidata entity types were used as a controlled vocabulary. The reconciliation interface offered a range of category types: ethnic group (Q41710), First Nation band (Q2882257), federally recognized Native American tribe in the United States (Q7840353), nation (Q6266), ethnic minority group (Q2531956), indigenous people (Q103817), indigenous peoples of North America (Q15571255), ethnic community (Q25380035), ethnolinguistic group (Q4533081), political territorial entity (Q1048835), polity (Q1063239), and broader fallback types like state (Q7275) and entity (Q35120).

Not all cells were tested against each Wikidata category as the priority was both time and the need to ensure affiliations resolved to a Wikidata entity rather than remaining as literals. In practice, these were applied: First Nation band (Q2882257) and ethnic group (Q41710), the latter used for both Indigenous and non-Indigenous authors. One labeling issue remains: the "Indigenous Group" Source Field in OpenRefine needs to be updated to reflect the Wikidata label it was reconciled to, federally recognized Native American tribe in the United States (Q7840353).

The available Wikidata categories are worth discussing, particularly regarding whether they reflect how Indigenous Nations would choose to describe themselves. Of course, no nation should be treated as a monolith, and consensus on preferred terminology remains an open question and a meaningful one for conversations around data sovereignty. Names and affiliations recorded in this dataset are time-bound assertions, not permanent facts. Nations, communities, and individuals may update how they identify over time, and records here should be treated accordingly.

### Limits of Claims

This dataset does not infer tribal affiliation. Imposed labels from ontologies are not treated as definitive. Sensitive details about living people are minimized where possible, and the dataset does not attempt to assert more than what is documented in publicly available, author-proximate sources.

The dataset cannot guarantee accuracy for all records; particularly where biographical sources were limited or where Wikidata divided up background in various categories as mentioned above.

### Potential Harms and Mitigations

Known risks include misidentification of author background, inadvertent reinforcement of colonial categories, and exposure of personal information. Mitigations in place include: use of literal strings and keeping the literals intact over imprecise URIs, source background notes to document uncertainty, minimal disclosure for sensitive details, and open correction pathways (see below).

### Feedback, Corrections, and Accountability

Corrections, contested claims, and community feedback are welcome and taken seriously. Self-identification takes priority in any disputed record. When a change is made based on feedback, the update will be documented transparently: noting what changed, why, and where the information came from.

To request a correction or flag a concern, open an issue in this repository or contact the dataset author directly. All feedback will be logged and acted on in future versions.

### Benefit and Reciprocity

The intended benefit of this project is improved discoverability for community research, easier correction pathways, and support for community-defined naming over imposed terminology. Contributions, whether corrections, additions, or verifications, will be acknowledged in future versions of the dataset.

This project does not extract value from Indigenous knowledge for academic gain alone. The goal is that the dataset remains freely available and genuinely useful to the Nations and communities whose authors and works it describes.

---

## Ontologies and Controlled Vocabularies

The dataset uses the following ontologies, vocabularies, and namespaces:

| Prefix | Namespace | Purpose |
|--------|-----------|---------|
| schema: | http://schema.org/ | Book, author, publisher metadata |
| bf: | http://id.loc.gov/ontologies/bibframe/ | BIBFRAME title, instance, ISBN, classification |
| dc: | http://purl.org/dc/elements/1.1/ | Subject headings, contributors |
| foaf: | http://xmlns.com/foaf/0.1/ | Person names |
| wd: | https://www.wikidata.org/wiki/ | Wikidata authority URIs |
| viaf: | https://viaf.org/en/viaf/ | VIAF authority URIs |
| xsd: | http://www.w3.org/2001/XMLSchema# | Datatypes (xsd:gYear) |
| rdf: | http://www.w3.org/1999/02/22-rdf-syntax-ns# | RDF type declarations |

**Classification System:** Subject headings and classification codes follow the X̱wi7x̱wa Library Classification System (University of British Columbia), an Indigenous-centered system that replaces Eurocentric classification frameworks.

**Language Codes:** Both ISO 639-1 two-letter and ISO 639-3 three-letter codes are used throughout (e.g., `en`, `es`, `pt`, `zap`, `gun`, `nhd`), looked up via the [BCP47 Language Subtag Lookup](https://r12a.github.io/app-subtags/) (r12a).

---

## Linking Strategy

The dataset connects records to external authority sources to improve interoperability and support provenance. The linking strategy works as follows:

**Author identity and background:** Indigenous author backgrounds are anchored in each author's self-identified Nation, community, or heritage as documented in publicly available biographical sources. Wikidata URIs (wd:) are used where an accurate match was available; a literal string is used where no suitable URI existed, to preserve the author's specific self-identification rather than force an imprecise match.

Non-Indigenous author backgrounds reflect ethnic or cultural heritage as described in publicly available biographical sources. Where no Indigenous background was mentioned, the author was treated as non-Indigenous.

Source background notes document cases where available Wikidata URIs did not precisely match an author's stated indigeneity, explaining the reasoning behind URI selection or the decision to use a literal string instead.

**Bibliographic authority:**
- VIAF URIs (viaf:) link to internationally recognized authority records for authors and contributors
- Wikidata URIs (wd:) link authors and subjects to structured knowledge graph entries
- BIBFRAME (bf:) is used for bibliographic structure including titles, instances, ISBNs, and classification codes

**ISBNs:** All records use `bf:Isbn` for ISBN identification. Book020 (*Alfabeto mazateco* by Juan Gregorio Regino, 1993) carries a 10-digit ISBN (`9686951067`); all other records use 13-digit ISBNs.

---

## Sample Triples

The following RDF/Turtle triples illustrate the structure and linking strategy used in this dataset.

```turtle
@prefix schema: <http://schema.org/> .
@prefix bf:     <http://id.loc.gov/ontologies/bibframe/> .
@prefix dc:     <http://purl.org/dc/elements/1.1/> .
@prefix foaf:   <http://xmlns.com/foaf/0.1/> .
@prefix wd:     <https://www.wikidata.org/wiki/> .
@prefix viaf:   <https://viaf.org/en/viaf/> .
@prefix xsd:    <http://www.w3.org/2001/XMLSchema#> .
@prefix rdf:    <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .

:Book024  rdf:type            schema:Book;
        bf:classification     "X; W; T; P; PW; YT-YUE";
        bf:identifiedBy       [ rdf:type   bf:Isbn;
                                rdf:value  "9788578883614"
                              ];
        dc:contributor        [ rdf:type       foaf:Person;
                                schema:sameAs  viaf:6101164913200718980007;
                                foaf:name      "Mirim, Wera Jeguaka"
                              ];
        dc:contributor        [ rdf:type       foaf:Person;
                                schema:sameAs  viaf:761150323684309971918;
                                foaf:name      "Junqueira, Fran"
                              ];
        dc:subject            "Languages; Arts; Worldview; Knowledge Keeping; Women; Guarani"@en;
        schema:author         [ rdf:type            foaf:Person;
                                schema:description  "Tupí-Ruaraní of Brazil (per elfikurten.com.br/2021/12/olivio-jekupe.html)"@en , "Tupi–Guarani peoples"@en;
                                schema:sameAs       wd:Q4465585;
                                foaf:name           "Jekupe, Olivio "
                              ];
        schema:datePublished  "2017"^^xsd:gYear;
        schema:inLanguage     "gun" , "pt";
        schema:name           [ rdf:type  schema:Book;
                                bf:title  "O presente de Jaxy Jatere";
                                bf:title  wd:Q121275825
                              ];
        schema:publisher      [ rdf:type     schema:Organization;
                                schema:name  "Panda books (Toronto, Ont.)"
                              ] .
```

---

## Data Notes

- **Indigenous author backgrounds** are anchored in each author's self-identified Nation, community, or heritage as documented in publicly available biographical sources. Wikidata URIs are used where an accurate match was available; a literal string is used where no suitable URI existed, to preserve the author's specific self-identification.
- **Non-Indigenous author backgrounds** reflect ethnic or cultural heritage as described in publicly available biographical sources. Where no Indigenous background was mentioned, the author was treated as non-Indigenous.
- **Source background notes** document cases where available Wikidata URIs did not precisely match an author's stated indigeneity, explaining the reasoning behind URI selection or the decision to use a literal string instead.
- **ISBN note:** All records use `bf:Isbn` for ISBN identification. Book020 (*Alfabeto mazateco* by Juan Gregorio Regino, 1993) carries a 10-digit ISBN (`9686951067`); all other records use 13-digit ISBNs.
- **Language codes** follow both ISO 639-1 two-letter and ISO 639-3 three-letter codes (e.g., `en`, `es`, `pt`, `zap`, `gun`, `nhd`), looked up via the [BCP47 Language Subtag Lookup](https://r12a.github.io/app-subtags/) (r12a).
- **Classification** uses X̱wi7x̱wa Library Classification System codes in place of Dewey Decimal.

---

## Known Limitations and Future Iterations

1. Author biographical sources can be improved upon through direct engagement with authors where possible.
2. Description sources can be improved upon in future iterations, particularly where richer or community-authored descriptions become available.
3. Some author background information may require verification or correction by community members with closer knowledge of the relevant Nations and peoples.
4. This dataset is intended as a foundation for community contribution and crowd-sourcing. Contributions adding new titles, authors, or correcting existing records are welcome.
5. A companion CSV or XLS file documenting the various projects, programs, organizations, initiatives, and best practices encountered through this project regarding indigeneity and data sovereignty will be added in a future version, serving as a resource for others doing similar work.

### CARE Principles Alignment

This dataset aspires to align with the CARE Principles for Indigenous Data Governance (Collective Benefit, Authority to Control, Responsibility, Ethics) as established by the Global Indigenous Data Alliance (GIDA). CARE alignment is understood here in the context of a bibliographic dataset, specifically how Indigenous authorship and cultural identity are attributed, described, and made accessible through linked data.

**What this dataset has done to honor the CARE Principles:**

- Grounded identity descriptors in authors' own self-identification, using author-maintained websites and community sources as the first preference in the source conflict policy
- Used literal strings over imprecise URIs where no accurate Wikidata match existed, to preserve the specificity of an author's stated indigeneity
- Documented decision-making inline through source background notes, explaining URI selection and known limitations transparently
- Applied the X̱wi7x̱wa Library Classification System in place of Eurocentric frameworks, centering Indigenous knowledge organization
- Included an open correction pathway so that self-identification takes priority in any disputed record
- Acknowledged positionality explicitly, and committed to this dataset remaining freely available and genuinely useful to the Nations and communities whose authors it describes

**What is needed in the next iteration:**

*Authority to Control*
- Verify identity descriptors with authors or their representatives where possible
- Check whether represented nations have data governance policies (e.g. OCAP® for Canadian First Nations) that should inform how their members are described

*Responsibility*
- Move inline decision notes to a formal methodology document
- Add `schema:dateModified` to records that are corrected or updated over time

*Ethics*
- Audit and document the inconsistency in how Indigenous vs. non-Indigenous authors are described
- Review any descriptors that may reflect colonial-era terminology

*Collective Benefit*
- Document the intended audience and use cases for the dataset
- Explore sharing the dataset with Indigenous library networks for feedback
- Consider contributing corrections or additions back to Wikidata to improve Indigenous author representation in the broader linked data community

---

## Resources

The following projects, programs, organizations, initiatives, and best practices were encountered through the development of this dataset. They are collected here as a reference for others doing similar work at the intersection of indigeneity, data sovereignty, and linked data.

### Principles and Frameworks

**Global Indigenous Data Alliance (GIDA) — CARE Principles for Indigenous Data Governance**
A framework centering Indigenous rights and interests in data: Collective Benefit, Authority to Control, Responsibility, Ethics. Often positioned as a complement and counterbalance to FAIR data principles.
[https://www.gida-global.org/care](https://www.gida-global.org/care)

**Local Contexts — Traditional Knowledge (TK) Labels**
A practical tool for communities to add cultural protocols to digitized materials, signaling how knowledge should be accessed, used, and attributed.
[https://localcontexts.org/labels/traditional-knowledge-labels/](https://localcontexts.org/labels/traditional-knowledge-labels/)

**Oral History Association (OHA) — Principles and Best Practices**
Ethical and methodological standards for oral history projects, emphasizing transparency, informed consent, narrator well-being, shared authority, and responsible access and use. Relevant where this dataset intersects with interview or oral-history-adjacent sources.
[https://oralhistory.org/principles-and-best-practices-revised-2018/](https://oralhistory.org/principles-and-best-practices-revised-2018/)

---

## Sources and Inspiration

1. ziya07. (2025). *Indigenous Knowledge Classification* [Data set]. Kaggle. https://www.kaggle.com/datasets/ziya07/indigenous-knowledge-classification
2. X̱wi7x̱wa Library: Indigenous Knowledge Organization. University of British Columbia. https://xwi7xwa.library.ubc.ca/collections/indigenous-knowledge-organization/
3. Cutter, C. A. (1904). *Rules for a dictionary catalog* (4th ed.). Archive.org. https://archive.org/details/rulesfordictiona00cutt/page/12/mode/2up
4. Indigenous Librarianship: Brian Deer Classification System. University of British Columbia. https://guides.library.ubc.ca/Indiglibrarianship/briandeer

---

## A Note on AI Assistance

This project was developed as part of LS 563 Linked Data at the University of Alabama. Feedback and coaching from the course professor, along with webinars and Indigenous policy resources, shaped the direction and decisions throughout. AI helped clean up the written content to make it flow in a user-friendly format and feel less overwhelming for potential dataset users.

Claude AI (Anthropic) was used as an additional technical guide at points where the Turtle file was not functioning as expected particularly when added columns introduced errors that needed to be worked through. Claude helped troubleshoot specific problems including the RDF transformation, the linked data model diagram, and getting the Turtle file to render correctly on GitHub.

The ideas, research, and conceptual direction are the author's own. The sources consulted, the frameworks chosen, and the thinking behind the metadata decisions all reflect the author's work and learning. Where Claude assisted, it was in working through technical problems and shaping the formal written expression of those ideas, not in generating the intellectual content itself.
