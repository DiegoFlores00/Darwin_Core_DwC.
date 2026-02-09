# Data Standardization and Curation using Darwin Core (DwC)

**Standardization of biodiversity records to the Darwin Core (DwC) format**

This repository presents a data management workflow developed by a network of collaborators with shared interests in the curation, standardization, and publication of biodiversity data.
Its main focus is to improve data quality and interoperability through the application of the Darwin Core standard.

## Objetives

- Consolidate a centralized database containing information on species diversity, distribution, and abundance.
- Standardize and format biodiversity datasets according to the core structure and terms of the Darwin Core (DwC) standard.
- Facilitate data interoperability, reuse, and publication across biodiversity information platforms.

## Target audience

- Researchers and environmental professionals
- Undergraduate and graduate students
- Biodiversity data managers
- Citizen science practitioners and data contributors 

## Use of the Darwin Core Standard

This repository applies the Darwin Core (DwC) standard for structuring and publishing biodiversity data.
Darwin Core is primarily designed to document biological occurrences, the events associated with their recording, and their spatial and temporal context.

As a result, some types of data can be directly represented using DwC terms, while others must be documented as metadata or through extensions.

The table below summarizes the compatibility of different data types with the Darwin Core standard and key considerations for their use.

## Data Type Compatibility with Darwin Core

| Data type | DwC compatibility | Description/considerations|
|--------------|------------------------|-------------------------------|
| Occurrence and distribution data| ✅ High | Core of DwC using terms such as `occurrenceID`, `scientificName`, `eventDate` y `locality`. |
| Presence/absence data | ⚠️ Medium | Documented using `occurrenceStatus`; true absences require a clearly defined sampling desing. |
| Abundance and individual counts | ✅ High | Represented using `individualCount`, `organismQuantity` and `organismQuantityType`. |
| Biomas, size, and life stages | ⚠️ Medium | Life stages  (`lifeStage`) and biomass can be included; detailed morphometrics have limitations. |
| Abiotic measurements | ⚠️ Medium | Included via the `MeasurementOrFact`; extension DwC is not an enviromental data standard. |
| Biotic measurements | ⚠️ Medium | Can be documented using `MeasurementOrFact` or descriptive fields, with limited support for complex interactions. |
| Sampling methods and study areas | ✅ High (metadata) | Documented using `samplingProtocol`, `eventRemarks`, `locationID`, and dataset-level metadata. |
| Sample processing protocols | ❌ Low | Outside DwC's main scope; recommended to document in EML metadata or external documentation. |

## Final cosiderations 
- Darwin Core is **not a comprehensive ecological standart**, but, a schema focused on biodiversity data interoperability.
- Environmental variables, datailed methodologies, and laboratory protocols should be documented primarily as **metadata**.
- Projects with a strong enviromental or oceanographic standars such as **EML**, **OBIS-ENV**, or domain-specific schemas.

## Data Curation and Standardization Setvices

This repository demonstrates the scope and capabilities of biodiversity data curation and standarization under the Darwin Core framework including:

- Curation of occurrence records with or without spatial information (geographic coordinates).
- Standarization and validation of science frames, including correction of typographical errors and taxonomic normalization.
- Conversion of dates to ISO 8601 format, including records with heterogeneous or multiple date formats.
- Normalization of key fields such as **locality. indentifers, individual counts, and taxonomic authorities**.
- Explicit documentation of curation decisions to ensure traceability of the original data.
- Preparation of datasets compatible with publication in infrastructures such as **GBIF** and **OBIS**.
