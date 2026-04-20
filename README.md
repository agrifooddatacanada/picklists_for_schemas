# Entry Codes for schemas

Entry codes, also known as enumerations (enums) or picklists, define a controlled set of allowable values for a field in a schema. Instead of accepting free-text input, a picklist restricts entries to predefined options (e.g., "Low", "Medium", "High").

In schema design, entry codes serve two primary purposes:

* Data consistency – Prevents spelling variations, synonyms, and ambiguous entries
* Validation – Ensures that only approved values are recorded, improving downstream analysis and interoperability.

Within the Semantic Engine, you can:
* Select existing entry codes from entry codes catalogued in this repository, or
* Generate custom entry codes tailored to your project needs.

When a schema containing entry codes is used to generate a Data Entry Excel sheet, these controlled values appear as dropdown menus. This constrains user input at the point of entry and reduces the need for later data cleaning.

Entry codes are especially useful for categorical variables such as status, method type, location category, or classification codes, where consistent terminology is essential for reliable aggregation and analysis.

# Backend library for the Semantic Engine

This repostitory contains entry code lists stored as .csv files which are automatically ingested into the Semantic Engine and used to generate the library where they are available for use. We welcome contributions of new entry code lists via the suggestion of new .csv files.

# Syntax for .csv entry codes
The first 9 rows contain space for the entry code metadata with headings on row 1. 
The general row is for language independent information. Below are rows available for language specific metadata. The order of the language doesn't matter, but the first column must specify the language used.

Starting on row 10 are the headings of the entry code list itself and entry code data is contained in row 11.

There is no requirement for the syntax of the entry codes, users can look at the column titles and select which entry code columns they want to use in their schema.

| | title | description | keywords | source |  
|----------|-------|-------------|----------|--------|
| general  |       |           |   |https://soilquality.nres.illinois.edu/bulk-density/ | 
| en       | Bulk density class | Generalized classes; specific restrictive thresholds depend on texture. |          |        |
| fr       | Classe de densité apparente | Classes généralisées; les seuils restrictifs dépendent de la texture. |          |        |
|es |Clase de densidad aparente | Clases generalizadas; los umbrales restrictivos específicos dependen de la textura.| | |
| | | | | |
| | | | | |
| | | | | |
| | | | | |
| Code | Class_en | Description_en | Class_fr | Description_fr |
|------|----------|----------------|----------|----------------|
| BDL  | Low      | Favorable for root growth (texture-dependent) | Faible   | Favorable à l’enracinement (selon la texture) |
| BDM  | Moderate | May affect growth (approaching restrictive) | Modéré  | Peut affecter la croissance (proche du restrictif) |
| BDH  | High     | Restrictive to roots (texture-dependent) | Élevé   | Restrictif pour les racines (selon la texture) |
