# Overview

The **iMicroSeq contextual data specification** is informed by a structured needs assessment designed to identify common data requirements across water-based microbial genomics use cases.This process aimed to ensure that the resulting specification is aligned with existing standards, grounded in real-world data collection practices, and sufficiently flexible to support multiple domains spanning environmental monitoring, public health, and One Health applications.

## Approach
### 1. Review of existing standards
Publicly available schemas and reporting standards (e.g. MIxS, NCBI BioSample, PHA4GE wastewater) were reviewed to identify:
- commonly captured data elements
- reusable structures and terminology
- areas of inconsistency or limited coverage

### 2. Stakeholder engagement
A structured questionnaire was used to gather input from projects across environmental monitoring, public health, and genomics. This focused on:
- what data is currently collected
- how it is generated across workflows
- key gaps and challenges in data capture

## Materials
The materials used to conduct the needs assessment are provided in this folder:
- [stakeholder-questionnaire.pdf](https://github.com/cidgoh/iMicroSeq_Contextual_Data_Specification/blob/main/Needs%20assessment/iMicroSeq_Needs-assessment-questionnaire_2025.pdf)

## Role in specification development
The needs assessment underpins the development of the specification by informing the identification of priority data domains, supporting alignment with existing standards, and providing justification for the inclusion or extension of specific data elements. By integrating insights from both standards review and stakeholder input, the process ensures that schema design is evidence-informed, interoperable, and adaptable to evolving requirements while maintaining consistency with best practices in semantic data modelling.

## Summary of results
The needs assessment identified strong alignment across existing standards for core sample descriptors (e.g. identifiers, collection date, and location), but also highlighted key gaps in the representation of process-driven and measurement-rich contextual data. In particular, archival standards such as NCBI BioSample and European Nucleotide Archive (ENA) provide limited support for structured capture of sampling context, sample handling, and environmental measurements, with many elements represented as optional or free-text attributes.

In contrast, the PHA4GE wastewater specification demonstrates the value of a more granular and semantically structured approach, particularly for modelling sampling events, provenance, and value–unit–method measurement patterns. However, some elements (e.g. wastewater-specific picklists and domain constraints) are tailored to wastewater surveillance and require extension to support broader water-based microbial genomics applications. Stakeholder input reinforced the importance of these elements, alongside the need for improved traceability across the sample lifecycle and flexibility to support diverse workflows.

These findings directly informed the design of the iMicroSeq specification, which adopts an event-based, ontology-aligned model to support interoperable, FAIR contextual data while remaining compatible with existing submission standards.